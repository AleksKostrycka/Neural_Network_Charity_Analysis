# Neural_Network_Charity_Analysis

## Overview

The purpose of this project is to use deep-learning neural networks with the TensorFlow platform in Python, to analyze and classify the success of charitable donations. We use the following methods for the analysis:

* preprocessing the data for the neural network model,
* compile, train and evaluate the model,
* optimize the model.

## Results

### Data Preprocessing

* The following variables and neither features nor targets: EIN and NAME, they are identification information and removed.
* APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, STATUS, INCOME_AMT, SPECIAL_CONSIDERATIONS, ASK_AMT are the features for our model.
* The column IS_SUCCESSFULis considered as the target for our deep learning neural network.

### Compiling, Training, and Evaluating the Model

* The deep-learning neural network model is made of 2 hidden layers with 80 and 30 neurons respectively. The input data has 43 features and 25,724 samples.To speed up the training process, we are using the activation function ReLU for the hidden layers. As our output is a binary classification, Sigmoid is used on the output layer.
For the compilation, the optimizer is adam and the loss function is binary_crossentropy.

* The model accuracy is under 75%. Reached a 73% accuracy. This is not a satisfying performance to help predict the succcess of the charity donations.

* To increase the performance of the model, we applied bucketing to the feature ASK_AMT and organized the different values by intervals.
We increased the number of neurons on one of the hidden layers, then we used a model with three hidden layers.
We also tried a different activation function (tanh) but none of these steps helped improve the model's performance.

## Summary
The results of our model did not reach the desired 75% accuracy, we reached a 73% accuracy. This would indicated that the model is not permforming to the desired outcome in predicing the charities to donate to. Another option could be to use the supervised machine learnig model such as the Randon Forest Classifier to combine a many decision trees to generate a classified output and evaluate its performance against our deep learning model.


