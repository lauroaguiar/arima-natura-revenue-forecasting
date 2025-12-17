# 📈 Natura & Co. Revenue Forecasting: A Time Series Analysis

> **Econometric analysis of the stochastic process of Natura & Co's gross revenue using SARIMA models.**

[![R](https://img.shields.io/badge/Made_with-R-blue?style=for-the-badge&logo=R)](https://www.r-project.org/)
[![Methodology](https://img.shields.io/badge/Method-Box--Jenkins-orange?style=for-the-badge)]()
[![Status](https://img.shields.io/badge/Status-Educational-yellow?style=for-the-badge)]()

## 📄 Project Overview

This repository contains the coursework for **Econometrics II**, focusing on Time Series Analysis. The objective was to model the stochastic process of **Natura & Co's Gross Revenue** (quarterly data) to forecast future performance.

Using the Box-Jenkins methodology, we identified seasonality, tested for stationarity, and estimated a Seasonal ARIMA (SARIMA) model to predict revenue for the upcoming quarters.

### 📂 Repository Contents

| File | Description |
|------|-------------|
| **[`arima-natura-revenue-analysis.Rmd`](arima-natura-revenue-analysis.Rmd)** | The **R source code** containing the full data pipeline: data loading, stationarity tests (ADF), model selection (AIC/BIC), and forecasting. |
| **[`Final Report.pdf`](Time%20Series%20Analysis%20-%20Identificação%20de%20processo%20estocástico%20da%20Receita%20Bruta%20da%20Natura&Co.pdf)** | The **final academic report** (in Portuguese) presenting the theoretical framework, visual decomposition, and detailed interpretation of the results. |

---

## 🛠️ Methodology & Approach

The analysis followed a rigorous statistical pipeline:

1.  **Exploratory Data Analysis (EDA):** Visual inspection of the series revealed a strong trend and quarterly seasonality.
2.  **Stationarity Tests:** Applied the **Augmented Dickey-Fuller (ADF)** test and analyzed Autocorrelation Functions (ACF/PACF).
3.  **Transformations:** Performed seasonal and non-seasonal differentiation to stabilize the mean and variance.
4.  **Model Selection:** Tested multiple SARIMA configurations, selecting the best fit based on **AIC/BIC criteria**.
5.  **Validation:** Residual analysis using Ljung-Box and normality tests.

---

## 📊 Key Findings

* **Seasonality:** The series showed a clear seasonal pattern, with revenue peaks typically occurring in Q4.
* **Selected Model:** The model that best minimized information criteria was the **SARIMA(1,1,1)(1,1,1)[4]**.
* **Forecast:** The model successfully generated point forecasts and confidence intervals (80% and 95%) for the subsequent year (4 quarters).

### ⚠️ Model Limitations
* *Normality of Residuals:* Although the model handled autocorrelation well, the residuals did not follow a perfectly normal distribution (p-value < 0.05). This limitation is noted in the conclusion, and the forecast is presented for educational purposes within the scope of the course.

---

## 📦 Dependencies

To run the analysis locally, ensure you have the following R libraries installed:

```r
install.packages(c("readxl", "tseries", "forecast", "dygraphs", "ggplot2"))
```

## 👥 Authors

* **Lauro Aguiar**
* **José Pedro**

---
This project is academic and educational in nature, developed within the scope of the Econometrics II course.
