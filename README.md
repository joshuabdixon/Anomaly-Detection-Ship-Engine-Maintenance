# Anomalous Activity of a Ship’s Engine

This repository contains the code and analysis for detecting anomalous activity in a ship's engine using statistical and machine learning techniques. The project aims to improve ship maintenance and efficiency by identifying potential engine malfunctions.

## Problem Statement and Objective

The efficient operation of a ship's engine is crucial for the supply chain industry. Issues like overheating, poor lubrication, and fuel delivery problems can lead to increased risks, safety hazards, and downtime, impacting revenue. The objective of this project is to develop a robust anomaly detection system to monitor engine performance and predict potential maintenance needs. This can help reduce fuel consumption, prevent safety risks, and ensure timely deliveries.

Key challenges include identifying rare anomalies (approximately 1-5% of the data) in a vast dataset and developing a model that can detect these issues in real time.

## Statistical Techniques and Libraries

The analysis and anomaly detection process utilise the following statistical techniques and Python libraries:

### Statistical Techniques

- **Interquartile Range (IQR):** For identifying statistical outliers in the engine's operating parameters.
- **Principal Component Analysis (PCA):** Used for dimensionality reduction and data visualisation.
- **One-Class SVM:** A machine learning method for identifying anomalies in multivariate data.
- **Isolation Forest:** Another machine learning approach that isolates anomalies in the data.

### Python Libraries

- **NumPy:** For numerical computations and data manipulation.
- **Pandas:** For data analysis and preprocessing.
- **Scikit-learn:** For implementing machine learning models (e.g., One-Class SVM, Isolation Forest) and preprocessing (e.g., PCA, scaling).
- **Matplotlib/Seaborn:** For data visualisation, including histograms and box plots.
- **IPython:** For enhanced data display in Jupyter Notebooks.

## Key Variables and Assumptions

The data used for this project comprises six key features continuously monitored to evaluate the engine's performance:

### Key Variables

1. **Engine RPM:** High RPM can indicate overheating or excessive wear, while low RPM suggests potential mechanical issues.
2. **Lubrication Oil Pressure:** Low pressure may signal insufficient lubrication; high pressure can indicate blockages.
3. **Fuel Pressure:** High pressure may result in poor engine performance; low pressure suggests possible fuel delivery issues.
4. **Coolant Pressure:** Low pressure indicates potential leaks; high pressure may signal blockages or head gasket failure.
5. **Lubrication Oil Temperature:** High temperature can degrade oil quality; low temperature might affect lubrication.
6. **Coolant Temperature:** High temperature can cause overheating; low temperature may imply suboptimal operating conditions.

### Assumptions

- Anomalies constitute a small portion of the data (1-5%).
- Various statistical and machine learning methods can highlight deviations in engine performance that may require maintenance.
- Insights gained will guide recommendations for optimising engine maintenance and reducing operational risks.

## Simulation and Results

This project involved developing multiple anomaly detection models to identify potential issues in ship engine performance. The models were evaluated based on their ability to identify outliers accurately and provide actionable insights.

### Key Steps

1. **Data Exploration:** Conducted Exploratory Data Analysis (EDA) to identify data distributions, outliers, and central tendencies using statistical techniques.
2. **Anomaly Detection:**
   - **IQR Method:** Detected outliers in individual features and flagged anomalies.
   - **One-Class SVM:** Applied for identifying anomalies in multivariate data using scaled and PCA-transformed features.
   - **Isolation Forest:** Implemented to compare its effectiveness in detecting outliers.
3. **Evaluation:** Compared different models based on the percentage of detected anomalies and their alignment with business expectations.

### Results and Recommendations

- **Anomaly Distribution:** Identified anomalies that may lead to engine malfunctions, providing thresholds for critical features.
- **Feature Importance:** Utilised mutual information to rank the features based on their influence on anomaly detection.
- **Suggested Implementations:**
  - Monitor key engine features (e.g., lubrication oil pressure, engine RPM) closely for predictive maintenance.
  - Adjust thresholds based on business needs to optimise model performance.

## Summary

This anomaly detection project highlights the use of statistical and machine learning techniques to address real-world challenges in the maritime supply chain. By employing methods like IQR, One-Class SVM, and Isolation Forest, this analysis provides insights for proactive ship engine maintenance. The repository demonstrates expertise in data preprocessing, statistical analysis, and the application of machine learning models for anomaly detection.

Feel free to explore the code and analysis provided in this repository. If you have questions or would like to discuss further, please contact me.

### Files Included in This Repository

- **Notebook:** A detailed Jupyter Notebook (`Anomaly Detection - Ship Engine Maintenance.ipynb`) containing the full implementation of the anomaly detection models.
