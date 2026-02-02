 🩺 Health Monitoring and Anomaly Detection for Elderly Patients

**DSC 291 – Ubiquitous Computing**

---

## 📌 Overview

With a rapidly growing elderly population living independently, there is an increasing need for **proactive health monitoring systems**. Falls and physiological anomalies often go undetected or unreported, while most existing systems remain reactive and rule-based.

This project demonstrates the feasibility of a **machine learning–driven ubiquitous monitoring system** that combines:

* 🧍 Fall detection using wearable motion data
* ❤️ Physiological anomaly detection
* 📊 Interpretable caregiver visualization interface

The system bridges **ubiquitous sensing, machine learning, and user-facing deployment principles**.

---

## 🚨 Problem Statement

* Falls and health anomalies frequently go undetected
* Sensor streams are noisy and high-dimensional
* Systems must handle inter-subject variability
* Need for automated, reliable caregiver alerts
* Must align with mobile & ubiquitous computing principles

---

## 🎯 Project Objectives

* Build an ML-based monitoring system for elderly care
* Detect falls using wearable motion data
* Monitor physiological signals for abnormal patterns
* Provide an interpretable caregiver dashboard
* Design architecture scalable to real-time deployment

---

## 🏗️ System Architecture

**Pipeline Overview:**

Wearable Sensors → Feature Extraction → ML Models → Alert Prediction → Caregiver Interface

### Components:

* Wearable motion + vital sensors
* Signal processing & feature engineering
* Fall detection model
* Health anomaly prediction model
* Visualization dashboard

---

## 📊 Datasets

### 1️⃣ MobiFall Dataset

* Smartphone-based accelerometer recordings
* Simulated falls and daily activities
* Used exclusively for fall detection

### 2️⃣ AI for Elderly Care & Support (Kaggle)

* Physiological monitoring data
* Heart rate
* Glucose
* SpO₂
* Alerts & reminders
* Used for health monitoring & alert prediction

---

## ⚙️ Data Processing & Feature Engineering

### Motion Data (MobiFall)

* Acceleration magnitude:
  [
  \sqrt{x^2 + y^2 + z^2}
  ]
* Statistical features:

  * Mean
  * Standard deviation
  * Max / Min
  * Range
  * Signal energy
  * Sequence length

### Physiological Data

* Temporal features (hour of day)
* Binary encoding of alerts
* Data-driven threshold learning

---

## 🤖 Model Design

### 🧍 Fall Detection Model

* Random Forest Classifier
* File-level classification
* Subject-aware train/test split
* Handles:

  * Inter-subject variability
  * Non-linear feature interactions
* PCA used for interpretability

---

### ❤️ Health Alert Prediction Model

* Logistic Regression
* Predicts probability of health anomaly
* Input features:

  * Heart rate
  * Glucose
  * SpO₂
  * Time-of-day
* Interpretable coefficients for caregiver trust

---

## 📈 Evaluation Strategy

* Subject-level splitting (avoids data leakage)
* Metrics used:

  * Accuracy
  * Precision
  * Recall
  * F1-score
  * Confusion Matrix
* PCA visualization for feature separability

---

## 🖥️ Visualization Interface

A caregiver-facing dashboard that provides:

* Health trend visualization
* Alert classification
* Fall detection status
* Model confidence outputs

Designed with usability and interpretability in mind.

---

## 💪 System Strengths

* Modular & extensible architecture
* Uses ubiquitous sensor data
* Interpretable ML models
* Deployable pipeline
* Bridges sensing, ML, and UI

---

## ⚠️ Limitations

* Offline datasets (no real-time streaming)
* Simulated falls (not real elderly falls)
* Simplified physiological labeling
* Not a clinical diagnostic tool

---

## 🚀 Future Work

* Real-time sensor streaming
* Multi-modal temporal models (LSTM / Transformers)
* Integration with real wearable devices
* Clinically validated alert thresholds

---

## 🧠 Key Contribution

This project demonstrates the feasibility of:

* Combining motion safety + physiological monitoring
* Applying interpretable ML to ubiquitous sensing data
* Building a foundation for real-world elderly monitoring deployment

---

## 🛠️ Tech Stack

* Python
* Scikit-learn
* NumPy / Pandas
* Matplotlib / Seaborn
* PCA for visualization

---

## 📂 Project Structure

```
elderly-health-monitoring/
│
├── data/
├── src/
├── notebooks/
├── models/
├── dashboard/
├── requirements.txt
└── README.md
```
