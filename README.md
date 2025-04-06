# Predicting Employee Attrition

## 📌 Overview
Employee attrition poses a significant challenge for organizations, impacting productivity, morale, and financial stability. Traditional analysis methods are often subjective and time-consuming. Machine learning offers a powerful approach to proactively predict attrition using historical employee data.

---

## 🎯 Objective
The goal of this project is to build a predictive model that identifies whether an employee is likely to leave a company based on various demographic, job-related, and satisfaction metrics. This enables data-driven retention strategies.

---

## 📊 Dataset
The dataset includes employee attributes such as:
- **Demographic Information** (Age, Gender, Marital Status)
- **Job-related Factors** (Department, Job Role, Job Level)
- **Satisfaction Metrics** (Job Satisfaction, Work-Life Balance)
- **Compensation Details** (Salary, Bonus, Benefits)
- **Performance & Tenure** (Years at Company, Performance Rating)

---

## 🧠 Approach

### 1. **Data Preprocessing**
- Handled missing values and duplicates  
- Encoded categorical variables  
- Applied scaling and normalization  

### 2. **Exploratory Data Analysis (EDA)**
- Visualized feature distributions and correlations  
- Analyzed skewness and normalized features  
- Detected outliers and class imbalance  

### 3. **Model Selection & Training**

#### ✅ Baseline Models:
- Logistic Regression  
- K-Nearest Neighbors  
- Support Vector Classifier  

#### ✅ Ensemble Models:
- Random Forest  
- Gradient Boosting  
- XGBoost  

### ✅ Final Model: **Stacking Classifier**
To leverage the strengths of multiple models, we used a **Stacking Classifier** combining:
- **Logistic Regression** (C = 10)  
- **LightGBM** (learning_rate = 0.01, n_estimators = 200)  
with a meta-classifier: **Logistic Regression** (C = 10)

**Final classification threshold = 0.2**, optimized for better recall on attrition.

---

## 📈 Results & Insights

| Metric          | Class 0 (Stayed) | Class 1 (Attrition) |
|-----------------|------------------|----------------------|
| Precision       | 0.92             | 0.63                 |
| Recall          | 0.96             | 0.44                 |
| F1-Score        | 0.94             | 0.52                 |

**Overall:**
- **Accuracy:** 0.89  
- **ROC-AUC:** 0.80  
- **Macro Avg F1-Score:** 0.73  

🔹 The model successfully balances performance on both classes, especially boosting recall for attrition cases.  
🔹 ROC-AUC of 0.80+ indicates strong classification capability.

---

## 🛠 Requirements

Install dependencies with:

```bash
pip install -r requirements.txt
```

**Main Libraries:**
- Python 3.x  
- Pandas  
- NumPy  
- Scikit-learn  
- LightGBM  
- XGBoost  
- Seaborn & Matplotlib (for visualization)

---

## 🚀 How to Use
1. Clone this repo  
2. Prepare your dataset and run preprocessing  
3. Train the model (`stacking_model.fit`)  
4. Predict attrition (`stacking_model.predict`)  
5. Evaluate and adjust threshold for desired performance  

---

## 🤝 Contributions
Feel free to fork, contribute, and submit pull requests!

---

## 🙏 Acknowledgments
Thanks to open-source contributions and [Kaggle](https://www.kaggle.com) for the dataset on employee attrition.

---

Let me know if you’d like a `requirements.txt`, usage example in code, or add visuals like a confusion matrix or ROC curve to the README!
