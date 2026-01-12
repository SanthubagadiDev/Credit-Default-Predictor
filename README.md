# Credit Card Default Prediction


A machine learning project to predict **credit card default risk** using demographic information, credit data, and historical payment behavior.

**Credit card default prediction** is a critical task in the financial sector, as it helps banks and financial institutions minimize credit risk and make informed lending decisions. This project focuses on building a machine learning model to predict whether a credit card client will default on their payment in the following month.

The dataset used in this project contains detailed information on credit card clients in Taiwan, including demographic characteristics, credit limits, repayment history, bill statements, and previous payment amounts from April 2005 to September 2005. A total of 25 variables are included, providing a comprehensive view of customer behavior and financial status.

---

## 📊 Dataset Information
- **Source:** [DATASET](https://www.kaggle.com/datasets/uciml/default-of-credit-card-clients-dataset/data)

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
Financial institutions face significant losses due to credit card defaults, making it essential to accurately predict customers who are likely to fail in meeting their payment obligations. Traditional risk assessment methods often struggle to capture complex relationships between customer demographics, repayment behavior, and financial history.

The objective of this project is to build a machine learning model that predicts whether a credit card customer will default on their payment in the next month, using historical payment behavior, billing information, and demographic data.

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


