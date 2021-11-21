# Predicting-Employee-Attrition

##### Public Leaderboard : 4
##### Private Leaderboard: 3

## Problem Statement: 
Given the monthly information for a segment of employees for 2016 and 2017 and need to predict whether a current employee will be leaving the organization in the upcoming two quarters (01 Jan 2018 - 01 July 2018) or not.
## Approach: 
Train data contains the monthly information of employees for 2016 and 2017, as the data is about employee attrition the test data consist of employee id of employees who have not left the company in 2017. 
Need to predict whether the employee is going to resign in the next 2 quarters of 2018(6 months), so created an indicator variable wherever the last designation date is present or not (1,0) and then have taken the lead (6) of the indicator variable and then filled with the same value for the remaining records of the variable. Basically, the employee’s indicator variable will continue to be 1 if the employee has resigned 6 months later as per given data. There were one more thing to be taken care of, the employees whose record is <=6. Here either the employee has resigned within 6 months or employee who has joined after July 2017. For the first case indicator variable is 1, and for latter 0. This Indicator variable is considered as the target variable.
Using the data after Jul 2017 for Test, predicted the target values and the value predicted for December 2017 considered as the final output.
## Data Pre-processing/Feature Engineering: 
City, Gender, Report month have been encoded, For Total Business value, created a variable which tells how many times the employee provided value for company, and from Salary created variable saying whether there was a salary increase at some point of time. Education level has also been mapped to 1,2,3 and created Exp- how long the employee has been working with the firm.
## Model: 
Started from Decision tree, and there was a strong linear relation ship between variables has been detected. Tried Random Forest and logistic regression later with hyperparameter tuning.
The best fit comes out to be Logistic Regression with an F1 score of 0.74.
