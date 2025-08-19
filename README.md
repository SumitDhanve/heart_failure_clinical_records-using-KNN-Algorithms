# heart_failure_clinical_records-using-KNN-Algorithms
## Project Overview
This project predicts the likelihood of death events in patients with heart failure using the K-Nearest Neighbors (KNN) algorithm. By analyzing clinical records such as age, serum creatinine, ejection fraction, and high blood pressure, the model helps identify risk factors and predict patient outcomes.

## Dataset
Rows: 299

Columns: 13

## Features

**Numerical & Categorical:**

age → Age of patient

anaemia → Anemia status (0 = No, 1 = Yes)

creatinine_phosphokinase → Enzyme level

diabetes → Diabetes (0/1)

ejection_fraction → Percentage of blood leaving the heart

high_blood_pressure → Hypertension (0/1)

platelets → Platelet count

serum_creatinine → Serum creatinine level

serum_sodium → Sodium level

sex → Gender (0 = Female, 1 = Male)

smoking → Smoking history (0/1)

time → Follow-up period (days)

Target Variable:

DEATH_EVENT → (0 = Alive, 1 = Death)

## Project Workflow
1. Data Understanding

Dataset contains 299 rows × 13 columns.

Target variable: DEATH_EVENT (binary classification).

2. Data Cleaning

No missing values.

Checked for outliers and distributions.

3. Feature Engineering

Normalized numerical features (important for KNN).

Retained categorical and binary features as numeric.

4. EDA (Exploratory Data Analysis)

Univariate: Histograms for age, ejection fraction, serum creatinine.

Bivariate: Boxplots and correlation heatmaps with DEATH_EVENT.

Observed that older age, high creatinine, low ejection fraction are linked to higher death events.

5. Model Preparation

Features (X) = All columns except DEATH_EVENT.

Target (y) = DEATH_EVENT.

Train-Test Split: 80% training, 20% testing.

Scaled features using StandardScaler (important for distance-based algorithms).

6. Model Building

Applied K-Nearest Neighbors (KNN) Classifier.

Tuned k-values using cross-validation (e.g., k = 3, 5, 7, …).

7. Model Evaluation

Metrics Used:

Accuracy Score

Confusion Matrix

Precision, Recall, F1-score

ROC-AUC Score

## Results

The best KNN model gave good classification accuracy.

Key Predictors of DEATH_EVENT:

Age (age)

Ejection Fraction (ejection_fraction)

Serum Creatinine (serum_creatinine)

Time (time)

## Technologies Used

Python

Pandas, NumPy → Data Handling

Matplotlib, Seaborn → Visualization

Scikit-learn → KNN, Scaling, Model Evaluation
