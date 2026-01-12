Predictive Analytics on Natural Fiber–Recycled Aggregate Concrete (NF-RAC)
Overview

This Python code implements predictive analytics to estimate Compressive Strength and Split Tensile Strength of Natural Fiber–Recycled Aggregate Concrete (NF-RAC) using machine learning models:

Random Forest Regressor

XGBoost Regressor

Artificial Neural Network (MLPRegressor)

The script handles data preprocessing, feature engineering, model training, evaluation, and visualization.

System Requirements

Hardware:

CPU: Quad-core or higher

RAM: ≥8 GB (16 GB recommended)

GPU: Optional, recommended only for faster ANN training

Software & Libraries:

Python ≥ 3.10

Required Python packages:

pip install pandas numpy matplotlib scikit-learn xgboost openpyxl

Environment Setup

Ensure Python is installed and updated.

Install the required libraries.

Place the dataset file dataset.xlsx in the same folder as the script.

Recommended IDE: Jupyter Notebook, VSCode, or PyCharm.

How to Run

Open the terminal or IDE in the project folder.

Run the script using Python:

python predictive_NF_RAC.py


The script will automatically:

Preprocess the dataset

Train the three models

Generate evaluation metrics

Save plots for actual vs predicted values

Notes

Ensure dataset.xlsx is correctly formatted and in the project folder.

GPU is optional; the code runs on CPU but may take longer for ANN training.

Figures are saved automatically as PNG files in the same folder.
