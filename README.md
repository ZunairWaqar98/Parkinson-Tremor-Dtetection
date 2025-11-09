# Parkinson's Tremor Detection and Classification

This project focuses on detecting and classifying Parkinson's Disease (PD) hand tremors using **IMU-based time-series data** and machine learning. The system is entirely software-based, designed to preprocess data, extract features, train ML models, and classify tremor types for research and analytical purposes.

---

## Table of Contents

1.Overview
2. Dataset
3.remor Types
4. Features and Preprocessing
5. Machine Learning Models](#machine-learning-models

## Overview

Parkinson's Disease tremors can be categorized and analyzed using wrist-worn IMU sensors (accelerometer and gyroscope). This software pipeline allows:

- Loading and cleaning raw IMU data.
- Feature extraction in both time and frequency domains.
- Classification of tremors into clinically-inspired categories using machine learning.
- Visualizing tremor patterns for further analysis.

## Dataset

- Source: Open-access IMU-based Parkinson’s datasets (e.g., [Parkinson@Home](https://www.kaggle.com/datasets) or custom-collected datasets).
- Format: CSV files with columns:
  - `time` – timestamp
  - `acc_x`, `acc_y`, `acc_z` – accelerometer readings
  - `gyro_x`, `gyro_y`, `gyro_z` – gyroscope readings
  - Optional labels: `tremor_type` (rest, action, mixed)


## Tremor Types

The project follows clinically-inspired tremor classification:

- **Type I (Rest Tremor)** – occurs at rest, 4–7 Hz.
- **Type II (Mixed Tremor)** – present at rest and during movement, 4–7 Hz.
  - II-R: Re-emergent tremor
  - II-C: Continuous tremor
- **Type III (Action Tremor)** – occurs during movement, ~8–12 Hz.
- **Type IV (Mixed, Rare)** – rest and action tremors at different frequencies.

## Features and Preprocessing

**Preprocessing Steps:**

1. Handle missing values and outliers.
2. Normalize sensor readings.
3. Segment time-series data into fixed windows.
4. Extract features:
   - Time-domain: mean, standard deviation, variance, RMS.
   - Frequency-domain: FFT coefficients, dominant frequency, power spectral density.


## Machine Learning Models

- **Random Forest Classifier** – primary model for tremor classification.
- Optionally, can use:
  - Support Vector Machines (SVM)
  - Gradient Boosting
  - K-Nearest Neighbors (KNN)

**Evaluation Metrics:**

- Accuracy
- Precision, Recall, F1-score
- Confusion Matrix
- Cross-validation for robustness

