# Report

## Overview

In this challenge a binary classifier model is deployed using a deep learning and neural networks for classifying the likelihood of applicants receiving funding from Alphabet Soup, a nonprofit foundation. The dataset, comprising details on more than 34000 organizations, encompasses various features such as application type, affiliated industry sector, government organization classification, funding use case, income category, requested funding amount, and the effectiveness of fund utilization.

Data preprocessing involves eliminating unnecessary columns, encoding categorical variables, and dividing the dataset into training and testing sets. Subsequently, the neural network model is formulated, trained, and assessed for both loss and accuracy. Optimization steps are then performed by adjusting input data, changing the number of neurons and hidden layers, utilization of different activation functions etc.

## Results
### Data Prepocessing

* What variable(s) are the target(s) for your model?
   
The target variable is `IS_SUCCESSFUL` - this variable determines the outcome of a charity donation being successful or not.
   
* What variable(s) are the feature(s) for your model?
   
The non-target columns are the features (i.e. all other variables)
   
* What variable(s) should be removed from the input data because they are neither targets nor features?
 
The EIN variable was removed because it is a unique identifier for an entry in the data and will not help inform model training/testing.

### Compiling, Training, and Evaluating the Model

* How many neurons, layers, and activation functions did you select for your neural network model, and why?

For the final optimised model I had four hidden layers all with setting ReLU `activation='relu'`. The layers were, 80, 30, 20 and 10 for each successive layer. This was chosen because as I tested different layers, and activation types, the accuracy, though not initially pushing above around 72%, did go up in the final optimisation to 78.4%.

* Were you able to achieve the target model performance?

Yes, specifically after including the `NAME` feature for training the model.

* What steps did you take in your attempts to increase model performance?

First the cut off points were changed for the `APPLICATION_TYPE` and `CLASSIFICATION` features to 1000 and 2000 respectively. The number of nodes were altered too and the number of layers used. Finally when including the `NAME` feature, the accuracy went up to 78.4%.

## Summary

This deep learning model using neural networks was developed with the TensorFlow library based on Keras and achieved an accuracy of 78.4%. This classification problem can be approached using a Random Forest Classifier which will likely require less optimisation and be more accurate (with the potential risk of overfitting).