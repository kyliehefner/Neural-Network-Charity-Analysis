# Neural Network Charity Analysis

## Overview
### Purpose
The purpose of this project is to create a deep learning model that will predict whether organizations will be successful if funded. The data consists of a CSV of organizations that have recieved funding from a company, Alphabet Soup. The data includes information such as industry affiliation, requested amount, and use case, as well as whether or not the company was successful with the funding. The neural network will serve as a binary classifier with success being the target variable.

## Results
### Data Preprocessing
- The target variable for this analysis is the column "IS_SUCCESSFUL", which is labeled 1 if the organization that recieved money from Alphabet Soup was used effectively, and 0 if it was not.
- The features of the neural network model consist of the application type, industry affiliation, government classification, use case for funding, organization type, active status, income amount, special considerations, and requested amount.
- The EIN and Organization Name are neither targets nor features, and are removed from the data set in preprocessing.
### Compiling, Training, and Evaluating the Model
- I selected 3 hidden layers for my deep learning model so that the model could adapt easily to non-linear relationships. I selected 38 neurons in the input layer since that's the number of features after preprocessing. I selected 30 neurons in the first hidden layer, then 10, then 3 because 30 is less than the input layer neurons, while 10 and 3 are about 1/3 of the previous layer. 
- I was not able to achieve the target model performance of 75%. My highest accuracy was 72.9%
- To increase model performance, I removed the noisy variable "USE_CASE" from the input variables, increased the number of hidden layers to 3, increased the number of neurons in the first two hidden layers, changed the activation function of the hidden layers to sigmoid, and changed the activation function of the output layer to softmax.

## Summary
### Overall Results
The highest accuracy achieved was 72.9%, less than the target model performance of 75%. Removing the USE_CASE variable increased the accuracy. Increasing the number of hidden layers and neurons in each layer also increased the accuracy. Changing the activation functions reduced the accuracy significantly, so the original choices of ReLu and Sigmoid were best for the hidden layer and output layer activation functions respectively. An accuracy of 73% is helpful for determing which organizations Alphabet Soup should invest in, but more optimization could be done to increase the accuracy of the model.
### Recommendation
I would recommend using a random forest classifier as an alternative to the deep learning model for predicting success outcomes of these organizations. A random forest classifier is easy to interpret and explain, while maintaining high accuracy, scalability, and ability to adapt to non-linear data. With enough estimators, a random forest model should be able to achieve similar accuracy to our deep learning model, perhaps more. 
