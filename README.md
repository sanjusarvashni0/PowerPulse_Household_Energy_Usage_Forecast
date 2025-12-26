PowerPulse Household Energy Consumption Analysis
Project Overview

This project analyzes household energy consumption and predicts Global Active Power using various features like voltage, reactive power, and sub-metering data.
The goal is to identify patterns, build predictive models, and compare performance to select the best model for accurate forecasting.

Dataset

Rows: 1,258,632

Columns: 13

Features:

Global_reactive_power, Voltage

Sub_metering_1, Sub_metering_2, Sub_metering_3

Hour, DayOfWeek, Is_Weekend

Rolling_mean_1h, Rolling_std_1h, Total_sub_metering, Unmetered_power

Target: Global_active_power

Data Cleaning & Feature Engineering

Removed missing values and dropped features causing target leakage (Total_sub_metering, Unmetered_power).

Created additional features:

Hour, DayOfWeek, Is_Weekend

Rolling mean and rolling std over 1 hour

Scaled features for Neural Network.

Tools & Technologies

Programming: Python

Libraries: Pandas, NumPy, Scikit-learn, Matplotlib, Seaborn

Environment: Jupyter Notebook / VS Code

Models Used

Linear Regression – baseline model

Random Forest Regressor – captures non-linear patterns

Gradient Boosting Regressor – sequential ensemble

Neural Network (MLPRegressor) – captures complex non-linear relationships

Model Hyperparameters
Model	Key Parameters
Linear Regression	Default
Random Forest	n_estimators=100, max_depth=10
Gradient Boosting	n_estimators=100, learning_rate=0.1, max_depth=3
Neural Network	hidden_layer_sizes=(64,64), activation='relu', alpha=0.001, max_iter=500
Model Performance
Model	MSE	MAE	R²
Linear Regression	0.2055	0.2862	0.8272
Random Forest	0.1384	0.2052	0.8837
Gradient Boosting	0.1508	0.2230	0.8732
Neural Network	0.1127	0.1805	0.9052

Best Model: Neural Network

Insights

Evening hours have higher energy usage.

Sub_metering_3 contributes most to total active power.

Weekends show slightly lower household consumption.

Conclusion

Neural Network performed best with R² ~0.905.

Random Forest and Gradient Boosting are good alternatives.

Future work: hyperparameter tuning, incorporate external factors like weather or occupancy.