# Income Prediction Using Census Data
# Overview
This project applies the machine learning life cycle to the Adult Census Income dataset (1994). The objective is to build a classification model that predicts whether an individual earns more than or equal to  $50K or less than or equal to $50K per year, based on demographic and employment-related features. This type of model can be valuable in economic research, policy making, and targeted services or marketing based on income segmentation.

## 📊 Dataset

- **Source:** UCI Adult Census Income Dataset (1994)
- **File:** `censusData.csv`
- **Target Variable:** `income_binary` (`<=50K` or `>50K`)
- **Features:**
  - `age`
  - `education-num`
  - `hours-per-week`
  - `workclass`
  - `race`
  - `sex_selfID`

## 🔍 Machine Learning Problem

- **Type:** Supervised Learning
- **Category:** Binary Classification
- **Goal:** Predict income level (<=50K or >50K)


## 🛠️ Steps Performed

### 1. 🧼 Data Preparation
- Removed missing data rows
- One-hot encoded categorical features (`workclass`, `race`, `sex_selfID`)
- Standardized numerical features using `StandardScaler`

### 2. 🤖 Model Building
- **Model 1:** Logistic Regression  
  - Accuracy: ~74%
  - Best at predicting `<=50K`
- **Model 2:** Random Forest Classifier  
  - Accuracy: ~78%
  - Better balance across income classes

### 3. 📈 Evaluation
- Metrics used:
  - Accuracy
  - Precision, Recall, F1-score
  - Confusion Matrix with heatmap (Seaborn)

## ✅ Results Summary

- **Random Forest Classifier** outperformed logistic regression.
- It was more effective at predicting higher-income individuals.
- Class imbalance was observed, affecting recall for `>50K` class.

## 📚 Tools/Technologies Used

- **Language:** Python 3, Jupyter Notebook
- **Tools:** Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn
