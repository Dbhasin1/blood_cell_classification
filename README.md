# blood_cell_classification
In this repository I take up the task of classifying red blood cells into four different classes, namely - Eosinophil, Lymphocyte, Monocyte, and Neutrophil. 
I undertook two different approaches, one depends on the neural network architecture to extract the features from the blood cells and then classify them whereas the other utilises a heuristic search algorithm based on the concepts of natural selection and genetic to select features followed by a KNN-Classifier to classify the blood-cells. 
APPROACH 1 - Combining Convolutional Neural Network With Recursive Neural Network
This approach was heavily inspired from https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8402091 and https://arxiv.org/pdf/2101.03604.pdf where the authors show that combining a CNN with RNN improves classification performance by virtue of preserving the temporal and spatial information of image features and can learning the structured information of image features. 
My implementation achieved an accuracy of 85%, the individual precision, recall and f1 scores for each blood-cell class are displayed in the notebook itself 
Scope for Improvement:
• Usage of transfer learning method to migrate pretrained weight parameters to the CNN branch, thereby enhancing the robustness of the combined model and accelerating the convergence of the model.


APPROACH 2 - Genetic Algorithm + KNN for Feature Reduction and classification


