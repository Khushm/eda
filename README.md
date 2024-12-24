# Exploratory Data Analysis for Diabetes Prediction

**CSE 5243 - Introduction to Data Mining - Fall 2024**

## Table of Contents
1. [Project Overview](#project-overview)
2. [Dataset Overview](#dataset-overview)
3. [Data Understanding and Exploratory Data Analysis (EDA)](#data-understanding-and-exploratory-data-analysis-eda)
4. [Data Preprocessing](#data-preprocessing)
5. [Logistic Regression Modeling](#logistic-regression-modeling)
6. [Visualizations](#visualizations)
7. [Results and Insights](#results-and-insights)
8. [Conclusions](#conclusions)
9. [Access the EDA Results](#access-the-eda-results)

## Project Overview
This project explores a modified version of the **Pima Indians Diabetes Database** to predict the likelihood of a patient having diabetes based on various health and demographic attributes. The goal is to apply techniques in data preprocessing, exploratory data analysis (EDA), and logistic regression modeling to analyze the dataset.

### Key Tasks:
- Perform an in-depth exploratory data analysis (EDA).
- Clean the data by handling missing values, duplicates, and outliers.
- Build and evaluate a logistic regression model to predict the probability of diabetes.
- Assess the model's performance with metrics such as misclassification tables and ROC curves.

## Dataset Overview
The dataset used in this analysis is based on the **Pima Indians Diabetes Database**, which contains medical data for female patients of Pima Indian heritage. The goal is to diagnose diabetes based on various health indicators such as glucose levels, blood pressure, and body mass index (BMI).

### Features:
- **Pregnancies**: Number of pregnancies
- **Glucose**: Plasma glucose concentration
- **Blood Pressure**: Diastolic blood pressure (mm Hg)
- **Skin Thickness**: Triceps skin fold thickness (mm)
- **Insulin**: 2-Hour serum insulin (mu U/ml)
- **BMI**: Body mass index (weight in kg / height in m^2)
- **Diabetes Pedigree Function**: A function that scores the likelihood of diabetes based on family history
- **Age**: Age of the patient in years
- **Outcome**: Binary outcome (1 for diabetes, 0 for no diabetes)

## Data Understanding and Exploratory Data Analysis (EDA)
### Key Steps:
- **Initial Review**: Understanding the structure of the data, identifying any missing or inconsistent values, and detecting possible correlations between attributes.
- **Feature Analysis**: Investigating the statistical characteristics of each feature such as the mean, median, and distribution.
- **Bivariate Analysis**: Exploring relationships between pairs of attributes and how they may relate to the target variable, `Outcome`.

#### Key Observations:
- The data contains both continuous (e.g., glucose, BMI) and categorical (e.g., outcome) attributes.
- We focus on identifying relationships between the features and the outcome to understand potential predictors for diabetes.

## Data Preprocessing
- **Outlier Handling**: Identified outliers were adjusted by replacing them with median values within specific outcome groups.
- **Missing Data Imputation**: Missing values were imputed based on the mean or median of the respective outcome groups to ensure the integrity of the data.
- **Duplicates**: Any duplicate records were removed to avoid biasing the model.

### Impact of Data Handling:
- Imputation and outlier adjustment helped stabilize the dataset and ensured a more accurate analysis. Without proper imputation and handling of outliers, the model could yield misleading conclusions.

## Logistic Regression Modeling
### Steps:
1. **Data Preparation**: Cleaned data is split into training and test sets for model training and evaluation.
2. **Modeling**: A logistic regression model was built using the cleaned dataset.
3. **Evaluation**: The model's performance was evaluated using metrics like misclassification tables at different cutoff values (0.5 and 0.75).
4. **Odds Ratios**: Interpreted the logistic regression coefficients to determine the significance of each feature.

### Results:
- **Misclassification Table**: The confusion matrix was computed for two different cutoff thresholds to analyze classification performance.
- **ROC Curve**: A Receiver Operating Characteristic (ROC) curve was plotted to visualize the model’s diagnostic ability.

## Visualizations
Key visualizations generated in the project include:

### Correlation Matrix
This matrix shows how the features correlate with each other, which can help identify which variables are more strongly related to one another and to the outcome.

![Correlation Matrix](./images/correlation_matrix.png)

### Histograms

![Histogram](./images/histogram.png)

Further, Violin Plot of key features like **Glucose**, **BMI**, and **Age** were created to visualize their distributions.

![Violin Plot](./images/volinplot.png)

### Box Plots
Box plots were used to detect outliers and analyze the distribution of variables like **Skin Thickness** and **Blood Pressure**.

![Box Plot](./images/boxplot.png)


### Interpretation:
Each visualization helps identify key patterns, correlations, and outliers, providing a clearer picture of how features relate to diabetes prediction.

## Results and Insights
- Logistic regression results show the odds ratios for various predictors, providing insights into which features significantly contribute to predicting diabetes.
- The imputation and handling of outliers impacted the model's performance, and the results emphasize the importance of clean data for accurate predictions.

### ROC Curve:
Visualizing the trade-off between sensitivity and specificity, allowing to assess the performance of the model at different decision thresholds.

![ROC Curve](./images/roc.png)

### Key Insights:
- Higher glucose levels and BMI are strong indicators of diabetes.
- The effect of family history (via Diabetes Pedigree Function) and age was also significant in determining the likelihood of diabetes.

## Conclusions
- The data reveals significant relationships between certain medical and demographic features and the likelihood of diabetes.
- Handling outliers and missing values had a notable impact on the model's predictions, underlining the importance of thorough data cleaning.
- Future research could explore the inclusion of more diverse datasets or additional health factors to improve model accuracy.

## Access the EDA Results
You can view the detailed Exploratory Data Analysis (EDA) and the logistic regression model results on the project website:

[**View the EDA Results Here**](https://khushm.github.io/eda/)

