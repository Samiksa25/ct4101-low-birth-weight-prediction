# CT4101 – Low Birth Weight Prediction Using Machine Learning

## About the Project

For this project, I am using machine learning to predict whether a baby will have a low birth weight based on information about the mother and pregnancy.

A baby is considered to have a low birth weight if their birth weight is below 2,500 grams.

The main aim is to explore the data, prepare it for modelling and try different machine learning methods. I will then compare their results to see which models are better at identifying low-birth-weight cases.

## Dataset

I downloaded the **Birthweight_Smoking** dataset from the Stock and Watson website.

The dataset contains 3,000 records and 12 original variables. It includes information such as the mother's age, smoking and alcohol use, education level, prenatal visits and the baby's birth weight.

**Dataset link:**  
https://www.princeton.edu/~mwatson/Stock-Watson_3u/Students/EE_Datasets/

The dataset was provided by Douglas Almond, Kenneth Chay and David Lee.

**Research paper:**

Almond, D., Chay, K. Y. and Lee, D. S. (2005). The Costs of Low Birth Weight. *Quarterly Journal of Economics*, 120(3), 1031–1083.

## Work Completed

I started by exploring the dataset to understand its structure and check the quality of the data. The main steps I completed are:

1. Loaded the dataset using Python and pandas.
2. Checked the rows, columns and data types.
3. Checked for missing values and duplicate records.
4. Looked at unusual values and explored the different variables.
5. Created a new variable called `low_birthweight`. Babies weighing less than 2,500 grams were labelled 1, while the remaining babies were labelled 0.
6. Removed the ID and original birthweight columns from the input features.
7. Split the data into training and testing sets using an 80:20 ratio.
8. Built a Dummy Classifier as a starting point.
9. Developed Logistic Regression and Random Forest models.
10. Used GridSearchCV to find better settings for both models.
11. Compared the performance of all five models.
12. Created confusion matrices, ROC curves and Precision–Recall curves.
13. Compared the false-positive and false-negative predictions made by each model.

## Model Results

I compared five models using accuracy, precision, recall, F1-score, ROC-AUC and Average Precision.

| Model | Accuracy | Precision | Recall | F1-score |
|---|---:|---:|---:|---:|
| Dummy Classifier | 93.83% | 0.00% | 0.00% | 0.0000 |
| Logistic Regression | 71.33% | 10.98% | 51.35% | 0.1810 |
| Random Forest | 89.00% | 6.06% | 5.41% | 0.0571 |
| Tuned Logistic Regression | 72.67% | 12.43% | 56.76% | 0.2039 |
| Tuned Random Forest | 82.00% | 15.53% | 43.24% | 0.2286 |

From the results, I found that Tuned Random Forest had the highest F1-score of 0.2286. Tuned Logistic Regression had the highest recall of 56.76% and correctly identified 21 out of the 37 low-birthweight cases in the test set.

The Dummy Classifier had the highest accuracy, but it did not identify any low-birthweight cases. This helped me understand why accuracy alone is not enough to judge a model, especially when the dataset is imbalanced.

## How to Run the Project

### Requirements

Python 3 is required, along with the libraries listed in `requirements.txt`.

### Steps

1. Download or clone this repository to your computer.
2. Open a terminal in the project folder.
3. Install the required libraries by running:

   `pip install -r requirements.txt`

4. Download the Birthweight_Smoking dataset from the link provided above.
5. Place the Excel file inside the `data` folder.
6. Start Jupyter Notebook by running:

   `jupyter notebook`

7. Open `notebooks/birthweight_analysis.ipynb` and run the cells from beginning to end.

## Project Structure

```text
CT4101_Low_Birth_Weight/
│
├── data/
│   └── README.md
│
├── notebooks/
│   ├── README.md
│   └── birthweight_analysis.ipynb
│
├── reports/
├── .gitignore
├── README.md
├── requirements.txt
└── AI_Assistance_Declaration.md
```

The dataset should be downloaded separately and placed inside the `data` folder before running the notebook.

## Limitations

One of the main challenges I faced was that the dataset contains far fewer low-birthweight cases than non-low-birthweight cases. Only 6.23% of the records belong to the low-birthweight group.

The test set also contained only 37 low-birthweight cases. Because of this, the results should be interpreted carefully. The models still made incorrect predictions, including cases where they missed babies with low birth weight.

This project is for academic purposes. The models are not intended to provide medical advice or make decisions about individual pregnancies.

## Assistance Declaration

I used AI tools to help me understand parts of the project, work through some Python code and organise the project documentation. I reviewed the code and results while completing the work. Any external resources and assistance have been acknowledged in line with the module's academic integrity guidelines.