

# 📞 Telco Customer Churn Analysis

![Python](https://img.shields.io/badge/Python-3.9-blue?logo=python)
![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-yellow?logo=pandas)
![NumPy](https://img.shields.io/badge/NumPy-Numerical-lightblue?logo=numpy)
![Matplotlib](https://img.shields.io/badge/Matplotlib-Visualization-orange?logo=plotly)
![Seaborn](https://img.shields.io/badge/Seaborn-Statistical%20Plots-green)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML%20Models-red?logo=scikitlearn)
![Imbalanced-learn](https://img.shields.io/badge/Imbalanced--learn-SMOTEENN-purple)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter)

---

## 📊 Project Overview

This project analyzes **customer churn behavior** at a fictional telecom company, **TelcoCorp**. Using **EDA** and **Machine Learning**, the aim is to **identify churn drivers** and build a **predictive model** to reduce churn.

---

## 🎯 Objectives

* Explore customer demographics, services, and billing details.
* Identify **key churn factors**.
* Build a **predictive model** with high recall for churned customers.
* Recommend **data-driven retention strategies**.

---

## 🧰 Tools & Technologies

* **Python** | **Pandas** | **NumPy** | **Matplotlib** | **Seaborn**
* **Scikit-learn** | **imblearn (SMOTEENN)** | **Pickle**
* **Jupyter Notebook** | **VS Code**

---

## 📂 Dataset

* **Source**: IBM Sample Dataset (Public)
* **File**: `WA_Fn-UseC_-Telco-Customer-Churn.csv`
* **Rows**: 7,043 | **Columns**: 21

**Features:**

* 👤 Demographics (Gender, SeniorCitizen, etc.)
* 🛠️ Services (Internet, OnlineSecurity, TechSupport, etc.)
* 💳 Billing (MonthlyCharges, TotalCharges, PaymentMethod)
* 🎯 Target → **Churn (Yes/No)**

---

## 🧹 Data Cleaning

✔ Converted `TotalCharges` → numeric
✔ Filled missing values
✔ Removed irrelevant columns (`customerID`)
✔ Encoded categorical features
✔ Balanced dataset using **SMOTEENN**

---

## 📈 Key Insights (EDA)

* 📉 **Churn Rate**: \~26.5%
* 💳 **Electronic Check** users churn most.
* 📆 **Month-to-Month contracts** → higher churn risk.
* 🔐 No **Online Security/Tech Support** → higher churn.
* 💰 High **MonthlyCharges + short tenure** → churn risk.
* 👥 Younger customers churn more than seniors.

---

## 🧠 Business Recommendations

* 💳 Encourage **Auto-Payments** to reduce churn.
* 📆 Offer **discounts on annual contracts**.
* 🛠️ Bundle **Online Security + Tech Support** services.
* 👩‍💼 Launch **engagement campaigns for younger customers**.

---

## 🤖 Model Building

### Data Prep

* Train-test split
* Class imbalance handled with **SMOTEENN**

### Models Tested

* **Decision Tree** → 78% accuracy (imbalanced), 93% with SMOTEENN
* **Random Forest** → **94.27% accuracy, 0.96 recall (best model)**
* **PCA** → 72% accuracy (discarded)

### Final Model

✅ **Random Forest + SMOTEENN**
✅ Saved using **Pickle (`model.sav`)**

---

## 📊 Results & Business Impact

* Predictive model detects **96% of churned customers**.
* Insights drive strategies to reduce churn:

  * Push auto-payments
  * Promote yearly contracts
  * Add bundled services
  * Focus on younger user retention

📌 **Impact** → Proactive strategies can **reduce churn, retain high-value customers, and save millions in revenue**.

---

## 🛠️ Project Workflow

```mermaid
flowchart TD
    A[📂 Dataset] --> B[🧹 Data Cleaning & Prep]
    B --> C[📈 Exploratory Data Analysis]
    C --> D[⚖️ Handle Imbalance - SMOTEENN]
    D --> E[🤖 Model Training - Decision Tree / RF]
    E --> F[📊 Model Evaluation]
    F --> G[✅ Final Model - Random Forest + SMOTEENN]
    G --> H[💡 Insights & Recommendations]
```

---

✨ This project demonstrates how **EDA + Machine Learning** can empower telecoms to proactively reduce churn and boost customer loyalty.


