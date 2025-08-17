# Remaining Useful Life (RUL) Prediction Project

## Project Overview

This project predicts the Remaining Useful Life (RUL) of aircraft engines using machine learning models trained on sensor and operational data. It leverages regression techniques to estimate how long an engine will function before failure, aiding predictive maintenance and reducing downtime.

---

## Project Steps

1. **Data Loading and Preprocessing**  
   - Loads the training dataset containing operational settings and sensor measurements.  
   - Removes unused sensor columns to optimize model input.  
   - Calculates RUL for each data point based on the engine's maximum cycle.

2. **Feature Preparation**  
   - Selects relevant features excluding identifiers and target variable (RUL).  
   - Scales features using Min-Max normalization for model compatibility.

3. **Train-Test Split**  
   - Splits dataset into training and test sets (80-20) to evaluate model performance on unseen data.

4. **Model Training and Evaluation**  
   - Trains multiple regression models:  
     - Random Forest Regressor  
     - Gradient Boosting Regressor  
     - Multi-layer Perceptron (Neural Network)  
   - Evaluates each model using MAE, MSE, and R² metrics on the test set.  
   - Prints performance summaries for model comparison.

5. **Model Selection and Saving**  
   - Selects the best-performing model based on highest R² score.  
   - Saves the trained model, scaler, and feature list to disk for later inference.

6. **Remaining Useful Life Prediction**  
   - Loads the saved model and scaler.  
   - Prepares new input engine data matching trained features.  
   - Performs scaling and predicts RUL for the new engine data.  
   - Outputs the predicted RUL in cycles.

---

## Performance Summary


- **MAE (Mean Absolute Error):** 29.64 cycles  
- **MSE (Mean Squared Error):** 1717.62  
- **R² Score:** 0.6241  
Predicted Remaining Useful Life (RUL): 201.62 cycle  
The metrics indicate strong predictive capability suitable for maintenance planning.

---

## Usage Instructions

1. Install dependencies:

