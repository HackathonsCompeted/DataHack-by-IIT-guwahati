# Predicting Vaccine Uptake Using Behavioral and Demographic Data

## Overview
This project aims to predict the likelihood of individuals receiving the xyz flu vaccine and the seasonal flu vaccine. It uses a dataset containing various features related to the respondents' behavior, opinions, and demographics to build a predictive model. The goal is to provide probabilities for each individual, indicating their likelihood of receiving each vaccine.

## Dataset
The dataset contains 36 columns:
- **respondent_id**: Unique identifier for each respondent.
- **35 Features**: Behavioral habits, opinions on vaccine effectiveness and risks, and demographic information.

### Features
- **Behavioral Variables**: antiviral medications, face mask purchase, social distancing, etc.
- **Opinion Variables**: perceived effectiveness and risks of vaccines.
- **Demographic Variables**: age group, education level, race, income level, marital status, employment status, etc.

### Labels
- **xyz_vaccine**: Whether the respondent received the xyz flu vaccine (0 = No, 1 = Yes).
- **seasonal_vaccine**: Whether the respondent received the seasonal flu vaccine (0 = No, 1 = Yes).

## Methodology

### Data Preprocessing
1. **Handle Missing Values**: Use `SimpleImputer` for imputation.
2. **Encode Categorical Variables**: Use `OneHotEncoder`.
3. **Scale Numerical Variables**: Use `StandardScaler`.

### Model Development
- **Algorithm**: RandomForestClassifier
- **Pipeline**: Integrate preprocessing steps and model training.

### Model Evaluation
- **Metric**: ROC AUC score for each target variable (`xyz_vaccine` and `seasonal_vaccine`).
- **Overall Score**: Mean of the ROC AUC scores.

### Prediction and Submission
1. **Predict Probabilities**: For the test dataset.
2. **Prepare Submission File**: With columns `respondent_id`, `xyz_vaccine`, and `seasonal_vaccine`.
