# Tourist Arrival Prediction Project

## Overview

This project aims to predict the number of tourist arrivals using various machine learning models: XGBoost, Random Forest, and Support Vector Regressor (SVR). The dataset includes two types of tourist arrival data: Chinese tourists (`arrival mainland`) and international tourists (`arrival global`). The project involves data preprocessing, model training, evaluation, and visualization of results.

## Project Structure

- `tourist_arrival_prediction.py`: Main Python script containing data loading, preprocessing, model training, evaluation, and plotting.
- `tourist_arrival_data.xlsx`: Excel file containing the dataset with columns `arrival mainland` and `arrival global`.

## Requirements

- Python 3.6+
- Required Python packages (can be installed via `requirements.txt`):
  ```bash
  pip install pandas numpy scikit-learn xgboost matplotlib
  ```

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/sadrasa97/tourist-arrival-prediction.git
   ```
2. Change into the project directory:
   ```bash
   cd tourist-arrival-prediction
   ```
3. Install the required packages:
   ```bash
   pip install -r requirements.txt
   ```

## Usage

1. Ensure the dataset (`tourist_arrival_data.xlsx`) is in the project directory.
2. Run the main script:
   ```bash
   python tourist_arrival_prediction.py
   ```

## Methodology

### Data Loading and Preprocessing

The data is loaded from the Excel file into a pandas DataFrame. The columns `arrival mainland` and `arrival global` are extracted for Chinese and international tourists, respectively.

### Train-Test Split

The data is split into training and testing sets using an 80-20 split. Two separate train-test splits are performed:
- Predicting international tourists using Chinese tourists data.
- Predicting Chinese tourists using international tourists data.

### Model Training

Three models are trained:
- XGBoost
- Random Forest
- SVR

Each model is trained on the training data and used to make predictions on the test data.

### Model Evaluation

The performance of each model is evaluated using the following metrics:
- Mean Squared Error (MSE)
- Mean Absolute Percentage Error (MAPE)
- Mean Absolute Error (MAE)

### Visualization

The results are visualized using matplotlib. Scatter plots show the actual vs. predicted values for each model, and bar plots compare the evaluation metrics across different models.

## Results

The results for each model are printed to the console, showing the MSE, MAPE, and MAE for both Chinese and international tourists.
