# 🌧️ RainDistill: Real-Time Bias Correction of Ensemble Rainfall Forecasts

RainDistill refines ensemble rainfall forecasts through real-time machine learning bias correction.  
Powered by knowledge distillation (LSTM → XGBoost), it transforms noisy, underestimated forecasts into reliable rainfall predictions — even in extreme events — using **only forecast inputs at inference time**.

---

## 🔍 Overview

**RainDistill** is a real-time, deployable ML framework for correcting systematic bias in ensemble rainfall forecasts, particularly in the Indian monsoon context.

Using a **teacher–student model** design:
- The **Teacher (LSTM)** learns complex correction patterns using both forecast and observed-derived features.
- The **Student (XGBoost)** mimics the teacher using only forecast-time inputs, enabling **real-time correction** without observed rainfall.

---

## ⭐ Key Features

- ✅ **Real-time bias correction** for ensemble rainfall forecasts  
- 🧠 **Knowledge distillation** (Teacher: LSTM, Student: XGBoost)  
- ⏱️ **Forecast-only inputs at inference** (no observed rainfall needed)  
- 📊 Evaluation across **entire distribution & extremes** (10th/90th percentiles)  
- 🗺️ **Spatial & temporal analysis**: maps, NSE skill scores, time series  
- 🔄 Easily extendable to other regions or forecast systems  

---

## 🧪 Methodology

### 🔷 1. Teacher Model (LSTM-based)
- **Trained per lead time** (e.g., 1-day, 2-day ahead)
- **Inputs**:  
  - Forecast ensemble features  
  - Observed-derived rainfall features (e.g., smoothed IMD rainfall)  
- **Target**: Residuals = (Ensemble Mean − Observed Rainfall)
- **Prediction**  


### 🔶 2. Student Model (XGBoost)
- **Inputs**: Forecast-only features  
- **Target**: Teacher-predicted residuals  
- **Prediction (real-time)** 

---

### 📬 Contact

For any queries, feedback, or collaboration ideas, feel free to reach out:

- 📧 Email: [shivanshshukla@gmail.com](mailto:shivanshs1707@gmail.com)
- 👤 Author: Shivansh Shukla  
  SRIP Intern, IIT Gandhinagar

---
