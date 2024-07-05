# Deep Learning Model

## Overview of the Analysis: ##
The purpose of this analysis is to develop a binary classifier using a deep learning model to predict whether applicants funded by Alphabet Soup will be successful. The goal is to effectively classify applicants based on provided features to optimize funding decisions.

## Data Preprocessing: ##
![preprocessing](Resources/preprocessing.PNG)

EIN and NAME — Identification columns<br/>
APPLICATION_TYPE — Alphabet Soup application type<br/>
AFFILIATION — Affiliated sector of industry<br/>
CLASSIFICATION — Government organization classification<br/>
USE_CASE — Use case for funding<br/>
ORGANIZATION — Organization type<br/>
STATUS — Active status<br/>
INCOME_AMT — Income classification<br/>
SPECIAL_CONSIDERATIONS — Special considerations for application<br/>
ASK_AMT — Funding amount requested<br/>
IS_SUCCESSFUL — Was the money used effectively<br/>

### Target Variable(s): ###
The target variable for the model would be the "IS_SUCCESSFUL" column, indicating whether an applicant was successful or not.

### Feature Variable(s): ###
The feature variables would include attributes such as "APPLICATION_TYPE," "AFFILIATION," "CLASSIFICATION," etc., which are used to predict the target variable.

### Variables to Remove: ###
After a few rounds of testing, I filtered out outliers from the feature variables such as "CLASSIFICATION" and "APPLICATION_TYPE." Variables like "EIN" (Employer Identification Number) may not contribute to the prediction and were removed altogether from the input data.

![cutoffs](Resources/cutoffs.PNG)

## Compiling, Training, and Evaluating the Model: ##
![model](Resources/model.PNG)

### Neurons, Layers, and Activation Functions: ###
The neural network model was created using the Rectified Linear Unit (ReLU) function with the X_train data (based on application_df). After some fine tuning with different amounts of layers, I settled on a hidden layer of 80 and 30 with a sigmoid output layer of 1. This provided the best balance between loss and accuracy.

![array](Resources/array.PNG)

## Summary: ##
Model was trained with 100 epochs putting the overall loss value at 0.5367 with an accuracy of 0.7966 meaning the model correctly predicted the target variable about 79.66% of the time. If I were to use a differnt model for this set of data, I would recommend decision trees as they are easy to interpret and can handle both numerical and categorical data which perfectly suit this funding data. Decision trees can be particularly useful for classification tasks and can handle non-linear relationships in the data making it ideal for the application.

![results](Resources/results.PNG) <br/>
