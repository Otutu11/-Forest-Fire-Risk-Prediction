# 🔥 Forest Fire Risk Prediction

This project implements a machine learning model to predict the risk of forest fires based on environmental parameters such as temperature, humidity, wind speed, and rainfall.

## 📊 Dataset

The model uses a dataset with the following columns:

- `temperature`: Ambient temperature in °C
- `humidity`: Relative humidity in %
- `wind`: Wind speed in km/h
- `rain`: Rainfall in mm
- `fire_risk`: Binary label (0 = Low Risk, 1 = High Risk)

You can use the provided synthetic dataset generator or your own dataset.

## 🧠 Model

The model uses a **Random Forest Classifier** for classification.

## 📁 File Structure

Forest-Fire-Risk-Prediction/
│
├── forest_fire_risk_prediction.py # Main ML training and prediction script
├── generate_forest_fire_data.py # Generates synthetic dataset
├── forest_fire_data.csv # Dataset used for model training
└── README.md # This file


## 🚀 Usage

### 1. Install Dependencies

```bash
pip install pandas numpy scikit-learn matplotlib seaborn

2. Generate Synthetic Dataset

python generate_forest_fire_data.py

3. Run the Model

python forest_fire_risk_prediction.py

📈 Output

    Classification accuracy and metrics

    Confusion matrix heatmap

    Feature importance bar chart

    Fire risk prediction for a new input sample
