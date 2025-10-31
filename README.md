# Bike Sharing Demand — AutoGluon

Predicting bike rental demand using tabular AutoML (AutoGluon) on the classic Kaggle "Bike Sharing Demand" dataset.

## Project goal
The goal is to predict the number of rented bikes (`count`) for each timestamp based on weather, calendar, and time-of-day features.  
This is useful for real-world demand forecasting (mobility, delivery, fleet planning).

Competition: Kaggle "Bike Sharing Demand".

## What I did
- Loaded the provided `train.csv` / `test.csv`
- Engineered time features from `datetime` (hour, weekday, etc.)
- Trained several AutoGluon Tabular models
- Generated predictions for `count` on the test set
- Submitted the results to Kaggle and recorded the score

## Tech stack
- Python
- Jupyter Notebook
- AutoGluon Tabular
- pandas / numpy / matplotlib

## Reproduce
1. Create and activate a virtual environment
2. Download the Kaggle data (`train.csv`, `test.csv`) and put them in `data/`
3. Open the notebook in `notebooks/` and run all cells to train and create a submission file

## Result
Best public leaderboard score: **0.46182 RMSLE**.

AutoGluon builds an ensemble of different models and ranks them. I compared multiple presets / training time limits and selected the best run for submission.

---
This project was done as part of the ML coursework to practice demand forecasting on tabular data and to build a full Kaggle workflow (training → inference → submission).
