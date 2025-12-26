# PowerPulse – Household Energy Consumption Forecasting

## Overview
This project focuses on predicting **Global Active Power** consumption using historical household energy usage data. Multiple regression models were trained and evaluated to determine the best-performing approach.

---

## Dataset
- Total records: 1.25M+
- Target variable: `Global_active_power`
- Key features include electrical measurements, time-based features, and rolling statistics.

---

## Feature Engineering
- Extracted time-based features: `Hour`, `DayOfWeek`, `Is_Weekend`
- Created rolling features: `Rolling_mean_1h`, `Rolling_std_1h`
- Removed leakage features: `Total_sub_metering`, `Unmetered_power`
- Applied feature scaling where required

---

## Models Implemented
- Linear Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Neural Network (MLP Regressor)

---

## Model Performance

| Model | MSE | MAE | R² |
|------|-----|-----|----|
| Linear Regression | 0.2055 | 0.2862 | 0.8272 |
| Random Forest | 0.1384 | 0.2052 | 0.8837 |
| Gradient Boosting | 0.1508 | 0.2230 | 0.8732 |
| Neural Network | **0.1127** | **0.1805** | **0.9052** |

---

## Visualizations
- Actual vs Predicted plots for all models
- Neural Network showed the closest alignment to the ideal prediction line

---

## Tools & Technologies
- Python
- Pandas, NumPy
- Scikit-learn
- Matplotlib, Seaborn

---

## Conclusion
The Neural Network model achieved the best performance, effectively capturing complex patterns in household energy consumption.
