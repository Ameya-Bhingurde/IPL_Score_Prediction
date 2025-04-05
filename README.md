# 🏏 IPL First Innings Score Predictor

A regression-based machine learning pipeline to **predict the first innings total** in an IPL match based on early match data.  
This project captures how the momentum of the opening overs — combined with team context — can forecast the final total.

---

## 🔍 Problem Statement

Can the final score of an IPL first innings be predicted using just the first few overs?

This project explores that question using historical IPL data and trains several regression models to make accurate score predictions, even before the innings is over.

---

## 📦 Dataset

- **Source:** Kaggle IPL Dataset (`matches.csv` & `deliveries.csv`)
- Only first innings data used  
- Cleaned for:
  - Missing values
  - Removed discontinued teams (e.g., Gujarat Lions, Kochi Tuskers)
  - Standardized team names

---

## 🎯 Features Used

Seven features were engineered and selected for modeling:

- `batting_team` 
- `bowling_team` 
- `overs`   
- `runs`  
- `wickets` 
- `runs_in_prev_5` 
- `wickets_in_prev_5` 

Categorical variables were one-hot encoded for model compatibility.

---

## 🧠 Modeling

### Models Trained:
- **Linear Regression**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **XGBoost Regressor**

Each model was evaluated using:
- 📉 **Mean Absolute Error (MAE)**
- 🧮 **Mean Squared Error (MSE)**
- 📐 **Root Mean Squared Error (RMSE)**

### 🧪 Evaluation Results:

| Model                    | MAE   | MSE     | RMSE  |
|--------------------------|-------|---------|--------|
| **Linear Regression**    | 12.11 | 236.14  | 15.37 |
| Decision Tree Regressor  | 14.21 | 290.85  | 17.05 |
| Random Forest Regressor  | 13.68 | 275.39  | 16.59 |
| XGBoost Regressor        | 13.44 | 262.00  | 16.18 |

✅ **Linear Regression** was selected as the final model due to its **lowest MAE, MSE, and RMSE** — offering a simple yet accurate solution with minimal overfitting.

---

## 🚀 How to Run

1. Open `DM_PROJECT_IPL (1).ipynb` in Jupyter Notebook or VS Code  
2. Ensure the dataset files (`matches.csv` and `deliveries.csv`) are in the same folder  
3. Run the notebook cells step-by-step to:
   - Clean data  
   - Engineer features  
   - Train & evaluate models  
   - Predict the first innings score

---

## 📚 Learnings

- Explored real-world sports data and regression techniques  
- Compared multiple models using consistent metrics  
- Understood the role of recent form (last 5 overs) in outcome prediction  
- Gained practical experience in feature engineering & model validation

---
**Always curious about what comes next — even before the innings ends. 🎯**
