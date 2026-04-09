# ✈️ Airline Passenger Satisfaction Prediction

![KNIME](https://img.shields.io/badge/KNIME-Analytics-orange)
![Random Forest](https://img.shields.io/badge/Model-Random%20Forest-blue)
![Decision Tree](https://img.shields.io/badge/Model-Decision%20Tree-lightgrey)

Machine learning pipeline achieving **91% accuracy and 0.97 AUC**, identifying key factors of airline passenger satisfaction.

---

## 🚀 Overview

This project analyses airline passenger satisfaction using KNIME, combining EDA, feature engineering, and tree based models to **predict outcomes and explain crucial factors of passenger satisfaction**.

---

## 📊 Key Results

| Model                 | Accuracy  | ROC-AUC   |
| --------------------- | --------- | --------- |
| Decision Tree         | 0.881     | 0.942     |
| Random Forest (tuned) | **0.909** | **0.971** |

---

## 🔍 Exploratory Data Analysis

* Identified hidden missingness (e.g. rating values of 0, age = 999)
* Analysed feature distributions and skew
* Detected strong correlations (e.g. arrival vs departure delay)
* Used χ² tests and ANOVA to identify significant relationships

---

## ⚙️ Feature Engineering

* Converted invalid ratings (0 → missing)
* Created **missingness indicator features**
* Group-based median imputation (e.g. by class, travel type)
* One-hot encoding of categorical variables

---

## 🧠 Modelling

### Decision Tree

* Information Gain splitting
* MDL pruning to prevent overfitting
* Highly interpretable decision rules

### Random Forest

* Hyperparameter tuning:
  * number of trees
  * maximum tree depth
  * minimum node size
* Cross validation on train data, with holdout test set
* Excellent performance

---

## 📂 Project Structure

```
airline-passenger-satisfaction/
├── EDA.knwf                 # Exploratory analysis workflow
├── model_pipelines.knwf     # End-to-end ML pipelines
└── README.md
```

---

## 🧠 Key Insights

* **Travel class is the strongest predictor of satisfaction**
* Other service quality features are also highly important:
  * inflight entertainment
  * seat comfort
  * ease of online booking
* Type of travel (business vs personal) is significant
* Flight delays are less important than expected
* Decision Tree and Random Forest show **consistent feature importance**, supporting result validity

---

## ▶️ How to Run

1. Download KNIME Analytics Platform (this project used v5.11.0)
2. Download both `.kwnf` files or just `model_pipeline.knwf` to see results.
3. Execute workflow nodes in order.
