# Predicting Employee Attrition

## Overview
Employee attrition poses a significant challenge for organizations, impacting productivity, morale, and financial stability. Traditional attrition analysis methods are often subjective and time-consuming. Machine learning provides a powerful approach to predicting employee attrition by identifying key factors and trends using historical data.

## Objective
The goal of this project is to leverage machine learning techniques to predict whether an employee is likely to leave a company based on various demographic, job-related, and workplace satisfaction metrics. By analyzing these factors, organizations can make data-driven decisions to improve employee retention strategies.

## Dataset
The dataset includes employee attributes such as:
- **Demographic Information** (Age, Gender, Marital Status, etc.)
- **Job-related Factors** (Department, Job Role, Job Level, etc.)
- **Workplace Satisfaction Metrics** (Job Satisfaction, Work-Life Balance, etc.)
- **Compensation Details** (Salary, Bonus, Benefits, etc.)
- **Performance and Tenure** (Years at Company, Performance Rating, etc.)

## Approach
1. **Data Preprocessing**
   - Handling missing values
   - Encoding categorical variables
   - Feature scaling and transformation
2. **Exploratory Data Analysis (EDA)**
   - Identifying trends and correlations
   - Visualizing key features impacting attrition
3. **Model Selection & Training**
3.1 The baseline Model :
  -  Logistic Regression.
3.2 * The Complex Models:
- K-Nearest Neighbors        
- Support Vector Classifier
- And some Ensemble Methods like: 
- Random Forest              
- Gradient Boosting          
- XGBoost
* 3.3 Our final model:
  - we preffred to leverage the strengths of multiple models,
  we applied an ensemble learning approach using a voting classifier, which combines predictions from Gradient Boosting, Random Forest, and XGBoost.
 By using soft voting, And here we have reached something we are satisfied with :) ..

5. **Evaluation & Optimization**
   - Accuracy, Precision, Recall, F1-score
   - Hyperparameter tuning using Grid Search/Randomized Search
   - Feature importance analysis


### Requirements
- Python 3.x
- Pandas
- NumPy
- Scikit-learn
- Matplotlib & Seaborn (for visualization)
- XGBoost/LightGBM (for advanced modeling)


## Results & Insights
The model demonstrates significant improvements in predicting employee attrition:

- Precision skyrocketed (from 0.64 → 0.96), meaning fewer false positives.

- Recall improved significantly (0.41 → 0.86), ensuring more true positives are captured.

- F1-score is now 0.90, showing a great balance between precision and recall.

- ROC-AUC (0.95) indicates strong overall classification ability.

These results highlight the effectiveness of the machine learning approach in identifying key factors influencing employee attrition, helping organizations make strategic decisions to improve retention

## Contributions
Contributions are welcome! Feel free to fork the repository, submit pull requests, or raise issues.

## Acknowledgments
- Open-source datasets on employee attrition from kaggle .

