# Time_Series_Forecasting2025

Project Title: Air Quality Forecasting in Beijing
Project Overview


This project applies Recurrent Neural Networks (RNNs) and Long Short-Term Memory (LSTM) models to forecast PM2.5 concentrations in Beijing. It utilizes historical air quality and weather data to build a robust and generalizable forecasting model, documented as part of the Machine Learning Techniques I course.


Repository Structure
*data*/: Contains the raw dataset files (train.csv and test.csv).
*notebooks*/: Includes the Jupyter notebooks used for the analysis, including the final report notebook.
*outputs*/: Stores the final model file (best_model.keras) and the Kaggle submission file (submission.csv).
src**/: Contains any reusable Python scripts.
*README.md*: This file, providing an overview of the project. 


##Instructions for Reproduction


1. Setup Environment
The project was developed in a Google Colab environment. The required libraries are listed in the notebook.
The data files must be placed in a data/ subdirectory within the project root.
The notebook is configured to load data from /content/drive/MyDrive/air_quality_forcasting/. To reproduce the results, please modify the pd.read_csv() file paths in the notebook to point to your local or Colab data/ directory.


 
3. Running the Code
Open air_quality_forecasting_final_report.ipynb in your Jupyter environment.
Execute all cells in order. The notebook will:
Load and preprocess the data.
Define and train the LSTM model.
Save the best model to the outputs/ directory.
Use the saved model to generate predictions on the test set.
Create the final submission.csv file. 
4. Generating Submissions for Kaggle
Data Preparation: The notebook includes all necessary data preparation steps.
Prediction: The trained model is used to generate predictions.
Submission File: A submission.csv is generated in the outputs/ directory, formatted according to the Kaggle requirements.
Key Insights from the Project
Model Stability: The project's development involved a critical debugging process to address severe overfitting.
Generalization: The final model, a single-layer LSTM with Dropout and EarlyStopping, demonstrated improved generalization compared to earlier flawed and overly complex architectures.
Preprocessing Importance: Proper data handling, including preventing data leakage and correctly formatting time-series data, was found to be crucial for achieving a reliable model.


GitHub Repository Link

License:
MIT License
