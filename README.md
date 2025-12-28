# Coding-Week-ML-Task

## 🧠 Dataset Description




- **Target Variable**: `Crowd_Energy` (range: 0–100)
- **Venues**:
  - `V_Alpha` – Converted monastery (noise-sensitive)
  - `V_Beta` – Gothic nightclub (time-dependent behavior)
  - `V_Gamma` – Exclusive venue (price sensitivity suspected)
  - `V_Delta` – Mosh pit (crowd-driven energy)

### Key Data Issues
- Mixed currencies (`$, £, €`)
- Invalid values (negative prices, extreme outliers)
- Inconsistent date formats
- Sensor failures (`NaN`, zeros)
- Potential data leakage from post-show variables

---

## 🧹 Data Cleaning & Preprocessing

The following steps were performed:
- Currency conversion to USD
- Removal or correction of impossible outliers
- Missing value imputation using robust statistics
- Encoding of categorical variables with unseen-category handling
- Elimination of data leakage features

---

## 📊 Exploratory Data Analysis (EDA)

EDA was used to:
- Test hypotheses from the lead singer’s notes (CHECK NOTEBOOOK FOR ANS)
- Analyze venue-specific behavior
- Study the effect of crowd size, volume, timing, and pricing
- Identify nonlinear relationships and interactions

Visualizations include:
- Distribution plots
- Scatter plots segmented by venue
- Time-based trend analysis
- lmplots

---

## 🛠 Feature Engineering

Examples of engineered features:
- weekend_flag
- Time_Slot
- categorical encodings
- droping uneccesary columns

---

## 🤖 Model Training & Hyperparameter Tuning

### Models Explored
- Polynomial Regression
- SVR
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor
- XGBoost 


### Tuning Strategy
-  `RandomizedSearchCV`
- 5-fold cross-validation
- Evaluation metric: **RMSE**
- Comparison between default and tuned models

The final model was selected based on validation performance and generalization ability.

---

## 📈 Model Evaluation

Performance was evaluated using:
- RMSE
- R² Score
- Predicted vs Actual plots

The selected model shows strong generalization and robustness to noisy data.


## 📦 Deliverables

- `analysis_notebook.ipynb`
- `predictions.csv`
- `readme.md`

---

## ⚠ Important Notes

- Lead singer’s notes are **not treated as ground truth**
- No test data leakage was introduced
- The pipeline handles unseen categories safely
- All steps are reproducible

 


 A SMALL EFFORT FROM A COMPLETE BEGINNER
