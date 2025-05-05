# Rain-Prediction-using-stacking-and-Multi-layer-Perceptron

Overview

This project, contained in the Jupyter Notebook DS_Project_Complete.ipynb, focuses on analyzing weather data and building a machine learning model to predict weather-related metrics. The dataset includes weather measurements such as temperature, humidity, precipitation, and wind speed, collected over multiple years (2021–2023). The notebook covers data loading, exploration, preprocessing, and model development, culminating in saving a trained model and scaler for future use.

Dataset

The dataset (Weather Data.csv) contains daily weather observations with the following columns:
YEAR: Year of observation (2021, 2022, 2023)
MO: Month of observation (1–12)
DY: Day of observation (1–31)
Temperature at 2 Meters (°C): Average temperature
Dew/Frost Point at 2 Meters (°C): Dew point temperature
Temperature at 2 Meters Maximum (°C): Maximum temperature
Temperature at 2 Meters Minimum (°C): Minimum temperature
Specific Humidity at 2 Meters (g/kg): Specific humidity
Relative Humidity at 2 Meters (%): Relative humidity
Precipitation Corrected (mm/day): Corrected precipitation
Wind Speed at 10 Meters: Wind speed
The dataset has 1094 entries with no missing values, as verified during exploration.

Notebook Structure

The notebook is organized into the following sections:
Data Loading:
Loads Weather Data.csv into a Pandas DataFrame using pd.read_csv.
Handles potential encoding issues (UTF-8, Latin1).
Displays the first 5 rows to verify successful loading.

Data Exploration:
Displays the first and last 5 rows (head, tail).
Provides dataset structure (info) and statistical summary (describe).
Checks for missing values and lists unique values in the YEAR column.

Handling Missing Data:
Verifies no missing values exist.
Implements a precautionary strategy to fill numeric columns with median values and categorical columns with mode (though not needed).

Model Development and Saving:
Trains a multilayer perceptron (MLP) model for weather prediction (specific details not shown in the provided excerpt).
Saves the trained model as mlp_weather_model.h5 and the scaler as scaler.save using HDF5 format.
Includes JavaScript code for downloading the saved files in Google Colab.


Requirements
To run the notebook, install the following Python libraries:
pip install pandas numpy tensorflow scikit-learn
The notebook was developed in a Google Colab environment, which provides the necessary dependencies and JavaScript functionality for file downloads.
Usage

Setup:
Place Weather Data.csv in the same directory as the notebook or update the file_path variable.
Ensure the required libraries are installed.

Running the Notebook:
Open DS_Project_Complete.ipynb in Jupyter Notebook or Google Colab.
Execute cells sequentially to load, explore, preprocess, and model the data.
The trained model and scaler will be saved and downloadable as mlp_weather_model.h5 and scaler.save.

Troubleshooting:
If the testing cell causes an error, remove or replace it with appropriate testing code (e.g., model evaluation or predictions).
For encoding errors during data loading, the script attempts latin1 encoding if utf-8 fails.

Outputs
Saved Files:
mlp_weather_model.h5: Trained MLP model for weather prediction.
scaler.save: Scaler used for data normalization.

