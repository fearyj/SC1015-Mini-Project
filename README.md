# SC1015-Mini-Project
## About
This is the mini project for NTU-SC1015 (Introduction to Data Science and Artificial Intelligence).

Job attrition can be a significant challenge for companies, but it is not inevitable. By understanding the causes of job attrition and taking steps to prevent it, companies can create a more stable, productive, and successful workplace for their employees.

## Problem Formulation
Dataset: Kaggle 



## Data Preparation and Cleaning
In this section of the project, we prepped and cleaned the dataset to help us analyze our data better and also to help us use our data for the purposes of machine learning in the later sections.


We performed the following:
Initial Variables Dropping: 5 of the variables are removed. They contain either only 1 unique value or 1470 unique values.
Clustering Categorical Data: Grouping appropriate data into “High” and “Low”.
Encoding Categorical Variables: Using One-Hot Key approach, variables that are categorical in nature are split into numerical data.
Secondary Variables Dropping: 9 pairs of the variables are mutually exclusive to each other. 1 variable from each pair is removed.
Data Padding: Since there is a more number of “No” than “Yes” for the variable “Attrition”. Upsampling is done to match pad the number of “Yes”.
Prepping Variables: Data of some variables were normalized and inverted for easy computation of weightage of the variables.

## Exploratory Data Analysis
Univariate Analysis
Plotting all the variables against attrition by hvPlot to visualize the correlation between attrition “Yes” and “No”.

Insights of EDA
The workers with low JobLevel, MonthlyIncome, YearAtCompany, and TotalWorkingYears are more likely to quit their jobs.

BusinessTravel:
The workers who travel a lot are more likely to quit than other employees.
Department:
The workers in Research & Development are more likely to stay than the workers in other departments.
EducationField:
The workers with Human Resources and Technical Degrees are more likely to quit than employees from other fields of education.
Gender :
The Male are more likely to quit.
JobRole:
The workers in Laboratory Technician, Sales Representative, and Human Resources are more likely to quit the workers in other positions.
MaritalStatus:
The workers who have Single marital status are more likely to quit the Married, and Divorced.
OverTime:
The workers who work more hours are likely to quit then others.

## Data Process
Plot attrition on barplot to see the ratio of “Yes” and “No”
Check for unique values and its total count for all variables
Grouping similar values i.e. “High” and “Very High” as “High”for easy analysis  of categorical variables 
Calculating the moderated values based on the weighted variables gathered from XGBoost.

## Machine Learning
Decision Tree Classifier
Upsampling Decision Tree Classifier
Random Forest
XGBoost


## Insights and Conclusion
The Decision Tree was able to identify the important variables that causes employee attrition
XGBoost was able to provide the weightage and the significance of the variables
Creating an accurate model for companies to use requires both the Decision Tree Classifier and XGBoost, which are necessary to determine the important factors and their corresponding weightage.

## References

XGBoost - https://www.nvidia.com/en-us/glossary/data-science/xgboost/#:~:text=What%20is%20XGBoost%3F,%2C%20classification%2C%20and%20ranking%20problems. 


Random Forest - 
https://www.analyticsvidhya.com/blog/2021/06/understanding-random-forest/

One-Hot Encoding - 
https://stackoverflow.com/questions/55229301/one-hot-encoding-multiple-columns-in-sklearn-and-naming-columns

MinMaxScalar - https://www.geeksforgeeks.org/data-pre-processing-wit-sklearn-using-standard-and-minmax-scaler/ 

Normalization -
https://www.digitalocean.com/community/tutorials/normalize-data-in-python 


Weighted Scale - 
https://towardsdatascience.com/ranking-algorithms-know-your-multi-criteria-decision-solving-techniques-20949198f23e
