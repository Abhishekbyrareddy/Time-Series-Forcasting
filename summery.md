# 🧠 Time Series Forecasting of PJM Energy Demand using XGBoost

## 📌 Project Overview

This project predicts **hourly electricity demand (in megawatts)** for the PJM region between **2002 and 2018**.  
Using **XGBoost Regressor**, the model learns from historical time-series data to forecast future energy usage.

The project demonstrates the use of **machine learning for time-series forecasting** by:
- Engineering meaningful **calendar-based features** (hour, day, month, etc.)
- Training a model using **chronological data splits**
- Evaluating results with RMSE and visual analysis

---

## ⚙️ Modeling Details

| Parameter | Value |
|------------|-------|
| Model | XGBoost Regressor |
| Learning Rate | 0.01 |
| Max Depth | 3 |
| Estimators | 1000 |
| Early Stopping Rounds | 50 |
| Evaluation Metric | RMSE (Root Mean Squared Error) |

The model was trained on **80% of the data** and tested on the remaining **20%** (chronological split).

---

## 📊 Results Summary

| Metric | Value |
|--------|--------|
| **Test RMSE** | **676.09 MW** |
| **Train RMSE** | ~508 MW |
| **Test Period** | 2015 – 2018 |
| **Total Data Points** | 143,206 (Hourly records) |

**Worst predicted days:**  
Mostly during **winter (Dec–Feb)** — likely due to sudden temperature changes and irregular holiday energy spikes.

---

## 🔍 Key Insights

- **Hour of day** is the most important feature — energy demand peaks during daytime and drops at night.  
- **Month** and **Quarter** show strong seasonal effects — high usage in summer and winter.  
- The model captures both **daily** and **seasonal** patterns effectively.  
- Errors increase during **unusual conditions** (extreme weather or holidays).

---

## 📈 Visual Highlights

| Plot | Insight |
|------|----------|
| **Actual vs Predicted (Full Test)** | Predictions closely follow real demand patterns |
| **Zoomed Week Plot** | Accurately captures hourly ups and downs |
| **Feature Importance** | “Hour”, “Quarter”, and “Month” dominate |
| **Hourly Boxplot** | Demand peaks during day, dips at night |
| **Monthly Boxplot** | Demand highest in winter and summer |

---

## 💡 Future Improvements

- Add **temperature, humidity, and holiday data** as external features  
- Try **LSTM** or **Facebook Prophet** for sequence-based forecasting  
- Deploy as a **Streamlit dashboard** for interactive predictions  

---

## 👨‍💻 Author

**Abhishek Byrareddy**    
📧 [abhishekreddy268@gmail.com]  

