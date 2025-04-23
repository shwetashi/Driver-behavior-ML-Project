# Driver-behavior-ML-Project
**Risky Driver Behavior Detection using Sensor Data**
**Project Overview**
This project aims to detect risky driving behaviors—such as sudden acceleration, sharp turns, and 
hard braking—using time-series data from an MPU6050 accelerometer and gyroscope, collected via a Raspberry Pi 3 Model B mounted in different vehicles.

**Dataset**
Sensor: MPU6050 (Accelerometer + Gyroscope)
Sampling Rate: ~2 Hz
Window Size: 14 seconds
Drivers: 3 (aged 27, 28, 37)
Vehicles: Ford Fiesta 1.4, Ford Fiesta 1.25, Hyundai i20
Behaviors Labeled:
1: Sudden Acceleration
2: Sudden Right Turn
3: Sudden Left Turn
4: Sudden Brake

**Feature Engineering**
Raw sensor data segmented into 14-second windows i.e. 28 rowset -> 28/2 seconds
Features extracted: mean, std, min, max, energy, skew and kurtosis (accel_x/y/z, gyro_x/y/z)

**Models Used**
Random forest classifier (with hyperparameter tuning via RandomizedSearchCV)
Logistic Regression (with hyperparameter tuning via GridSearchCV)
Support Vector Classifier (SVC with RBF and linear kernels)

**Evaluation Metrics**: Accuracy, Precision, Recall, F1-score

**Installation and set up **
git clone https://github.com/shwetashi/Driver-behavior-ML-Project.git
cd Driver-behavior-ML-Project
pip install -r requirements.txt

Run file with python

