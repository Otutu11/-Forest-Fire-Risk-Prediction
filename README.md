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


---

### 🧪 `generate_forest_fire_data.py`

```python
# generate_forest_fire_data.py

import pandas as pd
import numpy as np

# Set random seed for reproducibility
np.random.seed(42)

# Generate synthetic data
n_samples = 1000
temperature = np.random.normal(loc=30, scale=5, size=n_samples)  # °C
humidity = np.random.normal(loc=50, scale=15, size=n_samples)    # %
wind = np.random.normal(loc=10, scale=3, size=n_samples)          # km/h
rain = np.random.exponential(scale=1.0, size=n_samples)           # mm

# Define fire risk: more likely when temp is high, humidity low, rain low, wind high
fire_risk = ((temperature > 33) & (humidity < 45) & (rain < 1.0) & (wind > 12)).astype(int)

# Create DataFrame
df = pd.DataFrame({
    'temperature': temperature.round(2),
    'humidity': humidity.round(2),
    'wind': wind.round(2),
    'rain': rain.round(2),
    'fire_risk': fire_risk
})

# Save to CSV
df.to_csv('forest_fire_data.csv', index=False)
print("Synthetic dataset saved as 'forest_fire_data.csv'")

Author Name: Otutu Anslem
Github: https://github.com/Otutu11/
LinkedIn: https://www.linkedin.com/in/otutu-anslem-53a687359/
