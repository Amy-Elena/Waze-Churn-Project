# Waze-Churn-Project
End-of-course Projects for the Google Advanced Data Analytics Professional Certificate.  

### Project Overview  
This repository contains the Waze User Churn Prediction Project, aimed at identifying and predicting user churn within the Waze app. For this project, churn refers to users who either uninstalled the app or stopped using it. The ultimate goal is to develop machine learning models that can predict user churn, providing insights for strategies that improve user retention and overall app growth.  

### Data  
This project's dataset was created for pedagogical purposes and does not represent Waze’s actual data. The story, all names, characters, and incidents portrayed in this project are fictitious. No identification with actual persons (living or deceased) is intended or should be inferred.  

![Waze Logo](waze_logo.png)

### About Waze  
Waze’s free navigation app makes it easier for drivers around the world to get to where they want to go. Waze’s community of map editors, beta testers, translators, partners, and users helps make each drive better and safer. Waze partners with cities, transportation authorities, broadcasters, businesses, and first responders to help as many people as possible travel more efficiently and safely.

### Project Milestones  
This project was developed in multiple milestones, each contributing to the overall goal of building a robust churn prediction model. Below are summaries of each milestone.  

### Milestone 1: Project Proposal  
The first phase involved drafting a project proposal. This document outlined the scope, objectives, and methodologies to be applied throughout the project, including data inspection, feature engineering, and model building. Tasks were aligned with the **PACE** (Plan, Analyze, Construct, Execute) framework.  

### Milestone 2: Preliminary Data Summary 
In this phase, the initial dataset was inspected, containing 12 unique variables and showing that 18% of users churned while 82% remained active. Key insights revealed that churned users drove significantly more kilometers and spent more time driving than retained users, but used the app on fewer days.

* Target Goal: Inspect user data to learn important relationships between variables.
* Key Findings:
  * Churned users drove 240% more per driving day compared to retained users.
  * Retained users were active on twice as many days in the last month as churned users.
Recommendations from this stage included conducting more detailed exploratory data analysis (EDA) and investigating high-activity "super-drivers."

### Milestone 3: Exploratory Data Analysis (EDA) 
Milestone 3 involved in-depth EDA, revealing churn rates, usage patterns, and engagement dynamics. We found that churn rates were higher among users who drove long distances, but lower for users who engaged frequently with the app.

* Key Insights:
  * 18% of users churned, with churn rates increasing for long-distance drivers.
  * Distribution of sessions and drives showed right-skewed data, indicating outliers.
  * Churn rate was highest for users who barely used the app in the last month.
Further investigations were recommended for outliers and discrepancies between sessions, driving days, and activity days.

### Milestone 4: Two-Sample Hypothesis Testing 
This milestone tested whether the device type (Android vs. iPhone) influenced user behavior. A two-sample t-test was conducted to compare the mean number of rides between device types.

* Key Findings:
  * iPhone users averaged slightly more drives than Android users (68 vs. 66).
  * The t-test results indicated no statistically significant difference in mean drives between device types.
The results recommended further t-tests on additional variables to explore other factors influencing user behavior.

### Milestone 5: Regression Modeling 
The next step involved building a binomial logistic regression model to predict whether users would churn based on their behavior.

* Key Findings:
  * The model had a recall of only 9%, indicating it struggled to accurately predict churn.
  * Activity days were the most important feature, with a negative correlation to churn.
  * Distance driven per day, despite its earlier significance, was one of the least important predictors.
Due to the model's low recall, we recommended gathering additional data and refining feature selection to improve the model’s accuracy.

### Milestone 6: Machine Learning Model Comparison 
The final milestone involved building and comparing two machine learning models: Random Forest and XGBoost. Both models were designed to improve upon the earlier logistic regression model.

* Key Insights:
  * XGBoost outperformed Random Forest, especially in recall (17%) while maintaining similar accuracy and precision.
  * Engineered features (e.g., km_per_hour, percent_sessions_in_last_month) were crucial, with six out of the top 10 most important features being engineered.
The ensemble models demonstrated more predictive power than logistic regression but also highlighted the need for additional data to improve future model iterations.

### Conclusion  
The Waze User Churn Project successfully demonstrated key insights about user behavior and app engagement that contribute to churn. However, the machine learning models built during this project indicate that additional data and more advanced feature engineering are necessary to achieve higher recall and predictive accuracy.

The Waze team recommends a second iteration of this project with additional user interaction data to better understand the drivers behind churn and ultimately reduce user attrition.



