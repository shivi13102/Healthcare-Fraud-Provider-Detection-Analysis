# Healthcare Fraud Detection Analysis

## Project Overview

This project aims to develop a model for detecting healthcare fraud using machine learning techniques. The analysis leverages a dataset containing various beneficiary attributes and healthcare reimbursement amounts. The objective is to identify fraudulent claims and profile high-risk beneficiaries.

## Table of Contents

- [Technologies Used](#technologies-used)
- [Data Description](#data-description)
- [Data Cleaning and Transformation](#data-cleaning-and-transformation)
- [Data Modeling](#data-modeling)
- [Results](#results)
- [Conclusion](#conclusion)
- [Future Work](#future-work)

## Technologies Used

- **Python**: Programming language for data analysis and modeling.
- **Pandas**: Library for data manipulation and analysis.
- **NumPy**: Library for numerical computations.
- **Scikit-learn**: Library for machine learning algorithms.
- **Seaborn & Matplotlib**: Libraries for data visualization.
- **Google Colab**: Environment for executing Python code and collaborating.

## Data Description

The dataset used in this project is `train_bene_final_data.xlsx`, which includes the following columns:

- `BeneID`: Unique identifier for beneficiaries.
- `DOB`: Date of birth of beneficiaries.
- `DOD`: Date of death of beneficiaries (if applicable).
- `Gender`: Gender of the beneficiary.
- `Race`: Race of the beneficiary.
- `RenalDiseaseIndicator`: Indicator of renal disease.
- `State`: State of residence.
- `Country`: Country of residence.
- `NoOfMonths_PartACov`: Number of months covered by Part A.
- `NoOfMonths_PartBCov`: Number of months covered by Part B.
- `ChronicCond_*`: Indicators for various chronic conditions.
- `IPAnnualReimbursementAmt`: Annual reimbursement amount for inpatient services.
- `IPAnnualDeductibleAmt`: Annual deductible amount for inpatient services.
- `OPAnnualReimbursementAmt`: Annual reimbursement amount for outpatient services.
- `OPAnnualDeductibleAmt`: Annual deductible amount for outpatient services.
- `Age`: Age of the beneficiary.
- `ChronicConditionCount`: Count of chronic conditions.
- `fraud`: Target variable indicating whether a claim is fraudulent.

## Data Cleaning and Transformation

1. **Handling Missing Values**: Missing values are checked and managed appropriately.
2. **Feature Engineering**: Creation of a target variable `fraud` based on reimbursement amounts, identifying claims in the top 5% as fraudulent.
3. **Categorical Encoding**: Categorical variables are transformed into dummy variables for modeling.

## Data Modeling

The project employs several classification models to detect fraud:

1. **Logistic Regression**: A baseline model to understand the relationships between features and the target variable.
2. **Random Forest**: An ensemble model that improves predictive accuracy by combining multiple decision trees.
3. **Gradient Boosting**: Another ensemble method that sequentially builds models to improve predictions.

### Model Evaluation

Each model's performance is evaluated using:
- Classification reports (precision, recall, F1-score)
- AUC-ROC score to assess the ability to distinguish between classes.

## Results

- **Logistic Regression**:
  - AUC-ROC: 0.994
- **Random Forest**:
  - AUC-ROC: 1.0 (perfect classification)
- **Gradient Boosting**:
  - AUC-ROC: 1.0 (perfect classification)

### Anomaly Detection

- **K-Means Clustering**: Used to identify clusters in the data.
- **Isolation Forest**: Employed for detecting anomalies.

## Conclusion

The models developed in this project demonstrate high accuracy in detecting fraudulent claims, with Random Forest and Gradient Boosting achieving perfect classification. The analysis of high-risk groups highlights patterns that can inform further investigations and interventions.

## Future Work

- Explore advanced deep learning techniques for enhanced fraud detection.
- Implement real-time fraud detection systems.
- Integrate additional features for a more comprehensive analysis.
