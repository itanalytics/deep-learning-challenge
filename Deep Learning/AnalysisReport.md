# Analysis Report: Deep Learning Model

## Overview
The nonprofit foundation Alphabet Soup wants a tool that can help it select the applicants for funding with the best chance of success in their ventures. 
The goal is to create a binary classifier that can predict whether applicants will be successful if funded by Alphabet Soup.

## Data Pre-processing
1. What variable(s) are the target(s) for your model?
- The target for the model is the 'Is-Successful' column, which states whether the money was used effectively or not.
2. What variable(s) are the features for your model?
- The features used by this model are NAME, APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, and ASK_AMT
3. What variable(s) should be removed from the input data because they are neither targets nor features?
- EIN was removed because it was an identifier and also a number that doesn't hold useful information for the model's decision making. STATUS and SPECIAL CONSIDERATIONS had minimal variance and therefore were removed.
## Compiling, Training, and Evaluating the Model
1. How many neurons, layers, and activation functions did you select for your neural network model, and why?
- This model uses two hidden layers, the first with 100 neurons and the second with 50 neurons. The model performed slightly better with two rather than three hidden layers. The first activation function was a tanh function, the second a relu, and the output function was sigmoid. Starting with a tanh function improved the accuracy in the optimized model.
2. Were you able to achieve the target model performance?
- Yes, the target was 75% accuracy and a 79% was obtained.
3. What steps did you take in your attempts to increase model performance?
- To increase model performance, I reevaluated each column to decide which columns should be dropped and which rare values should be binned to improve the features being passed into the model. Then different models were designed with two or three hidden layers and different initial activation functions until the target outcome was surpassed.
## Summary
This model can correctly classify the test data with a 79% accuracy. This accuracy was obtained by combining many different features into an "Other" category, so the classification is most reliable if an applicant's features match the more common ones (ie. Most common application types, more than 10 total applications, a Trust or Association).  
Another possible model to use is a logistic regression model. Logistic regression is a common model for binary classification. With this same dataset, a logistic regression model acheives 78% accuracy.
