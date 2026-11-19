# Framingham-Heart-Study-Analysis
# Framingham Heart Study: Predicting 10-Year Coronary Heart Disease Risk

## Overview

This project uses a Framingham Heart Study dataset to explore how demographic and clinical characteristics relate to the development of coronary heart disease (CHD). It focuses on baseline health characteristics and their association with CHD over a 10-year period, and asks how well known cardiovascular risk factors distinguish individuals who develop CHD from those who do not.

The analysis takes two complementary perspectives:

- **Statistical inference:** identifying and interpreting associations between baseline characteristics and CHD development.
- **Predictive modeling:** evaluating how effectively logistic regression can predict CHD outcomes from clinical information.

## Dataset

This project uses the Framingham Heart Study teaching dataset from [Kaggle](https://www.kaggle.com/datasets/aasheesh200/framingham-heart-study-dataset).

The dataset contains **4,240 observations** and **16 columns**, including a binary outcome indicating whether the participant developed CHD within ten years.

| Category | Variables |
|---|---|
| Demographics | Age, sex, education |
| Behavioral | Cigarettes smoked per day |
| Clinical | Blood pressure, cholesterol, BMI, heart rate, glucose |

## Methodology

### Missing Data
Missing observations were handled with imputation. Multiple imputation was used for the inferential analysis to account for the uncertainty introduced by missing values.

### Statistical Inference
Multivariable logistic regression was used to examine the association between baseline characteristics and CHD development. Results are interpreted using odds ratios, 95% confidence intervals, and p-values.

### Predictive Modeling
Logistic regression was also used as a predictive model. Performance was evaluated using a stratified train/test split and cross-validation, with the following metrics:

- Receiver operating characteristic area under the curve (ROC-AUC)
- Brier score
- Sensitivity and specificity
- Positive and negative predictive values
- Calibration

## Key Findings

- Several characteristics were associated with CHD development, including **age, sex, smoking, systolic blood pressure, and blood glucose**.
- The predictive model showed **moderate discriminatory performance**, with a test ROC-AUC of approximately **0.704**.
- Baseline characteristics contain useful information about cardiovascular risk, but the model's predictive performance and calibration reveal meaningful limitations.

## Limitations

- **Observational data:** The associations identified cannot be interpreted as evidence of causation.
- **Missing data:** Imputation relies on assumptions about the mechanisms underlying missingness.
- **Generalizability:** The characteristics of the original study population may limit how well the findings apply to other populations.
