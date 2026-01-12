# Credit Card Default Prediction

![Python](https://img.shields.io/badge/Python-3.9-blue)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Classification-orange)
![Scikit-learn](https://img.shields.io/badge/Library-Scikit--learn-green)
![Status](https://img.shields.io/badge/Status-Completed-success)

A machine learning project to predict **credit card default risk** using demographic information, credit data, and historical payment behavior.

---

## 📌 Overview
This project focuses on predicting whether a credit card customer will **default on payment in the next month**.  
Multiple machine learning models were evaluated, and the final model was selected based on performance and interpretability.

The dataset is sourced from **Kaggle (UCI Credit Card Default Dataset)** and contains real-world financial data from Taiwan.

---

## 📊 Dataset Information
- **Source:** Kaggle (UCI Machine Learning Repository)
- **Time Period:** April 2005 – September 2005
- **Total Records:** 30,000
- **Total Features:** 25
- **Target Variable:** `default.payment.next.month`
  - `1` → Default
  - `0` → No Default

### Feature Categories
- **Demographics:** Sex, Education, Marital Status, Age
- **Credit Information:** Credit Limit
- **Payment History:** `PAY_0` to `PAY_6`
- **Billing Amounts:** `BILL_AMT1` to `BILL_AMT6`
- **Previous Payments:** `PAY_AMT1` to `PAY_AMT6`

---

## 🎯 Problem Statement
To build a classification model that predicts whether a customer will default on their credit card payment in the next month, with emphasis on identifying **high-risk customers**.

---

## ⚙️ Tech Stack
- **Language:** Python
- **Libraries:**
  - NumPy
  - Pandas
  - Scikit-learn
  - Matplotlib
  - Seaborn

---

## 🧠 Methodology
1. Data loading and preprocessing
2. Exploratory Data Analysis (EDA)
3. Feature selection
4. Train-test split
5. Model training
6. Model evaluation using appropriate classification metrics

---

## 🤖 Models Evaluated

Multiple algorithms were implemented and compared.

| Model | Accuracy (%) |
|------|--------------|
| Naive Bayes | 80.0 |
| K-Nearest Neighbors (KNN) | 79.44 |
| Decision Tree (Before Tuning) | 81.2 |
| **Decision Tree (After Tuning)** | **83.4** |

---

## 🔧 Hyperparameter Tuning (Decision Tree)
Hyperparameter tuning was applied to improve generalization and reduce overfitting.

**Parameters tuned:**
- `max_depth`
- `min_samples_split`
- `min_samples_leaf`
- `class_weight`

This improved accuracy from **81.2% to 83.4%**.

---

## 🤖 Final Model
### Decision Tree Classifier (Tuned)

The tuned Decision Tree was selected as the final model due to its superior performance and interpretability.

---

## 📈 Model Evaluation

Because the dataset is **imbalanced**, accuracy alone is insufficient.  
Additional metrics were analyzed.

### Classification Report

| Class | Precision | Recall | F1-Score | Support |
|------|----------|--------|---------|--------|
| No Default (0) | 0.84 | 0.95 | 0.89 | 4,660 |
| Default (1) | 0.69 | 0.37 | 0.48 | 1,340 |
| **Accuracy** |  |  | **0.82** | 6,000 |
| **Macro Avg** | 0.76 | 0.66 | 0.69 | 6,000 |
| **Weighted Avg** | 0.81 | 0.82 | 0.80 | 6,000 |

---

### Interpretation
- Strong performance in identifying **non-defaulters** (95% recall).
- Lower recall for **defaulters (37%)**, indicating missed high-risk customers.
- In financial applications, reducing **false negatives** is critical.

---

## 🧠 Key Insights
- Recent repayment behavior (`PAY_0`, `PAY_2`, `PAY_3`) is the strongest predictor of default.
- Customers with recent payment delays have significantly higher default risk.
- Credit limit and recent payment amounts also influence predictions.

---

## 🔗 Project Links
- 📊 **Dataset (Kaggle):**  
  https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset

- 📦 **Trained Model:**  
  PASTE_YOUR_MODEL_LINK_HERE


