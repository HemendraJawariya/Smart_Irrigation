# Smart_Irrigation
# 🌾 Irrigation System Sensor Data Prediction

This project uses sensor data from an irrigation system to predict the state of multiple parcels.  
It demonstrates an end-to-end machine learning workflow on IoT sensor data.

---

## 📁 Project Structure

Irrigation_System/ ├── irrigation_machine.csv       # Dataset containing sensor readings & parcel states ├── Irrigation_System.ipynb       # Jupyter notebook with analysis & training ├── models/ │   └── irrigation_model.pkl     # Saved trained model └── README.md                    # This file

---

## 📝 Dataset Overview

- **2000 samples**
- **20 sensor features:** `sensor_0` to `sensor_19`
- **3 parcel labels:** `parcel_0`, `parcel_1`, `parcel_2` (multi-label classification)

---

## ⚙️ What the Code Does

✅ Loads & explores the dataset (with `pandas`, `matplotlib`, `seaborn`)  
✅ Preprocesses data (drops extra columns, normalizes features)  
✅ Splits data into train/test sets  
✅ Trains a `RandomForestClassifier` inside a `MultiOutputClassifier`  
✅ Evaluates the model with classification reports  
✅ Saves the trained model using `joblib`

---

## 🚀 How to Run

### 🔨 Requirements

Install Python dependencies:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn joblib


---

▶ Running the Notebook

Launch Jupyter Notebook and run all cells:

jupyter notebook Irrigation_System.ipynb


---

💾 Using the Saved Model

After training, load and use your model like this:

import joblib
model = joblib.load("models/irrigation_model.pkl")

# Example prediction on new scaled data
# predictions = model.predict(new_sensor_data)


---

📊 Example Outputs

The notebook also generates:

Dataset summary statistics (df.describe())

Correlation heatmaps

Model classification reports

