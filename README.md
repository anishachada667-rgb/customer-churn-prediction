# Customer Churn Prediction Using Machine Learning

## 📌 Project Overview

Customer churn is one of the most important business challenges for subscription-based companies. This project aims to predict whether a customer is likely to leave a telecom service provider based on customer demographics, account information, and service usage patterns.

The objective is to identify at-risk customers early so that businesses can take proactive retention measures.

---

## 🎯 Problem Statement

Customer acquisition is expensive, and retaining existing customers is critical for business growth. The goal of this project is to build a machine learning model that predicts customer churn and helps businesses reduce customer attrition.

---

## 📊 Dataset

Dataset: Telco Customer Churn Dataset

- Total Records: 7,043
- Features: 21
- Target Variable: Churn

### Key Features

- Gender
- Senior Citizen
- Partner
- Dependents
- Tenure
- Phone Service
- Internet Service
- Online Security
- Online Backup
- Device Protection
- Tech Support
- Contract Type
- Payment Method
- Monthly Charges
- Total Charges

Target:

- Churn (Yes / No)

---

## 🛠️ Technologies Used

- Python
- Pandas
- NumPy
- Scikit-Learn
- XGBoost
- Imbalanced-Learn (SMOTE)
- Matplotlib
- Seaborn
- Jupyter Notebook
- Git
- GitHub

---

## 🔄 Project Workflow

### 1. Data Collection

- Loaded customer churn dataset using Pandas.

### 2. Data Exploration

- Analyzed dataset shape and structure.
- Checked data types and missing values.
- Explored target variable distribution.

### 3. Data Cleaning

- Converted TotalCharges to numeric format.
- Handled missing values.
- Removed unnecessary customerID column.

### 4. Feature Engineering

- Encoded target variable:
  - Yes → 1
  - No → 0
- Applied One-Hot Encoding for categorical features.

### 5. Handling Class Imbalance

- Applied SMOTE (Synthetic Minority Oversampling Technique) to improve minority class prediction performance.

### 6. Model Training

Models evaluated:

- Random Forest Classifier
- Logistic Regression
- XGBoost Classifier

### 7. Model Evaluation

Evaluation metrics:

- Accuracy
- Precision
- Recall
- F1-Score
- Confusion Matrix

### 8. Threshold Optimization

Adjusted classification threshold from 0.5 to 0.4 to improve churn recall and better identify at-risk customers.

---

## 📈 Results

### Model Comparison

| Model | Accuracy | Churn Recall |
|---------|---------|---------|
| Random Forest | 78% | 45% |
| Random Forest + SMOTE | 78% | 59% |
| XGBoost | 75% | 61% |
| XGBoost (Threshold = 0.4) | 73% | 76% |

### Best Model

**XGBoost with threshold tuning (0.4)**

Key achievement:

- Improved churn recall from 45% to 76%.
- Increased ability to identify customers likely to leave.
- Better suited for customer retention strategies.

---

## 🔍 Feature Importance

Top factors influencing customer churn:

1. Total Charges
2. Monthly Charges
3. Tenure
4. Internet Service (Fiber Optic)
5. Payment Method (Electronic Check)
6. Contract Type
7. Online Security
8. Tech Support

---

## 💾 Model Saving

The final trained model was saved using Pickle:

```python
import pickle

pickle.dump(model, open("churn_model.pkl", "wb"))
```

Saved file:

```text
churn_model.pkl
```

---

## 🚀 How to Run the Project

### Clone Repository

```bash
git clone https://github.com/anishachada667-rgb/customer-churn-prediction.git
```

### Navigate to Project Folder

```bash
cd customer-churn-prediction
```

### Install Dependencies

```bash
pip install pandas numpy scikit-learn xgboost imbalanced-learn matplotlib seaborn
```

### Run Notebook

Open:

```text
notebooks/customer_churn.ipynb
```

and execute cells sequentially.

---

## 📂 Project Structure

```text
Customer_Churn_Prediction
│
├── data
│   └── churn.csv
│
├── notebooks
│   └── customer_churn.ipynb
│
├── models
│   └── churn_model.pkl
│
├── README.md
│
└── requirements.txt
```

---

## 📚 Key Learnings

- Data Cleaning and Preprocessing
- Feature Engineering
- Handling Imbalanced Datasets using SMOTE
- Machine Learning Model Development
- Model Evaluation and Comparison
- Threshold Optimization
- Version Control with Git and GitHub

---

## 👩‍💻 Author

Anisha Reddy Chada

MS Information Technology  
University of Cincinnati

GitHub:
https://github.com/anishachada667-rgb