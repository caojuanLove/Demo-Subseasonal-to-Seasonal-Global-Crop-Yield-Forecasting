# Demo-Subseasonal-to-Seasonal-Global-Crop-Yield-Forecasting
README – Demo for 2018 Winter Wheat Yield Forecasting in India

This repository provides a demonstration of the workflow used to forecast 2018 winter wheat yield in India using an LSTM-based framework.
The Demo is designed for reader to understand the model construction, hyperparameter tuning, forecasting procedure, and interpretability analysis.

1. Overview

The steps include:

	Hyperparameter optimization of the LSTM model

	LSTM model construction, training, validation, and testing

	Dynamic yield forecasting using historical-week (Hist) datasets

	Dynamic yield forecasting using S2S forecast datasets

	Model interpretability using SHAP



2. Folder Structure
	Demo/
	│
	├── code/
	│   ├── 06_LSTM_Hyperparameter_Optimization.py
	│   ├── 07_LSTM_Model_Training_and_Evaluation.py
	│   ├── 12_Apply_Trained_LSTM_to_Dynamic_Hist_Yield_Forecast.py
	│   ├── 12_Apply_Trained_LSTM_to_Dynamic_S2S_Yield_Forecast.py
	│   └── 13_LSTM_Shapley_Factor_Importance.py
	│
	├── dataset/
	│   ├── 01_inputdata/
	│   └── 02_ForecastData/
	│       ├── Hist/
	│       └── S2S/
	│
	├── results/
	│   ├── LSTM/
	│   └── SHAP/
	│
	└── Trained_model/

3. Dataset Description
	3.1 01_inputdata
		Processed winter wheat datasets for all administrative regions in India.Time span 2001-2018
		Each sample includes:Weekly dynamic features,Static biophysical/socioeconomic features,Observed yield

3.2 02_ForecastData

Contains two types of forecasting inputs:

	a) Hist (Historical-week datasets)

	Located in:~\Demo\dataset\02_ForecastData\Hist\I. Leadweek_1 → 1-week lead,Leadweek_12 → 12-week lead.


	b) S2S (Sub-seasonal to seasonal forecast datasets)

	Located in:~\Demo\dataset\02_ForecastData\S2S\I


4. Expected Outputs

	(1) Best hyperparameters
	best_params/*.json

	(2) Trained LSTM model
	Trained_model/*.keras

	(3) Performance metrics and PFI
	results/LSTM/I/

	(4) Lead-time-based dynamic forecasts

	Historical-week forecast results

	S2S ensemble forecast results

	Line plots, distribution plots, and regional maps (if applicable)

	(5) SHAP interpretability results
	results/SHAP/

