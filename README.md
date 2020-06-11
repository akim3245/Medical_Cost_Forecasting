# Medical Cost Forecasting

## Project Objective
To predict the medical charges based on patient information using Linear Regression.

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

The dataset includes the following features: 
* Age
* Sex
* BMI
* Smoker/Non-smoker
* Number of Children
* Region

With increase in age there was an increase in charges and charges are higher among smokers compared to non-smokers.
[![Screen-Shot-2020-06-09-at-10-00-12-AM.png](https://i.postimg.cc/PJ79Bz7m/Screen-Shot-2020-06-09-at-10-00-12-AM.png)](https://postimg.cc/4HzWctsd)

The higher the BMI, the higher the charges which also appears to rise more quicker in smokers.
[![Screen-Shot-2020-06-09-at-10-00-18-AM.png](https://i.postimg.cc/MZ3CMqGv/Screen-Shot-2020-06-09-at-10-00-18-AM.png)](https://postimg.cc/hhxyNFTB)

## Feature Engineering
Two new columns were created. 

The first column, 'bmi_cat', organizes BMI into categories: underweight, normal, overweight and obese.
The second column, 'age_cat', categorizes age into age groups: child, youth, middle aged and senior. Children and seniors were not identified in the dataset. The youngest was 18 years old (youth) and the oldest was 64 years old (middle aged).

After exploring and preprocessing, the data was split 80/20 into train and test sets. 

The machine learning algorithms used:
* Multiple Linear Regression
* Polynomial Regression
* Lasso Regression

After training and predicting the target variable using Multiple Linear Regression, I plotted the predicted against the true charges to visually see a side-by-side comparison of how well the model performed.
[![Screen-Shot-2020-06-11-at-12-49-15-AM.png](https://i.postimg.cc/NftfKwGq/Screen-Shot-2020-06-11-at-12-49-15-AM.png)](https://postimg.cc/z3d1Q6R0)

The R2 score for Multiple Linear Regression turned out to be 0.74 which is okay, but it could definitely be better.

Normalizing the data slightly improved the model and gave an R2 score of 0.76. 
[![Screen-Shot-2020-06-11-at-1-23-16-AM.png](https://i.postimg.cc/Y0CGZ4n7/Screen-Shot-2020-06-11-at-1-23-16-AM.png)](https://postimg.cc/wynjsBY4)
[![Screen-Shot-2020-06-11-at-1-23-24-AM.png](https://i.postimg.cc/QCY93XwT/Screen-Shot-2020-06-11-at-1-23-24-AM.png)](https://postimg.cc/5QvN5Mx4)

Next was Polynomial Regression. I ran a few tests using different degrees but degree of 2 gave the best R2 score of 0.83. 

Lasso Regression with the best alpha param gave an R2 score of 0.74. 

Lastly, I ran backward elimination to filter out features greater than significance level 0.05 which ultimately gave an R2 score of 0.80. 

## Model Evaluation
Here is a summary to show the models used as well as the scores and RMSE that each produced. 
[![Screen-Shot-2020-06-11-at-12-42-58-AM.png](https://i.postimg.cc/8k9zNr95/Screen-Shot-2020-06-11-at-12-42-58-AM.png)](https://postimg.cc/3WjTZWK5)

As you can see, looking at the R2 Test scores, Polynomial Regression performed with the highest score followed by Linear Regression using features selected by backward elimination. 

## Model Comparison
Here is a bar chart to visually compare model performance by R2 test scores. 
[![Screen-Shot-2020-06-11-at-12-31-13-AM.png](https://i.postimg.cc/yNvGBcfr/Screen-Shot-2020-06-11-at-12-31-13-AM.png)](https://postimg.cc/t1nkNZGh)

Although Polynomial Regression performed the best, the scores are very similar and all fall within a short range between 0.7 and 0.85.

## Notebooks
* MedicalCost_Dev_eda -- Exploratory data analysis, data visualizations, cleaning, preprocessing
* MedicalCost_Dev_modelling -- Model performance (Multiple linear regression, polynomical regression, lasso regression, backward elimination), model validation, model comparison
