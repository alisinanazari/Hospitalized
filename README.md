📌 Project Overview
This project aims to predict patient hospitalization based on various clinical and demographic features using Stacking Classifiers (XGBoost & LightGBM).
The pipeline includes:
✔ Feature Importance Analysis using SHAP
✔ Hyperparameter Optimization using Optuna
✔ Stacking Classifier with Stratified K-Fold for better generalization
✔ Threshold Optimization using Precision-Recall Curve

Feature Importance (SHAP)
We use SHAP (SHapley Additive Explanations) to determine the most influential features affecting hospitalization.

A visualization of the Top 15 SHAP Features is generated for interpretability.

2️⃣ Feature Selection (Optuna)
Optuna dynamically selects the optimal percentage of features based on SHAP importance.

The best subset of features is determined through cross-validation.

3️⃣ Model Training (Stacking Classifier)
Base Models:

XGBoost: Gradient boosting for structured data

LightGBM: Faster and optimized gradient boosting

Meta Model:

Another XGBoost model trained on base model outputs

Stratified K-Fold Cross-Validation ensures balanced class distribution.

4️⃣ Threshold Optimization
Instead of using a default 0.5 threshold, we optimize it using the Precision-Recall Curve to improve F1-score.

Results & Evaluation
✅ Performance Metrics:
Validation F1-Score: ~0.91

Test F1-Score: ~0.76 - 0.78

Optimized Threshold: Determined dynamically

📊 Confusion Matrix & Classification Report
The model outputs a classification report and confusion matrix visualization after testing.

Key Takeaways
✅ SHAP-based Feature Selection improves model interpretability
✅ Optuna Optimization ensures dynamic feature selection & best hyperparameters
✅ Stacking Classifier enhances prediction accuracy
✅ Threshold Optimization helps handle imbalanced data better
