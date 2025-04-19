# Churn Prediction Project
## Overview
Customer churn is one of the most critical metrics in subscription-based businesses, especially in the telecommunications sector. This project aims to analyze patterns that lead to customer churn and build a machine learning model to predict the likelihood of churn based on customer attributes and service usage history.
The analysis dives deep into customer behavior, contract types, and service interactions to uncover actionable insights that can support business decision-making, improve customer retention, and guide targeted interventions.

## Objectives
- Analyze and visualize customer churn patterns.
- Understand the relationship between customer features (e.g., contract type, services used) and churn.
- Build and evaluate a predictive model that can classify customers as likely to churn or not.
- Identify high-impact features that influence churn behavior.
- Explore the limitations of the dataset and how they affect temporal storytelling.

## Dataset
The dataset used is the Telco Customer Churn dataset, which includes demographic, account, and service-related information for over 7,000 customers.
Each row represents a unique customer, along with attributes describing their demographics, services subscribed to, contract and billing information, and churn status.

### Features:
* Demographics: gender, SeniorCitizen, Partner, Dependents
* Customer Tenure & Contract: tenure, Contract, PaperlessBilling, PaymentMethod
* Services: PhoneService, MultipleLines, InternetService, OnlineSecurity, OnlineBackup, StreamingTV, StreamingMovies
* Charges: MonthlyCharges, TotalCharges
* Target Variable: Churn – whether the customer left the company (Yes/No)

## Results
### Preprocessing:
- Missing values in TotalCharges were imputed or removed.
- Categorical features were encoded.
- Tenure was binned into segments for clarity on visualization.

## Exploratory Analysis:
- Month-to-month contracts showed the highest churn rates.
- Customers with streaming services and fiber-optic internet churned more.
- Churn was most prominent among customers with tenures below 12 months.

## Modeling:
Multiple classification models were tested. The best-performing model was the Random Forest Classifier.

### Evaluation metrics: 
Accuracy: ~79%
Precision & Recall: Balanced, with an emphasis on recall for identifying churners.

## Key Findings

* Contract Type Matters:
Customers on month-to-month contracts are far more likely to churn. Unexpectedly, some customers on 2-year contracts begin churning earlier than month-to-month users, suggesting unmet long-term expectations.
* Streaming & Internet Services Contribute to Churn
Around 290 churned customers were subscribed to both StreamingMovies and InternetService, indicating possible dissatisfaction with bundled service quality.
* Tenure is Not a Timeline Substitute
Although tenure helps segment users by duration, it fails to provide chronological insights like seasonal churn trends or campaign effects due to the absence of actual dates.

** First-Year Drop-Off is High **
A majority of churn happens within the first 12 months, highlighting issues with onboarding, user experience, or expectation-setting.

## Conclusion
This project successfully demonstrates how customer churn can be predicted using machine learning techniques. 
Strong signals from features like contract type and tenure help flag at-risk customers early on.
