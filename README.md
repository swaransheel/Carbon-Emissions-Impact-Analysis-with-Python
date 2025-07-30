# 🌍 Analyzing the Impact of Carbon Emissions

This project explores the relationship between **CO₂ concentrations** and **temperature changes** over time using statistical and visual analysis. It aims to understand if rising carbon emissions are statistically correlated with or predictive of temperature change.

---

## 📁 Table of Contents

- [Overview](#overview)
- [Dataset Description](#dataset-description)
- [Key Objectives](#key-objectives)
- [Data Preprocessing](#data-preprocessing)
- [Visual Analysis](#visual-analysis)
- [Statistical Analysis](#statistical-analysis)
- [Modeling with Regression](#modeling-with-regression)
- [Conclusion](#conclusion)
- [Installation & Requirements](#installation--requirements)
- [How to Run](#how-to-run)
- [Results (Graphs)](#results-graphs)

---

## 🧠 Overview

In this project, we:
- Analyze temperature anomalies and atmospheric CO₂ levels over time.
- Visualize temporal trends and seasonal variations.
- Perform correlation and causality analysis.
- Build regression models using lagged CO₂ data to predict temperature change.

---

## 📊 Dataset Description

- `temperature_data`: Contains temperature anomalies labeled by year (e.g., `F1990`, `F1991`, ...).
- `carbon_data`: Contains columns like `Date` and `Value` representing CO₂ concentration per time point.

---

## 🎯 Key Objectives

- 📈 Visualize trends in temperature and CO₂ levels.
- 📊 Compute correlation coefficients (Pearson & Spearman).
- 🔁 Perform Granger causality test to analyze predictive influence.
- 🔍 Build a lagged regression model for temperature change.

---

## 🛠️ Data Preprocessing

- Extracted year and month from date strings.
- Cleaned temperature columns (`Fxxxx`) and matched them with CO₂ years.
- Created lagged versions of CO₂ for regression modeling.

---

## 📉 Visual Analysis

### 1. Time-Series Plot of Temperature and CO₂

![Time Series of Temperature and CO2](images/timeseries_plot.png)

---

### 2. Correlation Heatmap

![Correlation Heatmap](images/correlation_heatmap.png)

---

### 3. CO₂ vs Temperature Scatter Plot

![Scatter Plot](images/scatter_plot.png)

---

### 4. Trend Lines for Temperature and CO₂

![Trend Lines](images/trend_lines.png)

---

### 5. Seasonal Variation in CO₂

![Seasonal CO2 Variation](images/seasonal_variation.png)

---

## 📊 Statistical Analysis

- **Pearson Correlation**: Measures linear correlation.
- **Spearman Correlation**: Measures monotonic relationship.
- **Granger Causality Test**:
  - Determines if changes in CO₂ help predict future changes in temperature.
  - Conducted for multiple lags (1 to 3 years).

---

### 📌 Sample Results:
```
Pearson Correlation:  0.89
Spearman Correlation:  0.85
Granger P-values:  {'Lag1': 0.0142, 'Lag2': 0.0325, 'Lag3': 0.0871}
```

---

## 📈 Modeling with Regression

- Used multiple linear regression to model `Temperature Change` based on:
  - CO₂ at current year
  - CO₂ from 1, 2, and 3 previous years (lags)
- Built with `statsmodels.OLS` for interpretability.

---

### 📄 Regression Summary Output

![Regression Output](images/regression_summary.png)

---

## ✅ Conclusion

- CO₂ and temperature are **highly correlated**.
- Granger causality suggests CO₂ **predicts** temperature changes.
- Lagged regression models show a measurable statistical relationship.

---

## 🧩 Installation & Requirements

Make sure to install the required libraries:

```bash
pip install pandas numpy plotly scipy statsmodels
```

---

## ▶️ How to Run

1. Clone the repo or download the notebook.
2. Run the notebook `Analyzing_the_Impact_of_Carbon_Emissions.ipynb`.
3. Insert your own data or visualize using provided datasets.

---

## 📷 Results (Graphs)

All graphs will be saved in the `/images/` folder.

---

## 📌 Author

- **Your Name Here**
- [LinkedIn/GitHub (optional)]

---
