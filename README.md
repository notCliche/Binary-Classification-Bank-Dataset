# Bank Term Deposit Subscription Prediction
## Project Overview
This project is a part of Kaggle 2025 Playground series. It aims to predict whether a client will subscribe to a bank term deposit. The bank_prediction.py script uses a Random Forest Classifier model to handle data preprocessing, model training, and prediction, generating a submission file in the required format.

## Dataset
The data is provided in three CSV files, all present in [`csv_files.zip`](csv_files.zip):
- `train.csv`: The training set containing client data and the target variable y (1 for subscribed, 0 for not subscribed).
- `test.csv`: The test set for which predictions need to be made.
- `sample_submission.csv`: A file showing the correct submission format.

The dataset contains a mix of numerical and categorical features describing client demographics, campaign interaction, and previous campaign outcomes.

## Approach
The solution employs the following steps:
- **Data Loading:** The script loads the `train.csv` and `test.csv` datasets using pandas.
- **Preprocessing:** Categorical features are converted into a numerical format using one-hot encoding (`pd.get_dummies`). This is a crucial step for machine learning models that require numerical input. The script also ensures that the feature columns in the training and test sets are perfectly aligned after encoding.
- **Modeling:** A Random Forest Classifier is trained on the preprocessed training data.
- **Prediction:** The trained model predicts the subscription probability for each client in the test set.
- **Submission:** The predictions are saved to a submission.csv file with two columns: `id` and `y`, ready for upload to Kaggle.

## How to Run
#### 1. Prerequisites:
You will need Python 3 and the following libraries: `numpy`, `pandas` and `scikit-learn`
#### 2. Installation:
Install the required libraries using pip:
```
pip install pandas scikit-learn numpy
```
#### 3. Running the Script
- Place bank_prediction.py in the same directory as the CSV data files.
- Run the notebook [`bank-predictor.ipynb`](bank-predictor.ipynb) directly in a notebook IDE like Jupyter Notebook, Google Colab etc.
#### 4. Output
Progress is printed in the output, and a `submission.csv` file is generated, ready for submission to Kaggle.
## Author
Om Prakash Behera
