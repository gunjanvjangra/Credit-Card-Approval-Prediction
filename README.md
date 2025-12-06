# 📌 **Credit Card Approval Prediction — Machine Learning Project**

This project aims to build a machine learning-based system to predict whether a credit card applicant is likely to default, based on historical repayment behaviour and demographic attributes. Such a predictive model helps financial institutions automate and strengthen approval decisions.

---

## 🧾 Project Overview

Credit card approval decisions require careful evaluation of applicant creditworthiness. This system automates the classification process by analyzing customer information and past repayment history.
The project uses a dataset from Kaggle, consisting of:

| Dataset                | Description                          |
| ---------------------- | ------------------------------------ |
| **Application Record** | Personal & demographic details       |
| **Credit Record**      | Monthly repayment & credit behaviour |

The two datasets were merged for default classification.

---

## 🎯 Objectives

* Construct binary classification label — **Default (1)** or **Non-Default (0)**.
* Perform preprocessing: merging, encoding, scaling, cleaning.
* Train multiple machine learning models:

  * Logistic Regression
  * Support Vector Machine (SVM)
  * Random Forest Classifier
* Compare model performances using detailed evaluation metrics.
* Analyze most important risk factors affecting credit default.

---

## 📂 Project Workflow

1. **Data Collection**

   * Kaggle dataset: *Credit Card Approval Prediction*

2. **Data Preparation**

   * Merge datasets using ID
   * Drop missing/irrelevant features
   * Scale numeric attributes (StandardScaler)
   * One-Hot Encode categorical variables

3. **Target Variable Construction**

   * Based on STATUS codes:

     * Codes `2,3,4,5` → Default (1)
     * Others → Non-Default (0)

4. **Model Training**

   * 80/20 train-test split (stratified)
   * `class_weight="balanced"` used to handle imbalance

5. **Model Evaluation**

   * Accuracy
   * Precision
   * Recall
   * F1 Score
   * ROC-AUC Score

---

## 📊 Results Summary

| Model                        | Accuracy   | Precision | Recall     | F1-Score  | ROC-AUC   |
| ---------------------------- | ---------- | --------- | ---------- | --------- | --------- |
| Logistic Regression          | 62.42%     | 0.02      | 0.447      | 0.038     | 0.544     |
| Support Vector Machine (SVM) | 78.25%     | 0.0367    | **0.4715** | 0.068     | 0.651     |
| **Random Forest**            | **96.22%** | **0.191** | 0.382      | **0.254** | **0.803** |

📌 *Random Forest shows best overall balanced performance.*

---

## 🛠 Tools & Technologies

| Technology           | Role                    |
| -------------------- | ----------------------- |
| Python               | Implementation          |
| NumPy / Pandas       | Data Processing         |
| Scikit-Learn         | Machine Learning Models |
| Matplotlib / Seaborn | Visualization           |

---

## 🚀 How to Run the Project

```bash
# Clone Project
git clone <your-repository-link>

# Install Required Libraries
pip install -r requirements.txt

# Execute Notebook or Python Script
jupyter notebook CreditCardApprovalPrediction.ipynb
```
