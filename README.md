# phase-02-Task-2-End-to-End-ML-Pipeline-for-Customer-Churn-Prediction

## Project Overview
This project builds a production-ready machine learning pipeline to predict customer churn using the Telco Customer Churn dataset.

## Files Included
- `churn_pipeline_tuned.joblib` - The complete trained pipeline (preprocessing + model)
- `phase_02_task_02_customer_churn.ipynb` - Jupyter notebook with full implementation

## Model Performance

| Metric | Score |
|--------|-------|
| Accuracy | 79.60% |
| Cross-validation Score | 80.37% |
| Precision (Churn) | 0.66 |
| Recall (Churn) | 0.49 |
| F1-Score (Churn) | 0.56 |

## Best Hyperparameters (GridSearchCV)
- `n_estimators`: 100
- `max_depth`: 10
- `min_samples_split`: 2

## How to Use the Pipeline

### Load and Predict
```python
import joblib
import pandas as pd

# Load the pipeline
model = joblib.load('churn_pipeline_tuned.joblib')

# Predict on new customer data
predictions = model.predict(X_new)
probabilities = model.predict_proba(X_new)
Requirements
Python 3.10+

scikit-learn

pandas

numpy

joblib

Pipeline Components
Preprocessing: ColumnTransformer with StandardScaler (numerical) + OneHotEncoder (categorical)

Model: Random Forest Classifier

Tuning: GridSearchCV with 5-fold cross validation

Results Summary
Successfully predicted customer churn with ~80% accuracy

Pipeline is ready for production deployment

Exported using joblib for reusability

Author
Zaryab Ahmad
Task completed as part of ML Internship Assignment
