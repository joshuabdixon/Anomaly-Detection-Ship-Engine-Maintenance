# Anomalous Activity of a Ship’s Engine - Preliminary

This repository contains the code and analysis for detecting anomalous activity in a ship's engine using statistical and machine learning techniques. The project aims to improve ship maintenance and efficiency by identifying potential engine malfunctions.

## Problem Statement and Objective

The efficient operation of a ship's engine is crucial for the supply chain industry. Issues like overheating, poor lubrication, and fuel delivery problems can lead to increased risks, safety hazards, and downtime, impacting revenue. The objective of this project is to develop a robust anomaly detection system to monitor engine performance and predict potential maintenance needs. This can help reduce fuel consumption, prevent safety risks, and ensure timely deliveries.

Key challenges include identifying rare anomalies (approximately 1-5% of the data) in a vast dataset and developing a model that can detect these issues in real-time.

## Key Findings

Based on the analysis, several engine features exhibited more anomalies than others. This was apparent from the exploratory data analysis and remained generally consistent whether statistical or machine learning methodologies were used:
- **Lubrication Oil Temperature**
- **Coolant Pressure**
- **Fuel Pressure**
- **Engine RPM**

These features are crucial for ongoing monitoring as they often indicate potential engine malfunctions when anomalies are detected.

## Techniques and Libraries

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

## Key Variables and Assumptions

The data used for this project comprises six key features continuously monitored to evaluate the engine's performance:
- **Engine RPM:** High RPM can indicate overheating or excessive wear, while low RPM suggests potential mechanical issues.
- **Lubrication Oil Pressure:** Low pressure may signal insufficient lubrication; high pressure can indicate blockages.
- **Fuel Pressure:** High pressure may result in poor engine performance; low pressure suggests possible fuel delivery issues.
- **Coolant Pressure:** Low pressure indicates potential leaks; high pressure may signal blockages or head gasket failure.
- **Lubrication Oil Temperature:** High temperature can degrade oil quality; low temperature might affect lubrication.
- **Coolant Temperature:** High temperature can cause overheating; low temperature may imply suboptimal operating conditions.

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

## Recommendations
Note: The recommendations and conclusions in the code are preliminary. The One-Class SVM and Isolation Forest models will be amended to fit all key features rather than using only the Principal Components. 

- **Use the Anomaly Detection Models:** Implement the developed anomaly detection models to alert engineers of potential issues before they escalate, particularly for the key features outlined above.
- **Schedule Regular Maintenance:** Conduct regular maintenance checks based on anomaly reports to ensure engine components are functioning within safe parameters.
  
While this document identifies features classified as outliers, it is crucial for a domain expert or ship engineer to verify whether these outliers are normal/expected or if they require further investigation into their context.

By adopting these recommendations, the likelihood of engine malfunctions and downtime can be significantly reduced. Proactive maintenance and timely identification of potential issues will lead to more efficient operations, decreased repair costs, and fewer engine failures. This approach not only enhances crew safety but also supports timely deliveries, improving customer satisfaction and ultimately increasing the company's profitability.

## Files Included in This Repository

- **Notebook:** A detailed Jupyter Notebook (`Anomaly Detection - Ship Engine Maintenance.ipynb`) containing the full implementation of the anomaly detection models.
- **License:** MIT License file (`LICENSE`) outlining the terms of use for this project.

### License

This project is licensed under the MIT License. See the [LICENSE](LICENCE) file for details.
