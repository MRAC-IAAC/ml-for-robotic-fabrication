# ML for Robotic Fabrication: Predicting the Hypotenuse

## Overview

This project applies machine learning to Pythagoras’ theorem to predict the hypotenuse of a right-angle triangle given the lengths of its legs.


## Dataset Description

- **Features:**
  - `leg1`: Length of the first leg (randomly generated between 1 and 100).
  - `leg2`: Length of the second leg (randomly generated between 1 and 100).
- **Target:**
  - `hypotenuse`: Computed using the formula \( \sqrt{leg1^2 + leg2^2} \).
- **Generation:** 1,000 samples are generated with random values to simulate right-angle triangles.

## Model Details

- **Model Used:** Linear Regression
- **Input Features:** `leg1` and `leg2`
- **Target Variable:** `hypotenuse`
- **Rationale:** Although the true relationship is non-linear, Linear Regression provides a simple baseline model for this regression task.

## Evaluation Results

After splitting the dataset (80% training, 20% testing), the model was trained and evaluated. Below are the evaluation metrics:

- **Mean Squared Error (MSE):** *[insert printed value]*  
- **R² Score:** *[insert printed value]*  

### Graphs:

1. **Actual vs. Predicted Hypotenuse:**  
   A scatter plot showing the correlation between actual hypotenuse values and the model's predictions, with a red dashed line indicating the ideal prediction.

2. **Residuals Histogram:**  
   A histogram of the residuals (difference between actual and predicted hypotenuse values) to inspect the error distribution.

## Observations

- The model captures the trend of the hypotenuse well, but due to the inherent non-linearity of the square root function, the linear regression model has limitations.
- The error distribution (residuals) suggests that while most predictions are close to the actual values, there are systematic deviations that may be improved with non-linear models or feature engineering (e.g., including squared features).
- Future work could involve testing polynomial regression or more complex models such as neural networks to capture the non-linear behavior more accurately.

## How to Run

1. Clone the repository.
2. Ensure that you have Python installed along with the required packages (numpy, pandas, scikit-learn, matplotlib).
3. Navigate to the `src` folder and run the `pythagoras_ml.ipynb` notebook in Jupyter Notebook.

Feel free to reach out if you have any questions or need further clarifications.

