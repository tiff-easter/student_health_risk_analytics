# student_health_risk_analytics
About this Project
This project is a comparative bias audit. The goal was to evaluate a simulated student health dataset against a real-world benchmark (the MIT Student Health Dataset) to identify discrepancies in how stress, sleep, and physiological markers are represented across gender demographics.

The Dataset
Simulated Data: A custom-generated dataset focusing on student wellness metrics.Benchmark Data: MIT Student Health and Wellness dataset.

Key Variables: sleep_hours, heart_rate, stress_self_report, and gender_bin (Binary encoded: Male=0, Female=1).

The Problem: Synthetic data is a powerful tool used for training machine learning models, but it often lacks the messy nuances of human biology and variability.  If these models are biased, particularly regarding gender or physiological reporting, they can lead to inaccurate health risk assessments. 

Visualizations & Analysis

1. Sleep Distribution by Gender
We used Seaborn Box Plots to analyze the spread of sleep data. This allowed us to visualize the median sleep hours and the variance (whiskers) to ensure the simulation wasn't producing "too-perfect" or uniform results.

2. Physiological Correlations
A Scatter Plot with Linear Regression was utilized to track the relationship between sleep deprivation and heart rate.Finding: The simulation correctly identifies a negative correlation (as sleep decreases, heart rate increases), confirming that the physiological logic of the model is sound.

3. The Bias Audit (Simulation vs. Benchmark)
The core of the project was a side-by-side comparison of average stress scores.

Key Audit Finding: 
The simulation exhibits a "Pessimistic Bias," over-projecting stress levels by roughly 45%. Furthermore, it flipped the gender stress gap found in the MIT data, suggesting a need for recalibration in the simulation's demographic weights.

Technologies Used
Python (Pandas, Matplotlib, Seaborn)
Jupyter Notebooks
Data Normalization & Binary Encoding

