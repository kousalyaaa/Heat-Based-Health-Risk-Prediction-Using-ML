# Spatio-Temporal Heat Health Forecasting System for Tamil Nadu Using Machine Learning

## Overview

The Spatio-Temporal Heat Health Forecasting System is a Machine Learning-based application developed to predict district-level heat-related health risks across Tamil Nadu. The system combines historical climate data, real-time weather information, and predictive analytics to forecast temperature, humidity, and heat stress levels, enabling early warning and preventive decision-making.

The project focuses on identifying potential heatwave conditions and classifying health risks to support public health authorities, disaster management agencies, and citizens.

---

## Problem Statement

Heatwaves are becoming increasingly frequent due to climate change and pose serious threats to public health. Existing weather forecasting systems provide meteorological information but do not directly assess heat-related health risks. Furthermore, most forecasting systems lack district-level analysis and health-oriented risk categorization.

This project addresses these challenges by forecasting weather conditions and translating them into actionable heat-health risk levels.

---

## Objectives

* Predict future temperature and humidity levels.
* Calculate Heat Index (Feels-Like Temperature).
* Classify districts into Low, Moderate, and High heat-risk categories.
* Generate district-level heat-health alerts.
* Provide an interactive visualization dashboard.
* Support climate adaptation and public health planning.

---

## Dataset Sources

### NASA POWER Dataset

Used for collecting historical weather data including:

* Temperature
* Relative Humidity
* Solar Radiation
* Wind Speed

### Open-Meteo API

Used for obtaining:

* Real-time weather information
* Current temperature
* Current humidity

---

## Technologies Used

| Category                | Technology            |
| ----------------------- | --------------------- |
| Programming Language    | Python                |
| Machine Learning        | Scikit-Learn, XGBoost |
| Data Processing         | Pandas, NumPy         |
| Model Serialization     | Joblib                |
| Visualization           | Plotly                |
| Web Framework           | Streamlit             |
| Development Environment | Visual Studio Code    |
| Containerization        | Docker                |

---

## Machine Learning Algorithms

### Random Forest Regressor

Random Forest is an ensemble learning algorithm that combines multiple decision trees to improve prediction performance.

**Purpose**

* Baseline forecasting model.
* Prediction of weather parameters.
* Performance comparison with XGBoost.

**Accuracy**

* 82.85%

---

### XGBoost Regressor

XGBoost (Extreme Gradient Boosting) is an advanced ensemble learning algorithm that improves model accuracy through gradient boosting.

**Purpose**

* Forecast future temperature values.
* Forecast future humidity levels.
* Generate final district-level heat risk predictions.

**Advantages**

* High prediction accuracy.
* Efficient handling of non-linear weather patterns.
* Faster training and inference.

**Accuracy**

* 83.20%

**Selected as Final Model**

* Achieved the highest prediction accuracy among evaluated models.

---

## Heat Index Calculation

The Heat Index represents the perceived temperature experienced by humans by combining temperature and humidity values.

### Risk Classification

| Heat Index (°C) | Risk Level    |
| --------------- | ------------- |
| Below 32°C      | Low Risk      |
| 32°C – 35°C     | Moderate Risk |
| Above 35°C      | High Risk     |

---

## System Workflow

1. Collect historical weather data.
2. Fetch real-time weather information.
3. Preprocess and clean datasets.
4. Train Machine Learning models.
5. Predict future temperature and humidity.
6. Calculate Heat Index values.
7. Classify heat-health risk levels.
8. Display results through Streamlit dashboard.

---

## Key Features

* District-wise forecasting for all 38 districts of Tamil Nadu.
* Real-time weather data integration.
* Machine Learning-based prediction engine.
* Heat Index computation.
* Automated heat risk classification.
* Interactive dashboard using Streamlit and Plotly.
* Early warning alert generation.
* Comparison of Random Forest and XGBoost performance.

---

## Project Structure

```text
Heat-Based-Health-Risk-Prediction-Using-ML/
│
├── app.py
├── train_models.py
├── train_xgboost.py
├── test_prediction.py
├── nasa_data_download.py
├── requirements.txt
├── Dockerfile
├── .gitignore
├── data/
└── models_xgb/
```

---

## Installation

### Clone Repository

```bash
git clone https://github.com/kousalyaaa/Heat-Based-Health-Risk-Prediction-Using-ML.git
```

### Navigate to Project Directory

```bash
cd Heat-Based-Health-Risk-Prediction-Using-ML
```

### Install Dependencies

```bash
pip install -r requirements.txt
```

### Run Application

```bash
streamlit run app.py
```

---

## Results

| Model         | Accuracy |
| ------------- | -------- |
| Random Forest | 82.85%   |
| XGBoost       | 83.20%   |

XGBoost achieved the best performance and was selected as the final forecasting model.

---

## Future Enhancements

* Deep Learning models (LSTM, GRU).
* Mobile application deployment.
* SMS and Email alert system.
* IoT-based weather sensor integration.
* Statewide and nationwide deployment.
* AI-driven personalized health advisories.

---

## Conclusion

The Spatio-Temporal Heat Health Forecasting System successfully integrates climate analytics and Machine Learning to predict heat-related health risks across Tamil Nadu. By combining historical climate records, real-time weather data, XGBoost forecasting, and Heat Index calculations, the system provides accurate district-level risk assessments and supports proactive measures against heatwave-related health impacts.
