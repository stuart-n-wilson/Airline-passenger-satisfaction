# ✈️ Airline Passenger Satisfaction Analysis & Prediction

A machine learning project that identfies travel class, inflight entertainment, seat comfort and ease of online booking as the most important factors in customer (dis)satisfaction, with predictive machine learning accuracy of **91%**.

---

## Overview

This project explores airline passenger satisfaction through exploratory analysis and machine learning in KNIME. The aim of this project is to identify key factors in a passenger's satisfaction levels and optimise predictive model performance.

---

## Project Structure

```
airline-passenger-satisfaction/
└── README.md
└── EDA.knwf             # Exploratory data analysis
└── model_pipelines.knwf # End-to-end ML pipelines using tree based models.

```
---

## Methodology

### The ML pipeline

<img width="2323" height="870" alt="image" src="https://github.com/user-attachments/assets/fd0a27fa-1944-41bd-87ae-4c570f0851a9" />

### Exploratory Data Analysis

- Identified missingness mechanisms and hidden missingness among multiple features.
- Identified skewed feature distributions that could skewed results.
- Identified highly correlated features that would introduce collinearity.
- Utilised Χ-square tests and ANOVA to identify key relationships between features and the target variable.

### Feature Engineering

- Extracted hidden missingness and created missingness indicators for severeal features.
- Carefully imputed missing data to prevent data leakage, using EDA findings.

### Modelling

Two tree based models were used:

**Decision Tree**
- Reasonable performance
- High explainability

**Random Forest**
- Excellent performance
- Hyperparameter tuning: number of trees, max depth, minimum node size

### Model evaluation

Cross validation was used with the training data on both models, with the test data acting as a holdout set.

**Test set results:**

| Model | Accuracy  | ROC-AUC |
|---|---|---|
| Decision Tree | 0.881 | 0.942 |
| Random Forest | 0.909 | 0.971 |

<img width="670" height="699" alt="image" src="https://github.com/user-attachments/assets/81ca9638-ef43-4e32-ba9b-af5f600dd5b9" />

---

## Key findings

The most important aspects of passenger flight satisfaction:
- Travel class
- Inflight entertainment
- Seat comfort
- Ease of online booking
- Type of travel (personal/business)

**Service quality** features are hugely important in customer satisfaction.

Surprisingly, flight delay is **not** a top ranking feature within customer satisfaction.

Random Forest and Decision Tree produced consistant patterns, supporting the validity of these results.

---

## How to run

1. Download KNIME Analytics Platform (this project used v5.11.0)
2. Download both `.kwnf` files or just `model_pipeline.knwf` to see results.
3. Execute workflow nodes in order.



