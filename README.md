# ⚡ Time Series Forecasting of PJM Energy Demand (XGBoost)

This project predicts hourly electricity demand (in megawatts) for the **PJM region (2002–2018)** using **machine learning (XGBoost Regressor)**.  
The goal is to learn daily and seasonal patterns in energy usage to improve planning and capacity forecasting.

---

## 🧠 Project Overview

- **Model:** XGBoost Regressor  
- **Dataset:** PJM Hourly Energy Demand (Forcasting.csv)  
- **Period Covered:** 2002 – 2018  
- **Error Metric:** RMSE = **676.09 MW**  
- **Language:** Python  
- **Tools:** Pandas, NumPy, XGBoost, Seaborn, Matplotlib, Scikit-learn  

---

## 🧩 Key Features

- Time-based feature engineering (hour, day of week, month, quarter, year)
- Chronological train/test split to prevent data leakage
- Early stopping to avoid overfitting
- Visualization of feature importance, predictions, and patterns
- Error analysis to detect high-error days

---

## 📊 Results Summary

- **RMSE on Test Set:** 676.09 MW  
- **Worst Predicted Days:** Mostly winter months (Dec–Feb) due to extreme demand spikes  
- **Feature Importance:**  
  - Hour → most influential  
  - Quarter, Month → reflect seasonal trends  
  - Day of Week → captures behavioral patterns  

---

## 📈 Visual Insights

| Plot | Description |
|------|--------------|
| **Actual vs Predicted (Test Overlay)** | Model predictions follow actual demand trends closely |
| **Last 7 Days Zoom** | Model captures daily demand peaks and night dips accurately |
| **Feature Importance** | Hour, Quarter, and Month are strongest predictors |
| **Hourly Boxplot** | Demand rises during the day, drops at night |
| **Monthly Boxplot** | Demand peaks in winter and summer |

