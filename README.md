# 🚢 Ship Energy Consumption Prediction

## 📌 Overview
This project focuses on predicting the fuel consumption of a Ro-Ro passenger ship using onboard sensor data.

The dataset comes from the vessel **MS Smyril**, collected between February and April 2010. It contains data from 246 voyages and around 1.6 million records. The data includes measurements from navigation systems, engine-related sensors, and environmental conditions.

The main goal is to estimate how much fuel the ship is consuming at any given time based on these signals.

---

## 📊 Dataset

The dataset is split into multiple files, each corresponding to a specific sensor. These include:

### ⚡ Fuel System
- `fuelDensity` (kg/L)
- `fuelTemp` (°C)
- `fuelVolumeFlowRate` (L/s)

### 🚢 Navigation
- Speed over ground (SOG)
- Speed through water (STW)
- Latitude & longitude
- Heading and track angles

### 🌬️ Environment
- Wind speed (m/s)
- Wind angle (degrees)

### ⚙️ Ship Control
- Rudder angles (port & starboard)
- Propeller pitch (port & starboard)
- Trim angle (inclinometer)
- Water level measurements (port & starboard)

All data is time-series based, meaning proper alignment using timestamps is essential before any analysis.

---

## 🎯 Target Variable

Fuel consumption is computed using:
EC = (fuelDensity × fuelVolumeFlowRate × 3600 × 24) / 1000


- Unit: **tons/day**

This value represents the ship’s energy consumption and is the target variable for prediction.

---

## ⚠️ Notes
- Data comes from multiple sensors and must be merged carefully  
- Timestamps need to be parsed and aligned correctly  
- The dataset is relatively large (~1.6M rows), so efficient processing helps  
