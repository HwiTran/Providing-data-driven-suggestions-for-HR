# PROVIDING DATA DRIVEN SUGGESTION FOR HR 

## 📦 Project Structure

The repository is organized into the following directories:

- **/data**: This directory contains the dataset.
- **/EDA**: This directory contains the Jupyter notebook ```EDA.ipynb```. This notebook guides you through exploratory data analysis (EDA) and predict tasks.

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
   ### 🤔 Plan Stage
   - **Understand the business scenario and problem:**:
The HR department at Salifort Motors wants to take some initiatives to improve employee satisfaction levels at the company. They collected data from employees, but now they don’t know what to do with it. They refer to you as a data analytics professional and ask you to provide data-driven suggestions based on your understanding of the data. They have the following question: what’s likely to make the employee leave the company?

   - **Familiarize with the HR dataset**
   - **Gather basic information and descriptive statistics about the data**
   - **Preprocessing data**

   ### 📈 Analyze Stage
   - **Data visualization**:
Analyze relationships between variables to understand how many employees left and why.

   ### 🚧 Construct Stage
   - **Determine which models are most appropriate**
   - **Model building**


|No.| Model | Precision | Recall | F1-Score | Accuracy | AUC-ROC |  
   | -----| ----------- | ----------- | ---------- | ------- | ------- | ------- |
   |1|Logistic Regression|0.794|0.822|0.803|0.821|0.603|
   |2|Support Vector Machine (SVM)|0.966|0.966|0.966|0.966|0.939|
   |3|Multi-layer Perceptron (MLP)|0.948|0.949|0.949|0.949|0.905|
   |4|Decision Tree|0.981|0.982|0.982|0.982|0.961|
   |5|Random Forest|0.985|0.985|0.985|0.985|0.963|
   |6|Gradient Boosting Classifier (XGB)|0.986|0.986|0.986|0.986|0.966|

   
   - **Confirm model assumptions**
   - **Evaluate model results to determine how well model fits the data**

   ### ✅ Execute Stage 
   - **Interpret model performance and results**
   - **Share actionable steps with stakeholders**
## 🎯 The result
   ### 🔍 Insight
It appears that employees are leaving the company as a result of poor management. Leaving is tied to longer working hours, many projects, and generally lower satisfaction levels. It can be ungratifying to work long hours and not receive promotions or good evaluation scores. There's a sizeable group of employees at this company who are probably burned out. It also appears that if an employee has spent more than six years at the company, they tend not to leave.

   ### 🤖 Best model
   |Model | Precision | Recall | F1-Score | Accuracy | AUC-ROC |  
   | -----| ------ | ---------- | ------- | ------- | ------- |
   |Gradient Boosting Classifier (XGB)|0.986|0.986|0.986|0.986|0.966|

   ![image](https://github.com/user-attachments/assets/cbe4374e-ef79-4b4c-89da-e35bbfafede7)
   
The Gradient Boosting Classifier predicts more false positives than false negatives, which means that some employees may be identified as at risk of quitting or getting fired, when that's actually not the case. This model outperforms all other models in predicting the False Positive score (30), minimizing prediction risk. So this is still a strong model.

All tree-based models consistently highlight features `tenure`,`satisfaction_level`, `number_project`,  and `last_evaluation` as key factors influencing an employee's decision to leave their job

   ### ✨ Conclusion, Recommendations, Next Steps

The models and the feature importances extracted from the models confirm that employees at the company are **overworked**. 

To retain employees, the following recommendations could be presented to the stakeholders:

* Cap the number of projects that employees can work on.
* Consider promoting employees who have been with the company for atleast four years, or conduct further investigation about why four-year tenured employees are so dissatisfied. 
* Either reward employees for working longer hours, or don't require them to do so. 
* If employees aren't familiar with the company's overtime pay policies, inform them about this. If the expectations around workload and time off aren't explicit, make them clear. 
* Hold company-wide and within-team discussions to understand and address the company work culture, across the board and in specific contexts. 
* High evaluation scores should not be reserved for employees who work 200+ hours per month. Consider a proportionate scale for rewarding employees who contribute more/put in more effort. 

**Next Steps**

It may be justified to still have some concern about data leakage. It could be prudent to consider how predictions change when `last_evaluation` is removed from the data. It's possible that evaluations aren't performed very frequently, in which case it would be useful to be able to predict employee retention without this feature. It's also possible that the evaluation score determines whether an employee leaves or stays, in which case it could be useful to pivot and try to predict performance score. The same could be said for satisfaction score. 

For another project, you could try building a K-means model on this data and analyzing the clusters. This may yield valuable insight. 

