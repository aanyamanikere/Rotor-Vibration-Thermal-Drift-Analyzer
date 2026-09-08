# Drone Battery Thermal Drift Analyzer
A Python project that uses Machine Learning to model drone battery overheating caused by rotor vibrations and archive high-risk flight logs.

![Thermal Drift Analysis](thermal_drift_analysis.png)

## 📌 Project Overview
Mechanical rotor vibration in unmanned aerial vehicles (UAVs) transfers kinetic energy into internal components, leading to friction and thermal buildup. Unmonitored thermal drift can accelerate battery degradation or trigger thermal runaway mid-flight.

This project uses **Linear Regression** to:
1. Generate synthetic data for 100 drone flights (`vibration_hz` and `battery_temp_c`).
2. Train a predictive model to estimate battery temperature based on vibration level.
3. Identify high-risk flights predicted to exceed **65 °C**.
4. Archive the high-risk logs into a binary `.pkl` file using Python's `pickle` library.
5. Plot the results with Matplotlib.
