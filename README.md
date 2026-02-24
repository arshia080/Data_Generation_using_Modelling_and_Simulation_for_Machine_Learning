# Data_Generation_using_Modelling_and_Simulation_for_Machin_Learning
##  Project Aim

This project focuses on generating synthetic traffic data using simulation techniques and applying multiple Machine Learning models to identify the most accurate predictor for vehicle waiting time at traffic signals.


## Simulation Tool Used

**SimPy** – A Python-based discrete-event simulation library used to model real-world systems like traffic flow, queues, and signal timing.


## Project Workflow

## Tool Setup
SimPy was chosen for its simplicity and seamless integration with Python for simulation-based data generation.

### Installation
All required libraries were installed in Google Colab using `pip`, followed by small test simulations to understand system behavior.

###  Parameter Configuration

| Parameter | Min | Max |
|------------|-----|-----|
| Vehicle Arrival Rate | 5 | 40 |
| Green Signal Duration | 20 | 90 |
| Red Signal Duration | 20 | 90 |
| Number of Lanes | 1 | 4 |
| Simulation Time | 60 | 300 |

Random values within these ranges were generated using **NumPy** for each simulation run.

### Data Generation
- Conducted **1000 simulation runs**
- Stored results in `simulation_data.csv`


## Machine Learning Models Applied

- Linear Regression  
- Decision Tree Regressor  
- Random Forest Regressor  
- KNN Regressor  
- Support Vector Regressor  
- Gradient Boosting Regressor  


## Evaluation Metrics

- **R² Score** – Measures model accuracy  
- **MAE** – Mean Absolute Error  
- **RMSE** – Root Mean Squared Error  


##  Model Selection

Initial comparison showed **Linear Regression** performing strongly.

To ensure unbiased ranking across multiple metrics, the **TOPSIS (Technique for Order Preference by Similarity to Ideal Solution)** method was implemented manually.

The model ranked **1st in `topsis_results.csv`** is considered the best overall predictor.

## Analysis

Graphs were generated to compare models based on:
- R² Score  
- MAE  
- RMSE  

These visualizations help understand performance differences clearly.


## Conclusion

This project demonstrates how simulation-generated synthetic datasets can be effectively used for Machine Learning model training and evaluation.

By integrating:
- Simulation (SimPy)
- Machine Learning
- Multi-Criteria Decision Making (TOPSIS)

the most suitable predictive model for traffic waiting time was successfully identified.

## Project Files

- `traffic_signal_simulation.ipynb` – Complete implementation  
- `simulation_data.csv` – Generated dataset  
- `model_results.csv` – Model evaluation metrics  
- `topsis_results.csv` – Final ranking  
- `README.md` – Documentation  


## How to Execute

1. Open the notebook in **Google Colab**
2. Install required libraries
3. Run all cells sequentially
4. Results, CSV files, and graphs will be generated automatically
