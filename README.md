# Retain'Em: IIS Ltd. Customer Churn Prediction

[![Hackathon Project](https://img.shields.io/badge/Hackathon-CxC-blue)](https://devpost.com/software/retain-em-iis-ltd-customer-churn-prediction)

Our project leverages data analysis and machine learning techniques to predict customer churn in a wealth management platform, enabling proactive retention strategies and enhancing financial service efficiency.

---

## Table of Contents

- [Inspiration](#inspiration)  
- [What it does](#what-it-does)  
- [How we built it](#how-we-built-it)  
- [Marketing Strategy](#marketing-strategy)  
- [Challenges we ran into](#challenges-we-ran-into)  
- [Accomplishments we're proud of](#accomplishments-were-proud-of)  
- [What we learned](#what-we-learned)  
- [What's next](#whats-next)  
- [Team](#team)  

---

## Inspiration

Motivated by a practical interest in data science and machine learning, our team aimed to improve customer retention strategies. Customer churn is a significant challenge across subscription-based services, and identifying patterns to prevent churn can provide tangible business impact.  

We were particularly interested in the technical challenge of handling large datasets with missing values and applying advanced ML models to derive actionable insights for financial institutions.

---

## What it does

The XGBoost model predicts customer churn on test data, serving as a foundation for statistical analysis. This analysis allows us to create actionable marketing strategies autonomously, using insights from model predictions to enhance retention efforts and optimize customer engagement.

---

## How we built it

1. **Data Preprocessing**
   - Removed columns with >50% missing values and columns with a single unique value.  
   - Implemented targeted imputation for remaining missing values.  
   - Transformed date columns into months relative to a fixed date.  
   - Normalized features for model consistency.  
   - Applied SMOTE + Tomek links to address class imbalance.

2. **Modeling**
   - Used **XGBoost** with a subsampling rate of 0.8 for bagging.  
   - Achieved **Accuracy:** 98.06% and **F1 Score:** 0.981.  

**Classification Report:**

|                | Precision | Recall | F1-score | Support |
|----------------|-----------|--------|----------|---------|
| Non-Churn (0)  | 1.00      | 0.96   | 0.98     | 107293  |
| Churn (1)      | 0.97      | 1.00   | 0.98     | 107623  |
| **Accuracy**   |           |        | 0.98     | 214916  |
| **Macro Avg**  | 0.98      | 0.98   | 0.98     | 214916  |
| **Weighted Avg** | 0.98    | 0.98   | 0.98     | 214916  |

**Confusion Matrix:**

|                | Predicted Non-Churn | Predicted Churn |
|----------------|-------------------|----------------|
| Actual Non-Churn | 103414           | 3879           |
| Actual Churn    | 272              | 107351         |

---

## Marketing Strategy

Some key insights derived from model predictions:

- **Account types Cash, Margin, Cash Sweep, COD** are more likely to churn.  
  - **Strategy:** Offer value-added services, rewards, and exclusive perks to incentivize retention.  

- **is_registered = false** → higher churn probability.  
- **is_arp_locked = true** → customers are less likely to churn.  

These insights provide actionable directions for marketing and retention strategies.

---

## Challenges we ran into

- Large dataset with many missing values and irrelevant features.  
- SVM model training was computationally expensive (>3 hours) and ineffective.  
- PCA made feature importance interpretation challenging.  
- Required careful selection of interpretable models to derive actionable insights.  

The CxC Hackathon workshops were invaluable for navigating these challenges and improving our approach.

---

## Accomplishments we're proud of

- Efficiently handled missing values and irrelevant features through preprocessing and feature engineering.  
- Selected and fine-tuned **XGBoost**, achieving 98.06% accuracy.  
- Derived actionable marketing strategies from predictive insights.  

---

## What we learned

- Importance of robust data preprocessing and feature engineering.  
- Application of data balancing techniques like SMOTE + Tomek links.  
- Exploration of model evaluation metrics, particularly F1 score and accuracy.  
- Hands-on experience with bagging, boosting, and XGBoost model implementation.  

---

## What's next for Retain'Em

- Conduct deeper exploratory analysis on model predictions.  
- Refine marketing strategies based on nuanced patterns identified.  
- Enhance retention strategies and overall business impact for IIS Ltd.  

---

## Team

- **Aditya Parekh** – Data preprocessing, XGBoost modeling, analysis  
- **Aditya Mani** – Data Cleaning & Feature Engineering  
- **Jithin Krishna** – Model Development & Evaluation  
- **Srishti Prayag** – Data Visualization & Insights

---

**Project Link on Devpost:** [Retain'Em: IIS Ltd. Customer Churn Prediction](https://devpost.com/software/retain-em-iis-ltd-customer-churn-prediction)
