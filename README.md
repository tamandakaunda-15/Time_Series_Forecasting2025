# Air Quality Forecasting in Beijing

## Project Overview

This project applies **Recurrent Neural Networks (RNNs)** and **Long Short-Term Memory (LSTM)** models to forecast PM2.5 concentrations in Beijing. Utilizing historical air quality and weather data, the goal was to build a robust and generalizable forecasting model.

The development process, documented as part of the **Machine Learning Techniques I course**, involved a deep dive into debugging and correcting severe overfitting.

## Key Project Learnings & Outcomes

**Diagnosing and Overcoming Overfitting:**

The project highlighted a critical machine learning challenge: building a model that generalizes well beyond its training data. Our initial low local RMSE was misleading, as revealed by a high, inconsistent score on the Kaggle leaderboard. This led to a systematic debugging effort.

**Model Stability and Generalization:**

We transitioned from an unstable, overly complex stacked LSTM architecture with an incorrect `ReLU` activation to a simpler, more robust **single-layer LSTM** with **`Dropout`** and **`EarlyStopping`**. This strategic simplification resulted in a more stable and reliable model.

**Preprocessing is Paramount:**

The experience reinforced the foundational importance of a meticulous preprocessing pipeline. Critical fixes included:
*   Avoiding **data leakage** during scaling.
*   Correctly handling the `datetime` column.
*   Implementing a robust **iterative prediction loop** for the test set.

## Repository Structure

air_quality_forcasting/

├── data/

│ ├── train.csv

│ └── test.csv

├── notebooks/

│ └── air_quality_forecasting_report.ipynb

├── outputs/

│ ├── best_model.keras

│ └── submission.csv

├── README.md

└── .gitignore


## Instructions for Reproduction

**1. Setup Environment**

The project was developed in a Google Colab environment. The required libraries can be installed from the notebook.

The data files must be placed in a `data/` subdirectory within the project root.

**Action Required:** File paths in the notebook need to be updated. Modify paths like `/content/drive/MyDrive/air_quality_forcasting/` to point to your local or Colab `data/` directory.

**2. Running the Code**

Open `air_quality_forecasting_report.ipynb` in your Jupyter environment.

Execute all cells in order. The notebook will:
*   Load and preprocess the data, including handling non-stationarity.
*   Define and train the refined LSTM model.
*   Save the best model to the `outputs/` directory.
*   Use the saved model to generate predictions on the test set.
*   Create the final `submission.csv` file.

**3. Kaggle Submission**

The notebook generates a `submission.csv` file in the `outputs/` directory, correctly formatted for Kaggle. Use this file for your final submission.

## Acknowledgements

This project benefited from resources provided during the Machine Learning Techniques I course. We also thank the creators of the open-source libraries `pandas`, `NumPy`, `TensorFlow`, and `Scikit-learn` for their invaluable contributions to the machine learning community.

## License
