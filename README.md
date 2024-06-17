# Vaccine Prediction Project

Overview

This project aims to predict how likely individuals are to receive the XYZ and seasonal flu vaccines. Specifically, we predict two probabilities: one for the XYZ vaccine and one for the seasonal flu vaccine. The problem is formulated as a multilabel classification task.

Data Description
The dataset contains 36 columns. The first column, respondent_id, is a unique identifier. The remaining 35 features include binary, ordinal, and categorical variables:

Binary Variables: Represented as 0 (No) or 1 (Yes).
Ordinal Variables: Represent levels of concern, knowledge, and opinions with numerical values indicating intensity or degree.
Categorical Variables: Include demographic and socioeconomic attributes such as age group, education level, race, and employment status.
Target Variables
xyz_vaccine: Whether the respondent received the XYZ flu vaccine (0 = No, 1 = Yes).
seasonal_vaccine: Whether the respondent received the seasonal flu vaccine (0 = No, 1 = Yes).
Evaluation Metric
The performance is evaluated using the area under the receiver operating characteristic curve (ROC AUC) for each target variable. The overall score is the mean of these two ROC AUC scores. Higher values indicate better performance.

Files
training_set_features.csv: The dataset containing features used for training.
training_set_labels.csv: The dataset containing labels for training.
test_set_features.csv: The dataset containing features for prediction.
submission.csv: The file where the final predictions will be saved.
Instructions
Requirements
Python 3.x
pandas
numpy
scikit-learn
Steps to Run the Code
Clone the Repository

bash
Copy code
git clone https://github.com/your-repo/vaccine-prediction.git
cd vaccine-prediction
Install Dependencies

Install the required Python packages using pip:

bash
Copy code
pip install pandas numpy scikit-learn
Run the Script

The main script to preprocess the data, train the model, and generate predictions is provided in the vaccine_prediction.py file. Ensure that training_set_features.csv, training_set_labels.csv, and test_set_features.csv are in the same directory as the script.

bash
Copy code
python vaccine_prediction.py
Output

The script will output the ROC AUC scores for the XYZ and seasonal flu vaccines and save the predictions to submission.csv.
