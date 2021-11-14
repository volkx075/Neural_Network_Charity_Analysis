# Neural Network Charity Analysis
## Overview
Our goal is to predict whether or not applicants will be succeful if they are funded by Alphabet Soup. We are starting with a CSV file with more than 34,000 orgnizations. First, we will bin certain columns in the data and then run a deep learning model to determine whether an applicant will be successful if they are funded by the company. Our goal is to have a model that has at least a 75% accuracy.
## Results
### Data Preprocessing
- The variable considered the target of my model is IS_SUCCESSFUL.
- The variables that are considered the features of my model are APPLICATION_TYPE, AFFILIATION, CLASSIFICATION, USE_CASE, ORGANIZATION, INCOME_AMT, SPECIAL_CONSIDERATIONS, and ASK_AMT. After binning APPLICATION_TYPE and CLASSIFICATION, I binned ASK_AMOUNT as it had a significant amount of unique values in the column.
- The variables that are neither target nor features and were removed from the input data are EIN and NAME.
### Compiling, Training, and Evaluating the Model
- I started by adding one more hidden layer (total of 3) with nodes of 100, 80, and 30 respectively. All three hidden layers had the activation fuction of relu. The outer layer had the activation function sigmoid.
- No, I was not able to achieve the target model performance of 75% accuracy. 
- I tried adding another hidden layer (total of 4) with nodes of 100, 80, 60, and 40 respectively. All four hidden layers had the activation function of relu. Again, the outer layer had the activation function sigmoid. However, the accuracy still did not hit 75%. Therefore, I tried another attempt with the three hidden layers I started with. I instead used the activation function tanh. However, the accuracy again did not hit 75%. 
## Summary
I was not able to achieve the target model performance of 75% accuracy. After binning ASK_AMT and then increasing the model's performance, the model performance still did not improve enough. I would recommend doing the Random Forest Classifier. The Random Forest Classifier is robust against data that is nonlinear and overfitting. It builds small trees and together can generate a strong learner. This could help sole the classification problem we are having using the deep learning model.
