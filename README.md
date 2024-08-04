# PROVIDING DATA DRIVEN SUGGESTION FOR HR 

## 📦 Project Structure

The repository is organized into the following directories:

- **/data**: This directory contains the dataset.
- 

## 🎯 Purpose
The goal in this project are to analyze the data collected by the HR department and to build a model that predicts whether or not an employee will leave the company.

If I can predict employees likely to quit, it might be possible to identify factors that contribute to their leaving. Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will be beneficial to the company.
## 🗂️ Dataset
The dataset was taken from Kaggle. To see the dataset visit [this](https://www.kaggle.com/datasets/mfaisalqureshi/hr-analytics-and-job-prediction?select=HR_comma_sep.csv)  or you can find csv file in data folder.

There are 14,999 rows, 10 columns, and these variables:
- **satisfaction_level**: Employee-reported job satisfaction level [0–1]
- **last_evaluation**: Score of employee's last performance review [0–1]
- **number_project**: Number of projects employee contributes to
- **average_monthly_hours**: Average number of hours employee worked per month
- **time_spend_company**: How long the employee has been with the company (years)
- **Work_accident**: Whether or not the employee experienced an accident while at work
- **left**: Whether or not the employee left the company
- **promotion_last_5years**: Whether or not the employee was promoted in the last 5 years
- **Department** The employee's department
- **salary**: The employee's salary (U.S. dollars)
## 🛠️ Methodology
![image](https://github.com/user-attachments/assets/80e240fb-354e-4d10-9fbc-9826d01395d6)
   ### 🤔 Plan 
   - **Understand the business scenario and problem:**
The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. They collected data from employees, but now they don’t know what to do with it. They refer to you as a data analytics professional and ask you to provide data-driven suggestions based on your understanding of the data. They have the following question: what’s likely to make the employee leave the company?
    - **Familiarize with the HR dataset**
    - **Gather basic information and descriptive statistics about the data**
    - 

Your goals in this project are to analyze the data collected by the HR department and to build a model that predicts whether or not an employee will leave the company.

If you can predict employees likely to quit, it might be possible to identify factors that contribute to their leaving. Because it is time-consuming and expensive to find, interview, and hire new employees, increasing employee retention will be beneficial to the company.
## ✅ The result
   ### 🔍 Insight
It appears that employees are leaving the company as a result of poor management. Leaving is tied to longer working hours, many projects, and generally lower satisfaction levels. It can be ungratifying to work long hours and not receive promotions or good evaluation scores. There's a sizeable group of employees at this company who are probably burned out. It also appears that if an employee has spent more than six years at the company, they tend not to leave

   ### 🤖 Modeling
   |No.| Model | Precision | Recall | F1-Score | Accuracy | AUC-ROC |  
   | -----| ----------- | ----------- | ---------- | ------- | ------- | ------- |
   |1|Logistic Regression|0.794|0.822|0.803|0.821|0.603|
   |2|Support Vector Machine (SVM)|0.966|0.966|0.966|0.966|0.939|
   |3|Multi-layer Perceptron (MLP)|0.948|0.949|0.949|0.949|0.905|
   |4|Decision Tree|0.981|0.982|0.982|0.982|0.961|
   |5|Random Forest|0.985|0.985|0.985|0.985|0.963|
   |6|Gradient Boosting Classifier (XGB)|0.986|0.986|0.986|0.986|0.966|
