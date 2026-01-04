# Heart Disease Prediction Using Machine Learning

## Overview
This project predicts the presence of heart disease in patients using a Random Forest classifier.  
The workflow includes data preprocessing, training, and generating predictions on new data.

---

## Dataset
- Source: Kaggle ([Heart Disease Dataset](https://www.kaggle.com/ronitf/heart-disease-uci))
- Contains patient features such as age, blood pressure, cholesterol, and others.
- The target variable `target` indicates presence (`1`) or absence (`0`) of heart disease.

---

## Project Structure
heart_disease_model/
├── heart_input_data.csv # Features used for inference
├── heart_disease_prediction.csv # Model predictions (0/1)
├── heart_ml_notebook.ipynb # Jupyter notebook with training & inference
├── .gitignore # Git ignore for artifacts
└── README.md # Project description

---

## Features
- Handles missing values using median imputation
- Scales numerical features using `StandardScaler`
- Uses a Random Forest classifier
- Maintains class proportions using StratifiedShuffleSplit
- Predictions are generated on features-only data

---

## Usage
1. Open `notebook.ipynb` in Jupyter Notebook
2. Run cells to train the model (if model `.pkl` not present)
3. Run inference to generate `heart_disease_prediction.csv`
4. Input features are in `heart_input_data.csv`

> **Note:** The model and pipeline `.pkl` files are **not included**; they are generated automatically.

---

## Target Encoding
- `0` → No heart disease  
- `1` → Heart disease

---

## Requirements
- Python 3.x
- Libraries:
  ```text
  pandas
  numpy
  scikit-learn
  joblib
