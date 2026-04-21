# Bank Customer Churn Risk System

## Overview
A predictive churn intelligence system that assigns risk probabilities to bank customers before they leave, built on the European Central Bank dataset.

## Problem Statement
Banks lack accurate churn prediction models, quantitative risk scores, and explainable insights into churn drivers. This project solves all three.

## Dataset
- 10,000 customers
- 14 features including CreditScore, Age, Geography, Balance, NumOfProducts
- Target variable: Exited (1 = Churned, 0 = Retained)
- Churn rate: 20.37%

## Key Findings
- Churners are ~10 years older than retained customers
- Germany has the highest churn rate
- Inactive members churn at nearly double the rate of active members (27% vs 14%)
- High balance customers are paradoxically more likely to leave

## Methodology
1. Exploratory Data Analysis
2. Feature Engineering (4 derived features)
3. Preprocessing with SMOTE for class imbalance
4. Model Development (Logistic Regression, Decision Tree, Random Forest, Gradient Boosting)
5. SHAP Explainability Analysis
6. Streamlit Web Application

## Champion Model — Gradient Boosting
| Metric | Score |
|--------|-------|
| Accuracy | 0.8200 |
| Precision | 0.5449 |
| Recall | 0.7002 |
| F1 | 0.6129 |
| ROC-AUC | 0.8607 |

## Top Churn Drivers
1. Age
2. NumOfProducts
3. Geography — Germany

## How to Run
```bash
pip install -r requirements.txt
streamlit run app.py
```

## Deliverables
- Jupyter Notebooks (EDA, Feature Engineering, Preprocessing, Modeling, SHAP)
- Streamlit Dashboard (Risk Calculator, Probability Distribution, Feature Importance, What-If Simulator)
- Research Paper
- Executive Summary
