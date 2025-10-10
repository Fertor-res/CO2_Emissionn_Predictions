# 🟢 CO₂ Emissions Prediction App

This Streamlit web application allows users to **predict annual CO₂ emissions** from fossil fuel–based power plants using a machine learning model trained on real-world data from the **U.S. Energy Information Administration (EIA)**.

## Project Overview

This tool estimates **CO₂ emissions (in tons/year)** based on key operational parameters of a power plant, such as:

- Fuel consumption for electric generation (MMBtu)
- Total fuel consumption (MMBtu)
- Electricity generation (kWh)
- Fuel type (e.g., Natural Gas, Bituminous Coal, etc.)
- Prime mover type (e.g., Steam Turbine, Gas Turbine, etc.)

The model was trained using **measured emissions data** (not calculated) from fossil fuel power plants across the United States.

## Machine Learning Model

- **Algorithm**: Random Forest Regressor
- **Training Data Source**: [U.S. Energy Information Administration (EIA)](https://www.eia.gov/electricity/data)
- **Model File**: `trained_pipe_co2.joblib` (stored in `model_pickle/` directory)

## Getting Started

### 1. Clone the Repository

```
bash
git clone https://github.com/your-username/co2-emissions-predictor.gitcd co2-emissions-predictor
```

### 2. Install Dependencies
Make sure you have Python 3.8+ installed. Then install the required packages:

```
bash
pip install -r requirements.txt
```

### 3. Run the App
```
bash
streamlit run app.py
```

The app will open in your default browser at http://localhost:8501.


## How to Use
- Enter the following inputs:
- Fuel Consumption for Electric Generation (MMBtu)
- Total Fuel Consumption (MMBtu)
- Electricity Generation (kWh)
- Fuel Code (select from dropdown)
- Prime Mover (select from dropdown)
- Click "Predict CO2 Emissions".
- The app will display the estimated CO₂ emissions in tons per year.

## Project Structure

```
co2-emissions-predictor/
├── app.py                      # Main Streamlit app
├── model_pickle/
│   └── trained_pipe_co2.joblib # Trained Random Forest model
├── requirements.txt            # Python dependencies
└── README.md                   # Project documentation
```



## Example Inputs

| Parameter                                |Example Value       |
|------------------------------------------|--------------------|
| Fuel Consumption for Electric Generation |1,200,000 MMBtu     | 
| Total Fuel Consumption|1,500,000 MMBtu  |1,500,000 MMBtu     |
| Generation                               |500,000,000 kWh     | 
| Fuel Code                                |NG - Natural Gas    | 
| Prime Mover                              | ST - Steam Turbine | 


## Notes
- The model is intended for educational and exploratory purposes.
- Predictions are based on historical U.S. data and may not generalize to all global contexts.
- The app uses Streamlit session state to retain user inputs and predictions across interactions.

📄 License

This project is licensed under the MIT License. See the LICENSE file for details.


Developed by [Fernando Torres & Natasha Cuotto]

