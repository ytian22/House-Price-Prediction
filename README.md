# House-Price-Prediction
Explored features of houses, evaluated model fit and assumptions, and constructed a predictive model to estimate new house prices. 

## Part I: Exploratory Modeling  
For this part of the case study, our goal is to determine and explain what features of a house (the regressors) are most relevant in determining its expected sales price (the regressand). Since we are concerned with the explanatory power of the model, we need to validate assumptions for our final model.  

### 1. Exploratory Data Analysis: 
* Examine the structure of raw data: total of 1470 observations and 81 variables 
* Identify the data type of variables: composed of 43 factor/character variables and 38 numeric variables
* Identify variables with NAs: total 17 variables with NA values
* Imputation of missing values  

### 2. Variable Selection and Fit the Model  
* Build OLS model with all variables
* Check for Multicollinearity
* Use lasso to select variables
* Use selected variables to fit OLS model

### 3. Validation of Model 
* Quick Diagnostic Analysis
* Formally test assumptions
* Box-Cox Transformation
* Transform skewed regressor
* Compare the model accuracy

## Part II: Predictive Modeling 
We see that LASSO reduces a number of estimators to zero, while Ridge shrinks the estimators but none will ultimately reach exact zero. Elastic Net has a combination of effects of both Ridge and LASSO. 

The following describes the steps taken for fitting the Ridge regression:
* Create lambda grid
* Split dataset into train (50%) and test (50%) by random sampling
* Fit Ridge regression model (glmnet) on the train set of data with alpha = 0
* Cross-validate the model with cv.glmnet and choose the best lambda
* Predict the response on test set of data using the lambda chosen from step 4
* Calculate the MSPE from the prediction


## Full Report: https://drive.google.com/drive/u/1/folders/1_dVRUV_y0H203m3dMgM7bVBB_VpK-iu5
