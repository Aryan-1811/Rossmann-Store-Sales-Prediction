# Rossmann-Store-Sales-Prediction
Forecasting daily sales for Rossmann stores using advanced machine learning and deep learning models.

## Overview
This project predicts the daily sales of Rossmann retail stores using historical data.  
It covers data preparation, feature engineering, model training and evaluation, and final sales forecasting.

## Models Used
1. **RandomForestRegressor** – Ensemble model from scikit-learn  
2. **LGBMRegressor** – Gradient boosting model from LightGBM  
3. **Neural Network (Keras Sequential)** – Deep learning regression model built with TensorFlow/Keras  

After model comparison, **Random Forest was chosen for final predictions** because it achieved the **lowest RMSE value** on validation data.  
The final predictions were exported into `test_final_selected.csv`.

## Data
The following datasets are required for the notebook:
- `train.csv` – historical sales and store data  
- `test.csv` – test set for prediction  
- `store.csv` – store information such as type, assortment, and promo details  

Dataset links:  
- Train: https://drive.google.com/file/d/1lnls9LYC06S4-zE_Nz03TGwqF_RJkxAw/view?usp=sharing
- Test: https://drive.google.com/file/d/1kWw4OFhR_nLA8S2ogucUL_mJRDkt40nK/view?usp=sharing
- Store: https://drive.google.com/file/d/1-RcfNOjLjBDgNv2CYoIYhT6q3nJBbTrA/view?usp=sharing 

*(Datasets are not uploaded to GitHub due to size limits. Place them in a local `data` folder before running the notebook.)*

## How to Run
1. Create a folder named `data`  
2. Move `train.csv`, `test.csv`, and `store.csv` into it  
3. Open `RossmanStoresSalesPrediction.ipynb` in Jupyter Notebook  
4. Run all cells to preprocess data, train models, and generate predictions  
5. The notebook will produce `test_final_selected.csv` automatically  

## Libraries Used
- Python  
- Pandas and NumPy  
- scikit-learn  
- LightGBM  
- TensorFlow and Keras  
- Matplotlib and Seaborn  

## Key Steps
- Feature engineering on date, promo, and store-level attributes  
- Training multiple regression models for sales forecasting  
- Evaluation of RMSE scores for each model  
- Random Forest selected for final predictions based on best performance  

## Insights
- Ensemble models performed better than deep learning for this dataset size  
- Promotional and date-based features had strong impact on sales  
- Neural Network performed competitively but slightly under Random Forest in RMSE  
