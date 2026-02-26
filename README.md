# EV Battery Health & Sustainability Intelligence

## Project Overview

This project presents an AI-driven predictive battery analytics framework designed to enhance lifecycle management of lithium-ion batteries used in Electric Vehicles (EVs).

Unlike traditional rule-based Battery Management Systems (BMS), this system predicts:

- State of Health (SoH)
- Remaining Useful Life (RUL)
- Early degradation anomalies
- Second-life reuse feasibility

The system transforms reactive battery monitoring into a predictive and intelligent analytics platform.

---

##  Problem Statement

Conventional Battery Management Systems:
- Monitor voltage & temperature only
- Detect failures after they occur
- Do not predict long-term degradation
- Do not estimate Remaining Useful Life (RUL)
- Do not support intelligent reuse decisions

There is a need for an AI-based system that can forecast battery degradation, reduce unexpected failures, and support sustainable lifecycle management.

---

##  Proposed Solution

An AI-powered predictive battery analytics system that:

- Uses NASA battery telemetry dataset (1.33M+ records)
- Integrates 1,80,000 synthetic EV fleet records
- Applies advanced feature engineering
- Uses XGBoost regression for nonlinear degradation modeling
- Implements GroupShuffleSplit to prevent data leakage
- Supports real-time streaming simulation
- Includes anomaly detection module
- Provides automated reuse decision engine
- Deploys predictions through Streamlit dashboard

---

##  System Architecture (9-Phase Pipeline)

1. NASA Data Ingestion  
2. Synthetic EV Data Generation  
3. Unified Dataset Creation  
4. Feature Engineering  
5. XGBoost Modeling  
6. Real-Time Streaming Simulation  
7. Anomaly Detection Module  
8. Reuse Decision Engine  
9. Dashboard Visualization  

---

##  Technologies Used

- Python 3.x  
- NumPy  
- Pandas  
- Matplotlib & Seaborn  
- Scikit-learn  
- XGBoost  
- Streamlit  
- Joblib / Pickle  

---

##  Feature Engineering Highlights

Advanced engineered features include:

- Rolling Average Voltage  
- Temperature Variance  
- Depth of Discharge (DoD)  
- Voltage Degradation Slope  
- Internal Resistance Estimation  
- Cycle Count Progression  

These features capture nonlinear battery degradation physics.

---

##  Model Performance

Evaluation Metrics Used:
- MAE (Mean Absolute Error)
- RMSE (Root Mean Squared Error)
- R² Score

✔ Achieved high R² Score (~0.96)  
✔ Low MAE & RMSE  
✔ Handles nonlinear degradation patterns  
✔ Deployment-ready model saved as `battery_model.pkl`

---

##  Real-Time Streaming Simulation

- Simulates live battery sensor data
- Predicts SoH & RUL dynamically
- Mimics real IoT deployment environment
- Enables proactive maintenance planning

---

##  Anomaly Detection Module

Detects:
- Sudden voltage drops
- Temperature spikes
- Rapid internal resistance growth
- Abnormal degradation patterns

Uses:
- Threshold-based detection
- Statistical deviation methods
- Z-score analysis

---

##  Reuse Decision Engine

Automated second-life recommendations:

- SoH > 80% → Continue EV use
- 60–80% → Secondary vehicle use
- 40–60% → Stationary storage
- < 40% → Recycling

Promotes circular economy & sustainability.

---

## 📊 Dashboard (Streamlit)

Interactive dashboard provides:

- Live SoH & RUL prediction
- Degradation trend visualization
- Anomaly alerts
- Reuse recommendations
- Fleet-level monitoring

---

##  Strengths

- Large-scale real + synthetic dataset integration
- Nonlinear modeling using XGBoost
- Data leakage prevention (GroupShuffleSplit)
- Real-time capability
- Intelligent reuse engine
- Scalable architecture

---

##  Future Enhancements

- LSTM-based time-series modeling
- IoT hardware integration
- Cloud deployment
- Mobile application
- Reinforcement learning optimization
