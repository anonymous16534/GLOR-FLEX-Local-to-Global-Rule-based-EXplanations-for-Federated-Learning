# GLOR-FLEX: Local to Global Rule-based EXplanations for Federated Learning


The increasing spread of artificial intelligence applications has led to decentralized frameworks that foster collaborative model training among multiple entities. One of such frameworks is federated learning, which ensures data availability in client nodes without requiring the central server to retain any data. Nevertheless, similar to centralized neural networks, interpretability remains a challenge in understanding the predictions of these decentralized frameworks. The limited access to data on the server side further complicates the applicability of explainers in such frameworks. To address this challenge, we propose GLOR-FLEX, a framework designed to generate rule-based global explanations from local explainers. GLOR-FLEX ensures client privacy by preventing the sharing of actual data between the clients and the server. The proposed framework initiates the process by constructing local decision trees on each client's side to produce local explanations. Subsequently, by using rule extraction from these trees and strategically sorting and merging those rules, the server obtains a merged set of rules suitable to be used as a global explainer. We empirically evaluate the performance of GLOR-FLEX on three distinct tabular data sets, showing high fidelity scores between the explainers and both the local and global models. Our results support the effectiveness of GLOR-FLEX in generating accurate explanations that efficiently detect and explain the behavior of both local and global models.


## Code execution:

1. To execute The code, first we need to run the code 'preparing the non-iid data for model.ipynb' or 'preparing the data for model and the tree.ipynb' to prepare the data set for the experiments, the choice depends on the preferences of the user.
2. The second step is to train the HOLDA federated learning models using the code 'train the FL.ipynb'. To modify the structure of the models or the number of clients, the folder called 'holda_not_hier.xml' inside the folder 'architectures
/holda'.
3. Then we train the local explainers, using the code 'Trepan_train_the_trees.ipynb'.
4. the next step is to train the GMM models locally to generate the synthetic data using the code 'load the decision trees and create the rules and the gmm.ipynb'.
5. The final step is to merge the rules generated by the trees using the code 'Glocalx.ipynb'.
