# ⏱️ Time Series Forecasting – Emergency Clinic Walk-in Patients

## 📌 Project Overview
This project focuses on building a **forecasting tool** for a walk-in emergency clinic to predict patient inflow one month ahead. Using historical data from **April 2021 – February 2024**, various time-series models were applied to forecast the number of patients expected in **March 2024**.

---

## 🔹 Dataset & Insights
- **Total Days:** 1065  
- **Total Patients:** 48,446  
- **Daily Avg:** 45.48 patients  
- **Min / Max:** 16 (low) → 97 (high)  
- **Weekly Patterns:**  
  - Peak demand: **Mon, Tue, Fri**  
  - Lower demand: **Sat, Sun**  
- **Seasonality:** Repeating weekly & yearly patterns, visible spikes (March 2022 surge: +66.7%).  

---

## 🔹 Models Used
- **Baseline / Simple Approaches:** Naive, Mean, Moving Average, Linear Regression  
- **Advanced Approaches:** Single Exponential Smoothing (SES), Holt Linear, Holt-Winters, ARIMA, SARIMA  

| Model       | MSE    | Notes |
|-------------|--------|-------|
| Naive       | 346.74 | Basic benchmark |
| Moving Avg  | 419.34 | Weak fit |
| Linear Reg. | 287.90 | Reasonable |
| Holt-Winters| 179.40 | ✅ Best performer |
| ARIMA       | 393.48 | Stable but weaker |
| SARIMA      | 450.54 | Higher error |

---

## 🔹 Key Findings
- **Stationarity**: Achieved after first-order differencing (confirmed via ADF & KPSS tests).  
- **Holt-Winters** provided the **lowest MSE (179.40) and MAPE (0.200)** → best model.  
- **Stable demand** expected in March 2024 (~57–60 patients/day).  
- **No sharp peaks or troughs** → resource planning can be optimized.  

---

## 🔹 Business Implications
- Clinics can expect **steady patient volume**.  
- Staff & resources can be allocated efficiently (esp. Mon–Wed peak days).  
- Reliable short-term forecasting ensures better inventory & workforce planning.  

---

## 📑 Presentation
Here’s the detailed project presentation:  
📄 [View Full Presentation (PDF)](doc/Presentation4.pdf)

