# Semantics-2021
The framework for SEMANTICS 2021


(A) The excel files **replace** and **remove** xlsx contain the object action labels from Something-Something Dataset that were removed and replaced, for our experiments.\
(B) The **results.zip** folder contains the results of all the methods described in the paper (see Section 4.3) and the relation pattern method.\
(C) The **Object-Action Association Extraction from Knowledge Graphs.zip** contains the code for constructing the subgraphs, for the methods described in the paper, and our relation pattern mechanism. Each subfolder is described bellow.

(C.i) **crossValidation** folder has the code with which we created the folds based on the positive and negative object action relations.

(C.ii) **dataCleaning** folder contains the code with which we addressed queries to ConceptNet, to see which labels of objects and actions belong to the ConceptNet knowledge graph (see  Section 4.1.).

(C.iii) **graphConstructor** folder has the code with which we construct the subgraphs described in section 3.1, one needs to run the DemoMain.py to construct a subgraph, after (s)he inserts the labels (s)he desires. Moreover, the subgraphs we have created, 148 sub graphs that refer to object labels and 25 sub graphs that refer to action labels, can be found in **subgraph** folder, subgraphContextFinal-subgraphContextNegative-subgraphContextPositive are some helping files.

(C.iv) **posNegPattern** folder has the code with which we compute the relation patterns.

(C.v) **threshold** folder has the code which computes the results for the three methods described in the paper that are not ours, and the weights of importance for our relations pattern method.

(C.vi) **demo_bilinear** has the code for the AllenAI-Commonsense (top-k) method, that is relying on the library: https://github.com/allenai/commonsense-kg-completion. The method convert_json_gt_to_txt is used to convert the positive and negative json ground truth files, given above, to csv readable by this (and other embeddings-based) libary(ries). The main method, given a confidence threshold (defaults to 0.0) and k value (defaults to 5), evaluates the precision, recall, and F1 score of the pre-trained model (the pre-trained .pkl model file from the external library is also contained in this folder). 


Any disambiguation needed, please contact: valexande@csd.auth.gr
