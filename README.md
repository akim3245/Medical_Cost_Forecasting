# Medical Cost Forecasting
#### -- Project Status: [Active]

## Project Intro/Objective
The purpose of this project is to predict the medical charges based on patient information using Multiple Linear Regression.

### Methods & Technologies Used
* Machine Learning
* Data Visualization
* Predictive Modeling
* Jupyter Notebook
* Python
* Pandas, Numpy
* etc. 

## Project Description
Data was thoroughly analyzed to find patterns and correlations with the target variable being the charges. 

With increase in age there was an increase in charges. Charges are higher among smokers compared to non-smokers.
[![Screen-Shot-2020-06-09-at-10-00-12-AM.png](https://i.postimg.cc/PJ79Bz7m/Screen-Shot-2020-06-09-at-10-00-12-AM.png)](https://postimg.cc/4HzWctsd)

The higher the BMI, the higher the charges which also appear to rise more quickly in smokers.
[![Screen-Shot-2020-06-09-at-10-00-18-AM.png](https://i.postimg.cc/MZ3CMqGv/Screen-Shot-2020-06-09-at-10-00-18-AM.png)](https://postimg.cc/hhxyNFTB)

Overall, most patients in this dataset are non-smokers and most are overweight or obese.
[![Screen-Shot-2020-06-09-at-10-06-36-AM.png](https://i.postimg.cc/BbbRYwmS/Screen-Shot-2020-06-09-at-10-06-36-AM.png)](https://postimg.cc/N2hNLbhS)

After exploring and preprocessing, the data was split into training and testing sets 80/20. 

The machine learning algorithms used:
* Multiple Linear Regression
* Polynomial Regression
* Lasso Regression

### Model Evaluation

#### Multiple Linear Regression
[![Screen-Shot-2020-06-09-at-10-54-37-AM.png](https://i.postimg.cc/JzJpPW57/Screen-Shot-2020-06-09-at-10-54-37-AM.png)](https://postimg.cc/w1q5jZrn)
[![Screen-Shot-2020-06-09-at-10-56-03-AM.png](https://i.postimg.cc/yxZ9LH3X/Screen-Shot-2020-06-09-at-10-56-03-AM.png)](https://postimg.cc/wR97BnV7)

#### Polynomial Regression
[![Screen-Shot-2020-06-09-at-10-56-46-AM.png](https://i.postimg.cc/Y25QhhTX/Screen-Shot-2020-06-09-at-10-56-46-AM.png)](https://postimg.cc/PNMC7rXZ)

#### Lasso Regression
[![Screen-Shot-2020-06-09-at-10-57-04-AM.png](https://i.postimg.cc/sfQpjpHQ/Screen-Shot-2020-06-09-at-10-57-04-AM.png)](https://postimg.cc/NLtybrcB)

### Backward Elimination
Features with p val greater than 0.05 significance level were removed to improve model performance. Once backward elimination was done, the kept features were scaled and trained to produce the following result.

[![Screen-Shot-2020-06-09-at-11-10-20-AM.png](https://i.postimg.cc/kgx0kRPL/Screen-Shot-2020-06-09-at-11-10-20-AM.png)](https://postimg.cc/3kxfGRRZ)

## Model Comparison
Here is a barplot of the different algorithms used to compare the cross-validation r2 scores.
[![Screen-Shot-2020-06-09-at-11-12-55-AM.png](https://i.postimg.cc/1txJPJ0H/Screen-Shot-2020-06-09-at-11-12-55-AM.png)](https://postimg.cc/1gHpr0jn)

Looking at the graph above, there isn't too big of a difference in r2 scores across algorithms used. Although Lasso regression has the best score, all models fall within the same score range between 0.7 and 0.8. 

## Notebooks
* MedicalCost_Dev_eda -- Exploratory data analysis, data visualizations, cleaning, preprocessing
* MedicalCost_Dev_modelling -- Model performance (Multiple linear regression, polynomical regression, lasso regression, backward elimination), model validation, model comparison
