# blood_cell_classification
In this repository I take up the task of classifying red blood cells into four different classes, namely - Eosinophil, Lymphocyte, Monocyte, and Neutrophil. 
I undertook two different approaches, one depends on the neural network architecture to extract the features from the blood cells and then classify them whereas the other utilises a heuristic search algorithm based on the concepts of natural selection and genetic to select features followed by a KNN-Classifier to classify the blood-cells.

### Approach 1 - Combining Convolutional Neural Network With Recursive Neural Network

This approach was heavily inspired from https://ieeexplore.ieee.org/stamp/stamp.jsp?tp=&arnumber=8402091 and https://arxiv.org/pdf/2101.03604.pdf where the authors show that combining a CNN with RNN improves classification performance by virtue of preserving the temporal and spatial information of image features and can learning the structured information of image features. 
#### Model Architecture 

#### Results 
My implementation achieved an accuracy of 85%, the individual precision, recall and f1 scores for each blood-cell class are displayed in the notebook itself 
#### Scope for Improvement:
• Usage of transfer learning method to migrate pretrained weight parameters to the CNN branch, thereby enhancing the robustness of the combined model and accelerating the convergence of the model. <br />


### Approach 2 - Genetic Algorithm + KNN for Feature Reduction and classification

In this approach I used genetic algorithm to create feature vectors. The method is based on PCA-generated features to define initial population for genetic evolution. This is followed by the genetic evolution and finding significance of individual feature components. The feature vectors are then weighted according to their significance. The initial extraction of features was done from RBC images using VGGNet. 
#### Model Architecture 

#### Results 
The implementation is done in https://colab.research.google.com/drive/1SVUUi1gALjEqPYskvJ5AJA7uqPoyci-E?usp=sharing. Applying a kNN Classifier on top of the extracted features gave me an accuracy of 73%

#### Scope for Improvement 
• Genetic Algorithms are costly in computational terms since the evaluation of each individual requires the training of a model and these algorithms can take a long time to converge since they have a stochastic nature. Due to time limitations I had to decrease the number of iterations I ran the algorithm for. 
• Feature selection could have been enhanced by applying statistical operations to exclude irrelevant and noisy features, and by making it more computationally efficient and stable









