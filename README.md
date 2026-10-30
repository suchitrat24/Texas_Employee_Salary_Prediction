# Texas State Employee Salary Prediction

## Project Overview

This project focuses on analyzing and predicting annual salaries of employees working across Texas state government agencies using data science and machine learning techniques.

The project was completed as part of the **DataMites AI Engineer Program (Internship Project)**.

The primary objective was to perform exploratory data analysis, identify salary patterns and disparities, and develop a predictive machine learning model to estimate employee salaries based on employment-related features.

## Project Objectives

- Perform data cleaning and exploratory data analysis (EDA).
- Identify salary outliers using statistical techniques.
- Analyze salary differences between managers and non-manager employees.
- Examine workforce demographics, employee tenure, and salary patterns across hiring periods.
- Build and compare multiple regression models to predict annual employee salaries.
- Evaluate model performance and identify the best-performing algorithm.

## Dataset

The dataset contains salary information for employees across **113 Texas state government agencies**.

The dataset includes information such as:
- Agency and agency name
- Job classification and job title
- Gender and ethnicity
- Employment status
- Employment date
- Hours worked per week
- Monthly and annual salary

*Note: The analysis uses a 2020 dataset snapshot.*

## Technologies & Libraries

- Python
- Jupyter Notebook
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

## Project Workflow

### 1. Data Cleaning and Preprocessing
- Examined dataset structure, missing values, duplicates, and data types.
- Removed unnecessary columns, personal identifiers, and redundant features.
- Handled missing and inconsistent values.
- Converted employment dates into hire years and employee tenure.
- Created additional features, including full-time employment status and manager classification.

### 2. Exploratory Data Analysis (EDA)
- Analyzed annual salary distributions.
- Examined relationships between salary, employee tenure, and working hours.
- Compared salary distributions across agencies.
- Investigated salary differences across gender and ethnicity.
- Used histograms, boxplots, scatterplots, bar charts, and correlation heatmaps.

### 3. Salary Outlier Analysis
Used the Interquartile Range (IQR) method to identify unusually high and low salaries.

Key findings:
- Approximately 9,018 employees were classified as high salary outliers.
- High salary outliers accounted for approximately 14.6% of total payroll.
- Many outliers represented senior leadership, judges, and specialized investment positions rather than data errors.

### 4. Manager vs. Employee Salary Analysis
Compared median salaries between managers and non-manager employees across Texas government agencies.

Key findings:
- Median full-time manager salary: approximately $69,700.
- Median full-time non-manager salary: approximately $44,500.
- The largest salary ratios appeared in agencies such as the Secretary of State, Teacher Retirement System, and Department of Banking.

### 5. Workforce and Salary Trends
Analyzed employee hiring cohorts to investigate differences in workforce size, median salary, and total payroll.

Key findings:
- Approximately 56.4% of employees were hired between 2016 and 2020.
- These employees accounted for approximately 50% of total payroll.
- Salary patterns varied considerably across job classifications and agencies.

*Because the dataset represents a single year, these comparisons reflect differences between employee hiring cohorts rather than directly observed year-to-year changes in salaries.*

### 6. Machine Learning Model Development

This project uses supervised machine learning regression to predict annual employee salaries.

The following algorithms were implemented and evaluated:

1. Linear Regression
2. Decision Tree Regressor
3. K-Nearest Neighbors (KNN) Regressor
4. Random Forest Regressor
5. Gradient Boosting Regressor

**Selected Features:**
- Job Title
- Agency Name
- Manager Status
- Employee Tenure
- Hours Per Week
- Full-Time Status
- Gender
- Ethnicity

### 7. Model Evaluation and Comparison

Models were evaluated using:
- R² Score
- Mean Absolute Error (MAE)
- Root Mean Squared Error (RMSE)

| Model | Test R² | Test MAE | Test RMSE |
|---|---:|---:|---:|
| Random Forest | **0.912** | **$3,099** | **$7,527** |
| Decision Tree | 0.877 | $3,483 | $8,888 |
| KNN | 0.865 | $3,713 | $9,325 |
| Gradient Boosting | 0.628 | $9,037 | $15,457 |
| Linear Regression | 0.229 | $14,411 | $22,258 |

**Best Performing Model: Random Forest Regressor**

The Random Forest model achieved the highest test R² score and the lowest prediction errors among the five evaluated models.

The results suggest that Random Forest effectively captures nonlinear relationships between employee characteristics and annual salaries.

## Key Findings

- Job title was the most influential feature in predicting annual salary.
- Agency and employee tenure were also important predictors.
- Salary distributions were right-skewed, with a relatively small number of high-earning employees.
- Manager-to-employee salary differences varied significantly across agencies.
- Salary patterns differed across employee hiring cohorts.

## Challenges and Solutions

Some of the main challenges encountered included:

- **Missing data:** Removed columns with extremely high percentages of missing values.
- **Data quality:** Standardized inconsistent text values and corrected employment dates.
- **Data leakage:** Removed monthly salary because it was directly calculated from annual salary.
- **Feature redundancy:** Removed features containing duplicate information.
- **Categorical variables:** Used Label Encoding to convert categorical features into numerical representations.
- **Model selection:** Compared multiple regression algorithms using consistent evaluation metrics.


## Disclaimer

This project was completed for educational and portfolio purposes as part of the DataMites AI Engineer Program. The model results are based on the available 2020 dataset and should not be interpreted as a validated production payroll system.

The dataset contains public-sector salary information. Raw employee records and personal identifiers are not included in this repository.

## Author

**Suchitra Thanumalayan**

Data Science | Machine Learning | Artificial Intelligence
