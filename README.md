# ⚡ Household Electricity Consumption Forecasting

## 📌 Overview

This project focuses on forecasting household electricity consumption using a hybrid deep learning and statistical approach. It combines **State Space Models (SSM)** for structural decomposition with **CNN and BiLSTM** networks to capture complex temporal and non-linear patterns in power usage data.

---

## 🎯 Objectives

* Analyze and preprocess household electricity consumption data
* Capture trend, seasonality, and noise components
* Model non-linear temporal dependencies
* Improve forecasting accuracy using a hybrid architecture

---

## 📊 Dataset

* **Source**: Household Electric Power Consumption Dataset
* **Link**: [Download Dataset](https://www.kaggle.com/datasets/uciml/electric-power-consumption-data-set)

### 📁 Description

* Contains **~2 million records** collected over **47 months (2006–2010)** ([Kaggle][1])
* Sampling rate: **1-minute intervals** ([Kaggle][1])
* Type: **Multivariate Time Series** ([Kaggle][1])

---

### 🧾 Features

* `date`, `time` → timestamp
* `global_active_power` → total household power (kW)
* `global_reactive_power` → reactive power (kW)
* `voltage` → voltage (V)
* `global_intensity` → current intensity (A)
* `sub_metering_1` → kitchen appliances
* `sub_metering_2` → laundry appliances
* `sub_metering_3` → heating & AC

---

### ⚠️ Data Challenges

* ~**1.25% missing values** ([Kaggle][1])
* High-frequency noisy data
* Multiple correlated features
* Strong seasonal and temporal patterns

---

## ⚙️ Project Pipeline

### 1. Data Preprocessing

* Handling missing values
* Converting date-time formats
* Feature scaling
* Time-based aggregation

---

### 2. Exploratory Data Analysis (EDA)

* Trend and seasonality visualization
* Correlation analysis
* Distribution of consumption patterns

---

### 3. Model Architecture

#### 🔹 State Space Model (SSM)

* Decomposes time series into:

  * Trend
  * Seasonality
  * Noise
* Uses **Kalman Filter** for state estimation
* Parameters optimized via **Maximum Likelihood Estimation (MLE)**

---

#### 🔹 CNN (Convolutional Neural Network)

* Extracts **local temporal patterns**
* Captures short-term fluctuations and spikes
* Uses **ReLU activation**

---

#### 🔹 BiLSTM (Bidirectional LSTM)

* Captures **long-term dependencies**
* Processes sequence in both directions
* Uses **tanh and sigmoid activations internally**

---

### 🔗 Hybrid Approach

* SSM → structural decomposition
* CNN → local feature extraction
* BiLSTM → temporal sequence modeling

---

## 🧠 Why This Approach?

| Model                 | Limitation                    |
| --------------------- | ----------------------------- |
| ARIMA                 | Assumes linear relationships  |
| Exponential Smoothing | Cannot model complex patterns |
| SSM                   | Limited non-linear learning   |

### ✅ Hybrid Model Advantage:

* Handles **non-linearity**
* Captures **long + short-term dependencies**
* Improves **forecast accuracy**

---

## 📈 Results

* Hybrid model outperformed traditional models like ARIMA
* Better handling of:

  * Seasonal variations
  * Sudden spikes
* Reduced prediction error (**add your RMSE/MAE here**)

---

## 📏 Evaluation Metrics

* Mean Absolute Error (MAE)
* Root Mean Squared Error (RMSE)
* Mean Absolute Percentage Error (MAPE) *(optional)*

---

## 🧪 Technologies Used

* Python
* NumPy, Pandas
* Matplotlib, Seaborn
* TensorFlow / PyTorch
* Statsmodels

---

## 🔍 Key Learnings

* Handling high-frequency time series data
* Combining statistical + deep learning models
* Understanding temporal dependencies
* Applying Kalman Filtering and MLE

---

## 📌 Future Improvements

* Hyperparameter tuning
* Add external features (weather, holidays)
* Deploy as real-time API
* Experiment with Transformers

---
