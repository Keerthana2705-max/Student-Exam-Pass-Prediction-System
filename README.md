# STUDENT EXAM PASS PREDICTION SYSTEM USING LOGISTIC REGRESSION

## ABSTRACT

Educational institutions generate large amounts of student-related data, including study hours, attendance rates, previous exam scores, parental education levels, internet access, and extracurricular participation. Analyzing this data manually to identify students who are at risk of failing examinations is time-consuming and often ineffective.

This project aims to develop a Student Exam Pass Prediction System using Logistic Regression. The system performs Exploratory Data Analysis (EDA), identifies important factors influencing academic performance, classifies students based on risk levels, and predicts whether a student is likely to pass or fail. The project also includes data visualization and dashboard development to support data-driven decision-making by educational institutions.

Keywords: Logistic Regression, Student Performance Prediction, Machine Learning, Data Analysis, Dashboard Visualization, Academic Performance.

---

# 1: INTRODUCTION

## 1.1 Background

Student academic performance is influenced by multiple factors such as attendance, study habits, previous academic records, parental education, internet accessibility, and participation in extracurricular activities.

Educational institutions require an efficient system to identify students who may face academic difficulties. Early prediction allows teachers and administrators to provide appropriate support and intervention strategies.

Machine Learning techniques, especially Logistic Regression, can be used to predict whether a student will pass or fail based on historical and demographic information.

---

## 1.2 Problem Statement

Manual identification of students at risk of failing examinations is difficult and inefficient. Institutions need an automated system capable of analyzing student performance data and predicting examination outcomes accurately.

Failure to identify at-risk students may result in:

* Increased failure rates
* Poor academic performance
* Delayed academic intervention
* Reduced student confidence
* Lower institutional success rates

---

## 1.3 Objectives

The objectives of this project are:

* Perform Exploratory Data Analysis (EDA)
* Analyze factors affecting student performance
* Classify students into risk categories
* Build a Logistic Regression model
* Predict pass/fail outcomes
* Evaluate model performance
* Develop an interactive dashboard for visualization

---

# 2: DATASET DESCRIPTION

## Dataset Source

Kaggle

Dataset Name:
Student Performance Prediction Dataset

## Dataset Features

| Column Name                | Description                 |
| -------------------------- | --------------------------- |
| Student_ID                 | Unique Student Identifier   |
| Gender                     | Male/Female                 |
| Study_Hours_per_Week       | Weekly Study Hours          |
| Attendance_Rate            | Attendance Percentage       |
| Past_Exam_Scores           | Previous Exam Average       |
| Parental_Education_Level   | Parents' Education Level    |
| Internet_Access_at_Home    | Internet Availability       |
| Extracurricular_Activities | Participation in Activities |
| Final_Exam_Score           | Final Examination Score     |
| Pass_Fail                  | Target Variable             |

---

# 3: METHODOLOGY

## Step 1: Data Collection

The dataset is collected from Kaggle and loaded using the Pandas library.

Functions Used:

* pd.read_csv()
* head()
* info()
* shape()

---

## Step 2: Data Cleaning

Data cleaning ensures data quality before model training.

Activities performed:

* Missing value detection
* Missing value removal
* Duplicate removal
* Data type verification
* Feature selection

Functions Used:

* isnull()
* dropna()
* drop_duplicates()

---

## Step 3: Data Preprocessing

Categorical variables are converted into numerical values using Label Encoding.

Encoded Features:

* Gender
* Parental Education Level
* Internet Access
* Extracurricular Activities
* Pass/Fail

Student_ID is removed because it does not contribute to prediction.

---

## Step 4: Feature Scaling

Numerical features are standardized using StandardScaler.

Benefits:

* Improves model performance
* Ensures equal contribution of features
* Reduces bias caused by varying scales

---

# 4: EXPLORATORY DATA ANALYSIS

## Descriptive Statistics

The following metrics are calculated:

* Average Study Hours
* Average Attendance Rate
* Average Past Exam Score
* Average Final Exam Score
* Pass vs Fail Count
* Gender Distribution

---

## Student Performance Analysis

Comparison between pass and fail students based on:

* Study Hours
* Attendance Rate
* Past Scores
* Internet Access
* Extracurricular Activities

---

## Group-Based Analysis

The following relationships are analyzed:

* Study Hours vs Pass/Fail
* Attendance vs Pass/Fail
* Past Scores vs Pass/Fail
* Gender vs Pass Rate
* Internet Access vs Pass Rate
* Parental Education vs Student Performance
* Extracurricular Activities vs Pass Rate

---

# 5: DATA VISUALIZATION

The project uses Matplotlib and Seaborn for visualization.

## Bar Charts

* Pass vs Fail Distribution
* <img width="675" height="490" alt="image" src="https://github.com/user-attachments/assets/da452cde-3027-444e-b776-2cdf8eddb1c4" />

* Gender Distribution
* <img width="662" height="487" alt="image" src="https://github.com/user-attachments/assets/6f47538d-e406-469b-a3e8-ea0b3f84e288" />

## Histograms

* Study Hours Distribution
* <img width="666" height="490" alt="image" src="https://github.com/user-attachments/assets/43d1ca82-56c4-4bb0-8d78-95aed8246d15" />

* Attendance Distribution
* <img width="677" height="552" alt="image" src="https://github.com/user-attachments/assets/a4e3efcd-12fa-4c24-a624-4dc1fc9f14ea" />

* Final Exam Score Distribution
* <img width="661" height="492" alt="image" src="https://github.com/user-attachments/assets/0f89710b-51dc-4343-a181-c1b66d429e79" />


## Scatter Plots

* Study Hours vs Final Score
* Attendance vs Final Score

## Box Plots

* Final Score Outlier Detection
* Attendance Comparison

## Heatmap

Correlation analysis among numerical variables.
<img width="1295" height="697" alt="image" src="https://github.com/user-attachments/assets/67d652b4-7909-40dd-8357-470e6d478e14" />


---

# 6: RISK ANALYSIS

Students are classified into three categories.

## High Risk

Conditions:

* Attendance < 65%
* Study Hours < 10
* Past Score < 50

## Medium Risk

Conditions:

* Attendance < 80%
* Past Score < 70

## Low Risk

Conditions:

* Good attendance
* Sufficient study hours
* Strong academic performance

Purpose:

* Early intervention
* Academic support
* Improved student outcomes

---

# 7: LOGISTIC REGRESSION MODEL

## Independent Variables

* Gender
* Study Hours per Week
* Attendance Rate
* Past Exam Scores
* Parental Education Level
* Internet Access at Home
* Extracurricular Activities
* Final Exam Score

## Dependent Variable

Pass_Fail

---

## Model Training

Steps:

1. Data Splitting
2. Feature Scaling
3. Logistic Regression Training
4. Prediction
5. Probability Calculation

Functions Used:

* train_test_split()
* LogisticRegression()
* fit()
* predict()
* predict_proba()

---

# 8: MODEL EVALUATION

The model is evaluated using:

## Accuracy

Measures overall prediction correctness.

## Precision

Measures correctness of positive predictions.

## Recall

Measures ability to identify actual positive cases.

## F1 Score

Balances Precision and Recall.

## Confusion Matrix
<img width="622" height="491" alt="image" src="https://github.com/user-attachments/assets/6f06df50-d40f-4cd2-bcb7-a800fbbbcef4" />


Displays:

* True Positives
* True Negatives
* False Positives
* False Negatives

## ROC-AUC Score

Measures classification quality and separability.

---

# 9: DASHBOARD DEVELOPMENT

Tool Used:

Streamlit

## Dashboard Components

* Dataset Overview
* Pass vs Fail Distribution
* Study Hours Analysis
* Attendance Analysis
* Correlation Heatmap
* Performance Insights

## Interactive Features

* Dynamic Charts
* KPI Metrics
* Performance Filters
* Real-Time Visualization

---

# 10: RESULTS

The Logistic Regression model successfully predicts whether a student is likely to pass or fail.

Key findings:

* Attendance significantly influences academic performance.
* Students with higher study hours generally score better.
* Previous exam scores strongly impact final outcomes.
* Internet access positively contributes to performance.
* Risk categorization helps identify students requiring support.

---

# 11: CONCLUSION

The Student Exam Pass Prediction System provides an efficient solution for predicting student performance using Logistic Regression. Through EDA, visualization, and machine learning, the system identifies important academic factors and helps institutions take proactive measures to improve student success.

The developed dashboard enables educators to monitor performance trends and make informed decisions for academic planning and intervention.
4. Streamlit Documentation
5. Logistic Regression Research Papers
