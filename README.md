# Student Performance Prediction (Machine Learning)

This project develops regression models to predict final student grades (G3) using demographic, behavioral, and academic features from a public dataset.

The primary objective is to evaluate predictive performance under two real-world intervention scenarios:

1. **With prior-term grades (G1, G2)**  
   High predictive accuracy, usable later in the academic year.

2. **Without prior-term grades**  
   Lower accuracy, but useful for early risk detection and intervention planning.

---

## Dataset

- Source: UCI Machine Learning Repository  
- 395 student records  
- 35 features  
- Target variable: Final grade (G3)  
- 80/20 train-test split  

---

## Modeling Approach

- Feature engineering with custom transformer
- ColumnTransformer pipelines for:
  - Numeric features
  - Categorical (One-Hot Encoding)
  - Ordinal encoding
- Cross-validation (3-fold)
- Grid search hyperparameter tuning (SVR)

---

## Models Evaluated

- Linear Regression
- Lasso Regression
- Support Vector Regression (SVR)

---

## Test Set Performance

### With Prior-Term Grades
- **RMSE:** 2.142  
- **R²:** 0.776  

### Without Prior-Term Grades
- **RMSE:** 4.154  
- **R²:** 0.158  

---

## Key Insights

- Prior-term grades dominate predictive power.
- Early-year prediction is substantially more difficult.
- Feature engineering and structured pipelines significantly impacted model performance.
- Even lower-accuracy early models can be operationally valuable for identifying at-risk students.

---

## Repository Structure

notebooks/student_performance_ml_portfolio.ipynb

reports/student_performance_executive_summary.pdf

## Business Implications

- Use grade-inclusive model for mid-year intervention targeting.
- Use early-warning model to flag high-risk students before term grades are available.
- Focus interventions on attendance and study-time support.
