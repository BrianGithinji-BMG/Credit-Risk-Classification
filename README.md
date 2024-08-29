# Credit-Risk-Classification
![01c5314b726c20a242ea86ffe689d1a9](https://github.com/user-attachments/assets/9be8c86d-0ffe-4b91-93e6-a60bb31c74cc)![24dd66eae8b4476ad541b45696e6578d](https://github.com/user-attachments/assets/e158c638-53f3-4221-88b3-1e0b32da0f2b)


## Overview.
This repository contains a project that aims to develop a machine learning model that predicts whether a loan applicant is likely to default on their loan. By accurately classifying applicants into high-risk and low-risk categories, financial institutions can make more informed lending decisions, ultimately reducing the risk of loan defaults.
## Business Problem.
Loan defaults can lead to significant financial losses for lending institutions. The goal of this project is to build a predictive model that can classify loan applicants based on their likelihood of defaulting on a loan, using a dataset of applicant information and loan details.

## Objectives
### Main Objective
1. To build a predictive model that accurately classifies loan applicants into high-risk and low-risk categories.
### Specific Objectives
1. To identify and understand key features that influence loan default. i.e:

- Analyze the impact of age on loan default rates.
- Determine the income brackets most likely to default on loans.
- Investigate the effect of employment length on loan default.
- Identify the loan amounts that are most frequently defaulted.
- Assess how interest rates influence loan default likelihood.
- Evaluate the relationship between credit history length and loan default.
- Explore the influence of home ownership status on loan default.
- Examine which loan intents are most associated with defaults.

## Business Understanding
#### Data Source
The dataset used in this project is sourced from **[Kaggle Datasets](https://www.kaggle.com/datasets)**and contains various features related to the applicant’s demographics, financial status, and loan details. The target variable is a binary indicator representing whether the applicant defaulted on the loan.
### Data Understanding
The Features in our dataset Include:
- Applicant Income: Income of the loan applicant.
- Loan Amount: Amount of loan requested.
- Credit History: History of credit transactions.
- Employment Status: Employment status of the applicant.
- Property Area: Area where the applicant owns property.
- Education: Education level of the applicant.
- Loan Status: **Target variable** indicating if the applicant defaulted.

## Data Preprocessing
The data underwent several preprocessing steps to ensure optimal model performance:

- Handling Missing Values: Missing data was imputed using the mean for numerical columns.
- Encoding Categorical Variables: Categorical variables were encoded using one-hot encoding, particularly for the features related to loan intent and home ownership.
- Feature Scaling: Numerical features were scaled using StandardScaler to normalize the data.

## Key Findings from EDA
- **Age and Default:** 49% of loan defaulters are young adults aged between 18-25.
  ![download](https://github.com/user-attachments/assets/3014e2e3-bc3b-4881-a021-0a97c11b0e57)

- **Income Group:** Middle-income earners (40k-60k) represent 29% of loan defaulters.
- **Employment Length:** Borrowers with 0-5 years of work experience account for 52% of loan defaults.
  ![download](https://github.com/user-attachments/assets/723455a2-b68b-4ad8-b5d7-30d532d03b36)

- **Loan Amount:** 37% of the loans defaulted are low-value loans ranging between 5k-10k.
- **Interest Rates:** 53% of defaults occur on loans with high interest rates, especially between 11-15%.
- **Loan Tenure:** 63% of defaults happen with short-term loans, primarily between 0-5 years.
  ![download](https://github.com/user-attachments/assets/1865f6a5-e996-4e33-95dd-6af342777d70)

- **Home Ownership:** Renters are more likely to default compared to homeowners.
- **Loan Intent:** Education loans have the highest default rate, with 20% of borrowers defaulting.
![download](https://github.com/user-attachments/assets/ae224b0e-2ffb-4e9f-8dba-ef57004500cc)


## Model Development and Evaluation
### 1. Logistic Regression
- Best Parameters: {'C': 0.01, 'penalty': 'l2', 'solver': 'liblinear'}
- Accuracy: ~55%
- Model Insights: Although Logistic Regression provided a reasonable baseline, it struggled to effectively distinguish between defaulters and non-defaulters, particularly in reducing false negatives.
### 2. Decision Tree
- Accuracy: ~80%
- Model Insights: The Decision Tree model captured more complex interactions within the data, leading to better performance compared to Logistic Regression. However, the model was susceptible to overfitting.
### 3. Random Forest (Final Model)
- Accuracy: ~89%
- Model Insights: The Random Forest model significantly outperformed the other models, achieving a good balance between precision and recall. It was particularly effective in reducing false negatives, making it a reliable choice for predicting loan defaults.

## Feature Importance Ranking:

1. Credit Length
2. Employment Length
3. Age
4. Interest Rate
5. Income
6. Percent Income
7. Loan Amount
 


![download](https://github.com/user-attachments/assets/59992f25-210a-46d1-91b7-a2f528928a3e)

## Model Selection Summary
- After comparing the models, the **Random Forest model** was selected as the final model due to its superior performance.
-  It effectively reduces false negatives, which is crucial in identifying high-risk borrowers. The model’s robustness and interpretability make it well-suited for deployment in a real-world financial setting.

## LINKS :
**[CANVA PRESENTATION](https://www.canva.com/design/DAGPQ6N_5bQ/M7sHHsew8ycrQyxsDusGqA/edit?utm_content=DAGPQ6N_5bQ&utm_campaign=designshare&utm_medium=link2&utm_source=sharebutton)**
