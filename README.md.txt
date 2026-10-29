 CT4101 – Low Birth Weight Prediction

## About the Project

This project focuses on predicting whether a baby will have a low birth weight based on information about the mother and her pregnancy. For this project, low birth weight means a birth weight of less than 2,500 grams.

The aim is to explore the dataset, prepare the data for analysis and build a basic model to see how well it can identify low-birth-weight cases.

## About the Dataset

The dataset contains 3,000 records and 12 original columns. It includes information such as the mother's age, smoking and alcohol use, education level, and number of prenatal visits.

Before building the model, I checked the dataset for missing values, duplicate records, unusual values and the distribution of the target variable.

## Work Completed

The following steps have been completed so far:

1. Loaded the dataset using Python and pandas.
2. Checked the number of rows and columns and examined the data types.
3. Checked for missing values and duplicate records.
4. Created a new target variable called `low_birthweight`, where 1 represents a birth weight below 2,500 grams and 0 represents all other cases.
5. Selected the input variables and excluded the original birth weight column to avoid data leakage.
6. Split the data into training and testing sets.
7. Built a baseline model and evaluated its performance.

## Baseline Model Results

The baseline model achieved the following results on the test data:

- **Accuracy:** 93.83%
- **Precision:** 0.00
- **Recall:** 0.00
- **F1-score:** 0.00

Although the accuracy is high, the model predicted every case as non-low birth weight. It failed to identify any of the low-birth-weight cases in the test set.

This shows that accuracy alone does not give a clear picture of model performance when the dataset has an imbalanced target variable. These results will be used as a starting point when evaluating other models.

## How to Run the Project

### Requirements

Python 3 and the packages listed in `requirements.txt` are needed to run the project.

### Steps

1. Download or clone this repository to your computer.
2. Open a terminal in the project folder.
3. Install the required packages by running:

   `pip install -r requirements.txt`

4. Make sure the dataset is available in the location specified in the notebook.
5. Start Jupyter Notebook by running:

   `jupyter notebook`

6. Open the project notebook and run the cells from beginning to end.

## Preprocessing and Data Splitting

The target variable was created using the birth weight column. The original birth weight column was then excluded from the input features because it was used to define the target.

The dataset was split into 80% training data and 20% testing data. Stratified sampling was used to keep the proportion of low-birth-weight and non-low-birth-weight cases similar in both sets. A fixed random state of 42 was used to make the split reproducible.

The notebook contains the data audit, preprocessing steps, baseline model and evaluation results.

## Assistance Declaration

AI tools were used to help me understand the project requirements, work through parts of the Python code and organise the project documentation. I reviewed the code and results as part of my work. Any assistance and external resources are acknowledged in accordance with the module's academic integrity guidelines.