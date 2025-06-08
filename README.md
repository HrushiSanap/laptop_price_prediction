# Laptop Price Prediction

This repository contains a machine learning project focused on predicting laptop prices based on various features. The project leverages data analysis and machine learning techniques to create a regression model that estimates the market price of laptops.


## Project Overview

The goal of this project is to build a predictive model for laptop prices using publicly available datasets. The model can help users estimate the fair value of a laptop given its specifications, such as processor, RAM, storage, brand, and more.

## Features

- Data cleaning and preprocessing
- Exploratory data analysis (EDA)
- Feature engineering
- Multiple regression modeling approaches
- Model evaluation and performance metrics
- Jupyter Notebook(s) for experimentation and reproducibility

## Regression Models Used

The following regression models were implemented in the `4_modelling.ipynb` notebook:

1. **Linear Regression**
2. **Ridge Regression**
3. **Lasso Regression**
4. **ElasticNet Regression**
5. **Random Forest Regressor**
6. **Gradient Boosting Regressor**
7. **XGBoost Regressor**



## Results

**Result Summery**

| Model | Train R² | Val R² | Test R² | Train RMSE | Val RMSE | Test RMSE | CV RMSE |
|-------|----------|--------|---------|------------|----------|-----------|---------|
| Random Forest | 0.9757 | 0.8727 | 0.7707 | 1,001,517 | 2,063,782 | 2,841,306 | 2,670,264 |
| XGBoost | 0.9949 | 0.8281 | 0.7654 | 459,787 | 2,398,648 | 2,874,335 | 2,540,570 |
| Gradient Boosting | 0.9844 | 0.8474 | 0.7613 | 801,496 | 2,259,810 | 2,899,352 | 2,481,873 |
| LightGBM | 0.9542 | 0.8394 | 0.7182 | 1,375,579 | 2,318,078 | 3,150,033 | 2,657,594 |
| Ridge Regression | 0.8078 | 0.7629 | 0.6800 | 2,817,297 | 2,817,132 | 3,356,861 | 2,998,211 |
| ElasticNet Regression | 0.8083 | 0.7597 | 0.6784 | 2,813,799 | 2,835,823 | 3,365,442 | 2,996,216 |
| Linear Regression | 0.8093 | 0.7435 | 0.6692 | 2,806,194 | 2,929,694 | 3,412,918 | 3,003,509 |
| Lasso Regression | 0.8093 | 0.7435 | 0.6687 | 2,806,194 | 2,929,694 | 3,415,583 | 3,003,442 |

Based on these results, **Random Forest** appears to be the best model overall. Here's why:

**Key factors favoring Random Forest:**
- **Best test performance**: Highest Test R² (0.7707) and lowest Test RMSE (2,841,306)
- **Best generalization**: Smallest gap between validation and test performance
- **Good balance**: While it doesn't have the lowest training error, it maintains strong performance on unseen data
- **Reasonable cross-validation**: CV RMSE of 2,670,264 is competitive

**Why other top performers fall short:**
- **XGBoost**: Despite excellent training performance (R² = 0.9949), it shows significant overfitting with a large drop to test performance
- **Gradient Boosting**: Similar overfitting issues, though slightly better generalization than XGBoost

**The linear models** (Ridge, ElasticNet, Linear, Lasso) show consistent performance across train/val/test but are substantially weaker overall.

The key insight is that Random Forest achieves the best balance between model complexity and generalization. While XGBoost and Gradient Boosting can fit the training data better, Random Forest's ensemble approach with built-in regularization helps it perform best on new, unseen data - which is ultimately what matters most for a production model.


## Installation

**Clone the repository:**
   ```bash
   git clone https://github.com/HrushiSanap/laptop_price_prediction.git
   cd laptop_price_prediction
   ```



## Contact

- **Author:** [HrushiSanap](https://github.com/HrushiSanap)
- **Repository:** [laptop_price_prediction](https://github.com/HrushiSanap/laptop_price_prediction)

---

*Happy Predicting!*
