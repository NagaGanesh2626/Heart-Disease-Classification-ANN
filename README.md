# Heart-Disease-Classification-ANN

This project is a class assignment by Mike X Cohen sir on Mastering Deep Learning using PyTorch. Although for a Dataset that contains less feature examples, for educational purposes I have used a Feed Forward Network to check how good a model can perform.

Understanding the DataSet:

* The Dataset has total 297 feature examples with 13 features and one target column with which the model can be trained.
* The model is multiclass classification (4) but to simplify the process of classifying and for academical purposes it has been converted to a binary classification problem. ( 0-2 : 0 & 2-4: 1).

Neural Network architecture:
* * Input Layer: Size = (13,32), activation = ReLU
  * Hidden Layer_1: Size = (32,64), activation = ReLU
  * Hidden Layer_2: Size = (64, 32), activation = ReLU
  * Hidden Layer_3: Size = (32,10), activation = ReLU
  * Output Layer: Size = (10,1), activation = Linear
* Loss Function: Mean Squared Error, Optimizer = Adam
* Architecture is inspired from Mike X Cohen sir.

Final Observations:

* The model got a test accuracy of 84 % when relu activation function is used in the hidden layer, with the train accuracy being 100%. Nummber of batches = 16
* The model got a test accuracy of 86% percent when prelu, tanh, and elu activation functions in the hidden layer, with batch-size = 16
* It has been observed that using 16 batches, the training accuracy was 100% while test accuracy was 84% while the max test accuracy is 86%, so this means the model was memorizing the training data and is not able to generalize and work on new test data.
* So, by changing the batch-size to 32, the accuracy increased to 92% with 150 epochs
* My model achieved a test accuracy of 92% with 150 epochs and a batch size of 32, while the sir's model achieved a 90% accuracy with the 100 epochs and a batch size of 20.
