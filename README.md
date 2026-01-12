Predictive Analytics on Natural Fiber–Recycled Aggregate Concrete (NF-RAC)
Project Overview

This project implements predictive analytics to evaluate the mechanical performance of Natural Fiber–Recycled Aggregate Concrete (NF-RAC). The main target properties are:

Compressive Strength (MPa)

Split Tensile Strength (MPa)

The code uses three predictive models:

Random Forest Regressor

XGBoost Regressor

Artificial Neural Network (MLPRegressor)

It covers data preprocessing, feature engineering, model training, evaluation, and visualization of results. The outputs include performance metrics, scatter plots of predicted vs actual values, and saved CSV tables.

Dataset

Source: Ali, A., Khalid, M., & Khan, S. (2021). Natural fiber–recycled aggregate concrete dataset [Data set]. Mendeley Data. https://data.mendeley.com/datasets/7chtgrwkv3/2

Contains 482 experimental concrete mixes with features such as: mix proportions, fiber type, and curing conditions.

Target variables: Compressive Strength and Split Tensile Strength.

System Requirements

Hardware:

CPU: Quad-core or higher

RAM: ≥8 GB (16 GB recommended)

GPU (optional for ANN training): NVIDIA GPU with CUDA support

Software:

Python ≥3.10

Required Python libraries:

pip install pandas numpy matplotlib scikit-learn xgboost openpyxl


IDE: Jupyter Notebook, PyCharm, VSCode, or similar

Code Structure

Data Loading & Preprocessing

Loads dataset.xlsx

Replaces placeholders ('x') with NaN

One-hot encodes categorical features (Fiber Type)

Drops rows with missing values

Feature–Target Separation

X contains input features

y_comp and y_split are target variables

Train-Test Split & Scaling

80% training, 20% testing

Standard scaling applied to features

Model Definitions

Random Forest Regressor

XGBoost Regressor

ANN (MLPRegressor with early stopping)

Model Training & Evaluation

Fits each model separately for both targets

Calculates R², RMSE, and MAE

Saves results in Table_6_2_Model_Performance.csv

Visualization

Scatter plots of actual vs predicted values

Saved automatically as PNG files:

Figure6_Compressive_<ModelName>.png

Figure6_Split_<ModelName>.png

How to Run

Place dataset.xlsx in the same folder as the Python script.

Install required Python libraries.

Run the script in Jupyter Notebook or execute via terminal/IDE:

python predictive_NF_RAC.py


Outputs:

Table: Table_6_2_Model_Performance.csv

Figures: Actual vs predicted plots for all models

Outputs Example

Model Performance Table:

Model	R²_Compressive	RMSE_Compressive	MAE_Compressive	R²_Split	RMSE_Split	MAE_Split
Random Forest	0.947	4.449	3.069	0.941	0.336	0.236
XGBoost	0.964	3.659	2.450	0.960	0.276	0.208
ANN	0.933	5.008	3.462	0.906	0.424	0.327

Figures Generated:

Figure6_Compressive_Random_Forest.png

Figure6_Compressive_XGBoost.png

Figure6_Compressive_ANN.png

Figure6_Split_Random_Forest.png

Figure6_Split_XGBoost.png

Figure6_Split_ANN.png

Environment Notes

CPU execution is sufficient; GPU is optional for ANN

Ensure adequate RAM for large datasets or complex models

Figures saved with bbox_inches='tight' for publication-ready quality
