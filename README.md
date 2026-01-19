# Heart Disease Prediction using Machine Learning

This project predicts the presence of heart disease using several machine learning algorithms trained on the *Heart Failure Prediction* dataset from Kaggle.  

Models were evaluated using metrics such as Accuracy, ROC Curve, and AUC. Hyperparameter tuning was applied to optimize performance.

---

## Dataset
Source: Kaggle — *Heart Failure Prediction*

**Target variable:**
- `HeartDisease` (1 = disease, 0 = no disease)

**Example features used:**
- Age
- Cholesterol
- RestingBP
- ExerciseAngina
- Oldpeak
- ST_Slope
- Sex
- FastingBS
*(after encoding + preprocessing)*

---

## Models Used
- Logistic Regression
- Decision Tree
- Random Forest
- XGBoost

---

## Hyperparameter Tuning
Performed using `GridSearchCV` with AUC as optimization metric.

**Best Model:** Random Forest

**Best Parameters:** 
`{'n_estimators': 500,
'min_samples_split': 5,
'min_samples_leaf': 4,
'max_depth': 9,
'bootstrap': False}`

**Final Test Results (Random Forest):**
- Accuracy: ~0.87
- AUC: ~0.93

**Classification Report:**
- Class 0 (No Disease): Precision 0.84, Recall 0.84
- Class 1 (Disease): Precision 0.89, Recall 0.89
