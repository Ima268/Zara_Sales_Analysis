# Zara Sales Volume Prediction

## Overview
This project builds a machine learning model to predict **sales volume** for Zara products based on product category and seasonal attributes inorder to help with inventory management. A **Random Forest Regressor** is used for regression modeling.

## Dataset
- The dataset `cleaned_zara_sales.csv` contains product information such as product category, seasonal and sales volume.
- The data includes columns like:
  - `Product Category`
  - `Seasonal`
  - `Sales Volume`
  - (and other product details not used in modeling)

## Steps Performed

1. **Data Loading & Cleaning**  
   The CSV file is loaded using pandas with proper delimiter and encoding. Column names are stripped of whitespace.

2. **Data Preprocessing**  
   - Kept only relevant columns: `Product Category`, `Seasonal`, `Sales Volume`.  
   - Dropped missing values.  
   - Encoded categorical variables (`Product Category`, `Seasonal`) using `LabelEncoder`.

3. **Train-Test Split**  
   The dataset is split into training (80%) and testing (20%) sets.

4. **Model Training**  
   A `RandomForestRegressor` is trained on the training data.

5. **Model Evaluation**  
   Model predictions on the test set are evaluated using Mean Squared Error (MSE) and R² score.

6. **Results**  
   Actual vs predicted sales volumes are saved to `model_predictions.csv`.

## Visualization
Visualizations included in the project:
- Distribution of sales volume.
- Sales volume by product category and seasonal attributes.
- Actual vs predicted sales volume scatter plot.
- Feature importance plot from the random forest model.

## Requirements

- Python 3.x  
- pandas  
- scikit-learn  
- matplotlib  
- seaborn

Installed the requirements with:

```bash
pip install pandas scikit-learn matplotlib seaborn