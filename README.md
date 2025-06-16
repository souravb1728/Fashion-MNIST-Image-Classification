# Fashion-MNIST-Image-Classification
Here we analyze the MNIST fashion data and model a Fully Connected Neural Network to perform Image Classification

#### About Data : 
We are provided with a train data of 60000 images and test data of 10000 images consisting of 10 different classes of clothes. Using Neural Network we will create a model to predict the classes from the input images.

**Link for the data :** 

https://www.kaggle.com/datasets/zalando-research/fashionmnist

**Basic Analysis of the data :**
- Visualizing the sample images using imshow
- All the classes have same distribution of 10% each


### Predictive Analysis

1. First we will scale the features for train and test data. This could be done by dividing all the features with 255 (Maximum Pixel value)
2. Then we convert the categorical labels into One-Hot encoded format to suit the neural network’s output layer

#### Designing a fully connected Neural Network

Now that we have processed the features and classes we are ready to design the model

**Input :** Images of shape (28,28,1)

**Hidden Layers :** 

1. Dense layer of 32 neurons with activation function as relu
2. Another Dense layer of 32 neurons with activation function as relu
3. Flatten the array to transform into 1-D vector which is required to compute the Class probabilities
4. Another Dense layer of 128 neurons with activation function as relu

**Output :** Dense layer of 10 neurons with activation function as softmax

Training the model with following parameters :
1. loss function - *categorical cross-entropy*
2. optimizer - *stochastic gradient descent*
3. metrics - *accuracy*
4. epochs - *50*
5. batch size - *400*

#### Checking Model Performance : 

Model gives an accuracy of 88.5% on train data and 87% on test data which is decent for this type of Image Classification task

**Visualizing the loss and accuracy :**

Plotting graph of training and testing data to compare both loss and accuracy to identify any signs of overfitting or underfitting. Based on the accuracy data we can say there seems a little overfitting. 

**Class Prediction :**

Performed on test data to identify the prediction for any particular input

This can be analyzed further with the help of CNN to improve the accuracy and check the overfitting

