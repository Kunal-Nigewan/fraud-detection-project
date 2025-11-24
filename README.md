# Credit Card Fraud Detection

## 1. 📌 Project Overview  
This project focuses on detecting fraudulent credit card transactions using the popular **Kaggle Credit Card Fraud Detection dataset** containing **284,807 transactions**, of which only **492 are fraud** (0.172%).  

The dataset is highly imbalanced, and this project explores techniques such as:
- Handling class imbalance  
- Scaling numerical features  
- Model evaluation for rare event classification  
- Logistic Regression, Random Forest, and XGBoost  

---

## 2. 🎯 Motivation  
Credit card fraud causes massive financial losses globally.  
The goal of this project is to build an ML model that can detect fraudulent transactions with high recall while minimizing false positives.

---

## 3. 📂 Dataset (Kaggle)  
- **Rows:** 284,807  
- **Fraud cases:** 492  
- **Imbalance ratio:** ~0.172% (very imbalanced)  
- **Features:**  
  - 28 PCA-transformed columns: `V1, V2, ..., V28`  
  - `Time`  
  - `Amount`  
  - `Class` (0 = Non-Fraud, 1 = Fraud)  

The PCA transformation was applied by the dataset creators for privacy reasons.

---

## 4. 🔧 Methodology  

### 4.1 Data Preprocessing  
- Scaled the `Amount` feature (StandardScaler)  
- Kept PCA features as they are  
- Train-test split  
- Applied **SMOTE** to balance minority class  
- Handled class imbalance using:  
  - Oversampling  
  - Class weights  

---

### 4.2 Exploratory Data Analysis  
- Distribution of fraud vs non-fraud  
- Correlation analysis  
- Time vs fraud patterns  
- Amount vs fraud patterns  
- PCA feature visualization  

---

### 4.3 Machine Learning Models Used  
- **Logistic Regression**  
- **Random Forest Classifier**  
- **XGBoost Classifier**  

Each model was tested on:
- Original imbalanced data  
- SMOTE oversampled data  

---

## 5. 🏆 Results Summary  

### Logistic Regression  
- Good baseline  
- Accuracy high (because of imbalance)  
- Recall low → misses many frauds  

### Random Forest  
- Better recall  
- Handles imbalance better  
- Good precision  

### XGBoost (Best Performer)  
- Highest recall  
- Highest F1-score  
- Best ROC-AUC  
- Best fraud detection performance  

_(Exact numbers depend on your notebook, you can add them later.)_

---

## 6. 📌 Conclusion  
- Fraud detection is challenging due to extreme class imbalance  
- SMOTE and tree-based models significantly improve performance  
- XGBoost is the best model for this dataset  
- Real-world deployment must consider false positives + explainability  

---

## 7. 🚀 How to Run the Project  

1. Clone the repository:  
