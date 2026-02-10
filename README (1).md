# Sneha-102303723

# 🚀 Data Generation using Modelling and Simulation for Machine Learning

## 📌 Overview

A synthetic dataset was generated using **SimPy discrete-event simulation** of a queue system and used to compare multiple Machine Learning models for predicting **average waiting time**.

---

## 🧪 Methodology

1. **🛠 Simulator:** SimPy was used to model a multi-server queue with random arrivals and service times.

2. **📊 Parameters & Bounds →**

   * arrival_rate: 1–10
   * service_time: 1–8
   * servers: 1–5

3. **🗂 Data Generation →**

   * Random parameters were generated
   * Passed to simulator
   * Output metrics recorded
   * Process repeated **1000 times** to create dataset

4. **🤖 ML Pipeline →**

   * Features: arrival_rate, service_time, servers, customers
   * Target: avg_wait
   * 80–20 train–test split
   * Evaluated using MAE, RMSE, R²

---

## 📈 Results

### 🧾 Model Comparison

| Model         | MAE  | RMSE  | R²        |
| ------------- | ---- | ----- | --------- |
| Random Forest | 4.94 | 6.58  | **0.917** |
| XGBoost       | 5.68 | 7.53  | 0.892     |
| KNN           | 5.89 | 8.09  | 0.875     |
| Decision Tree | 6.66 | 9.21  | 0.838     |
| MLP           | 7.07 | 9.29  | 0.835     |
| SVR           | 7.67 | 11.96 | 0.727     |
| Linear Reg.   | 9.92 | 12.75 | 0.690     |




### 📊 Graph Insights

➡ The R² comparison graph shows **Random Forest** as the best model, followed by XGBoost.
➡ Linear Regression and SVR performed poorly, indicating a **non-linear relationship** between queue parameters and waiting time.
➡ Ensemble models captured the complex behavior more effectively.



<img width="839" height="665" alt="image" src="https://github.com/user-attachments/assets/3fab8603-ff7c-4855-83f1-c994d6f129cd" />


---


### 🧰 Tools

Python • SimPy • Scikit-Learn • XGBoost • Colab



## Conclusion

- SimPy successfully generated realistic simulation data
- Dataset was suitable for supervised ML
- **Random Forest** emerged as the most accurate predictor
- Approach can be extended to real-world queue systems

---


