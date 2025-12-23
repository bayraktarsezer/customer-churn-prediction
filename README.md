# Customer Churn Prediction

This project focuses on analyzing customer behavior and building a machine learning model to predict customer churn. The objective is not only to achieve strong predictive performance but also to extract actionable business insights that can support retention strategies.

---

## Project Overview

Customer churn is a critical problem for subscription-based businesses, where retaining existing customers is often more cost-effective than acquiring new ones. In this project, we analyze a real-world telecom customer dataset to:

- Understand the key drivers of customer churn
- Build and evaluate predictive models
- Segment customers based on churn risk for practical business use

The project follows a structured data science workflow, from exploratory data analysis to model interpretation and risk segmentation.

---

## Dataset

- Source: Telecom customer churn dataset
- Size: ~7,000 customers
- Target variable: `Churn` (Yes / No)
- Feature types:
  - Demographic (e.g., gender, senior citizen)
  - Account information (tenure, contract type, payment method)
  - Service usage (internet service, tech support, streaming services)
  - Financial variables (monthly charges, total charges)

---

## Exploratory Data Analysis (EDA)

The EDA phase focuses on identifying patterns and relationships associated with churn. Key findings include:

- Customers on **month-to-month contracts** have significantly higher churn rates
- **Short tenure** customers are far more likely to churn
- Higher **monthly charges** are associated with increased churn risk
- Customers using **electronic check** as a payment method show the highest churn rate
- Availability of **technical support** strongly reduces churn probability
  
---

## Modeling Approach

### Preprocessing
- Missing values handled appropriately
- Numerical features scaled using `StandardScaler`
- Categorical features encoded with `OneHotEncoder`
- Train-test split with stratification to preserve churn distribution

### Models Evaluated
- Logistic Regression (with class weight balancing)
- Random Forest Classifier

### Model Selection
Logistic Regression was selected as the final model due to:
- Strong ROC-AUC performance
- Higher recall for churned customers
- Better interpretability compared to ensemble models

---

## Model Performance (Logistic Regression)

- ROC-AUC: ~0.84
- Recall (Churn = Yes): ~0.80
- Balanced handling of class imbalance using `class_weight='balanced'`

---

## Feature Importance & Interpretation

Coefficient analysis from the Logistic Regression model highlights the most influential factors associated with churn:

- Contract type (especially month-to-month vs long-term contracts)
- Customer tenure
- Internet service type (fiber optic)
- Monthly and total charges
- Availability of technical support

This interpretability allows the model to be directly useful for business decision-making.

---

## Risk Segmentation

Customers were segmented into three risk groups based on predicted churn probability:

- **Low Risk** (0.0 – 0.3)
- **Medium Risk** (0.3 – 0.6)
- **High Risk** (0.6 – 1.0)

The high-risk segment exhibits a substantially higher observed churn rate, making this segmentation suitable for:
- Targeted retention campaigns
- Proactive customer support
- Personalized offers for at-risk customers

---

## Technologies Used

- Python
- Pandas, NumPy
- Matplotlib
- Scikit-learn
- Jupyter Notebook

---

## Key Takeaway

This project demonstrates a complete, end-to-end data science workflow that combines exploratory analysis, predictive modeling, interpretability, and business-oriented risk segmentation. The outcome is a practical churn prediction system that can support real-world retention strategies.

---

**Author:** Sezer Bayraktar  
*Aspiring Data Scientist & AI Engineer* 🇩🇪
