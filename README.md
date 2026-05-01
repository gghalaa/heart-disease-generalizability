# Heart Disease Generalizability Project

A data science and machine learning project that evaluates how well heart disease prediction models generalize across different patient populations. The project uses the UCI Heart Disease dataset and compares internal validation with external cross-cohort validation to study the impact of distribution shift on model performance.

## Dataset

The project uses the UCI Heart Disease dataset.

Dataset link: https://archive.ics.uci.edu/dataset/45/heart+disease

The dataset includes four cohorts:

- Cleveland
- Hungary
- Switzerland
- VA Long Beach

These cohorts represent different patient populations, making the dataset useful for evaluating model generalizability across heterogeneous populations.

## Project Aim

The main aim of this project is to evaluate whether machine learning models that perform well on one population can maintain reliable performance when tested on different populations.

The project focuses on:

- Internal validation within the same cohort
- External validation across different cohorts
- Cross-cohort model performance
- Distribution shift between patient populations
- Comparison between simple and complex machine learning models

## Research Questions

### RQ1

How does the predictive performance of heart disease models differ when they are trained and tested on the same cohort compared to when they are trained and tested on different cohorts?

### RQ2

How does model performance change when models trained on merged cohorts are evaluated on external cohorts?

### RQ3

Which machine learning model generalizes better across different patient populations?

## Hypotheses

### H1

Models will show higher performance under internal validation than external validation.

### H2

Model performance will decrease when evaluated on external cohorts due to distribution shift.

### H3

Ensemble-based models will be more robust than simpler linear models across populations.

## Methods

The project follows a complete machine learning workflow:

- Data collection from the UCI Heart Disease dataset
- Data cleaning and preprocessing
- Missing value handling
- Feature validation
- Outlier analysis
- Exploratory data analysis
- Model training
- Internal validation
- External validation
- Model comparison

## Preprocessing Steps

The preprocessing stage includes:

- Converting columns to numeric format
- Handling invalid categorical values
- Removing inconsistent entries
- Creating a binary target variable
- Handling missing numerical values using median imputation
- Handling missing categorical values using most frequent value imputation
- Applying feature scaling to numerical variables
- Applying one-hot encoding to categorical variables
- Using a preprocessing pipeline to avoid data leakage

## Machine Learning Models

The project compares two machine learning models:

### Logistic Regression

Logistic Regression was used as a baseline model because it is simple, interpretable, and commonly used in medical prediction tasks.

### Random Forest

Random Forest was used as an ensemble-based model because it can capture nonlinear patterns and feature interactions.

## Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- ROC-AUC

These metrics were used to compare performance under both internal and external validation settings.

## Key Findings

The main findings of the project include:

- Internal validation generally produced higher performance than external validation.
- External validation showed a noticeable performance drop across cohorts.
- Distribution shift affected model generalization across patient populations.
- Logistic Regression showed more stable performance across external cohorts.
- Random Forest showed greater sensitivity to cohort differences.
- The results supported H1 and H2.
- The results contradicted H3 because Random Forest did not generalize better than Logistic Regression.

## Technologies Used

- Python
- Jupyter Notebook
- pandas
- NumPy
- scikit-learn
- matplotlib
- seaborn

## Project Structure

    heart-disease-generalizability/
    ├── notebook/
    │   └── DS_Project.ipynb
    ├── paper/
    │   └── Evaluating the Generalizability of Heart Disease Prediction Models Across Heterogeneous Populations.pdf
    ├── presentation/
    │   └── DS Presentation.pdf
    ├── references/
    │   └── DS Table.pdf
    └── README.md

## Main Files

- `DS_Project.ipynb` - Main Jupyter Notebook containing data preprocessing, EDA, model training, and evaluation
- `Evaluating the Generalizability of Heart Disease Prediction Models Across Heterogeneous Populations.pdf` - Final research paper
- `DS Presentation.pdf` - Project presentation slides
- `DS Table.pdf` - Reference and dataset information table
- `README.md` - Project overview and instructions

## How to Run the Project

1. Clone or download this repository.
2. Open the project folder.
3. Open the Jupyter Notebook file:

    `notebook/DS_Project.ipynb`

4. Install the required Python libraries if needed:

    `pip install pandas numpy scikit-learn matplotlib seaborn`

5. Download the dataset from the UCI Machine Learning Repository:

    https://archive.ics.uci.edu/dataset/45/heart+disease

6. Run the notebook cells in order.

## Notes

- This project focuses on evaluating model generalization, not only achieving high accuracy.
- The dataset contains multiple cohorts, which allows cross-cohort validation.
- External validation is important because internal validation may overestimate real-world model performance.
- The project highlights the effect of distribution shift in healthcare machine learning.
- The results suggest that simpler models may sometimes generalize better than more complex models.
