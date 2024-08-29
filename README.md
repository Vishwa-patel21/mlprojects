# End-to-End Machine Learning Project

## Project Overview

This project demonstrates an end-to-end machine learning pipeline, covering data preprocessing, model training, evaluation, and deployment. The project is structured to provide a comprehensive guide for building and deploying machine learning models.

## Table of Contents

1. [Project Structure](#project-structure)
2. [Installation](#installation)
3. [Usage](#usage)
4. [Dataset Description](#dataset-description)
5. [Model Training and Evaluation](#model-training-and-evaluation)
6. [Deployment](#deployment)

## Project Structure

```
├── .ebextensions            # Configuration files for Elastic Beanstalk (if any)
├── .github                  # GitHub workflows and actions
├── .gitignore               # Git ignore file
├── README.md                # Project README file
├── application.py           # Flask application entry point
├── artifacts                # Directory to store models and other artifacts
├── catboost_info            # CatBoost-related files
├── notebook                 # Jupyter notebooks for exploration and experimentation
├── requirements.txt         # Python dependencies
├── setup.py                 # Project setup file
├── src                      # Source code for data processing and model building
├── templates                # HTML templates for the web app
```


## Installation

To get started with this project, clone the repository and install the required dependencies.

```bash
git clone https://github.com/Vishwa-patel21/mlprojects.git
cd mlprojects
pip install -r requirements.txt
```


## Usage

### Running the Web Application

To run the Flask web application locally:
```bash
python application.py
```
The app will be available at [http://127.0.0.1:5000/](http://127.0.0.1:5000/).


## Dataset Description

This section describes the dataset used in the project.

- **Dataset Name**: Student Performance Data
- **Source**: Kaggle
- **Description**: This dataset contains information about students, including their demographic information, parental education level, lunch type, test preparation course completion, and their scores in math, reading, and writing.

### Features:

- `gender`: The gender of the student (e.g., female, male).
- `race_ethnicity`: The race/ethnicity group of the student (e.g., group A, group B).
- `parental_level_of_education`: The highest level of education attained by the student's parents (e.g., bachelor's degree, some college).
- `lunch`: The type of lunch received by the student (e.g., standard, free/reduce).
- `test_preparation_course`: Whether the student completed a test preparation course (e.g., none, completed).
- `math_score`: The score obtained by the student in the math test.
- `reading_score`: The score obtained by the student in the reading test.
- `writing_score`: The score obtained by the student in the writing test.

## Model Training and Evaluation

This project involves training and evaluating various machine learning models to predict student performance based on a given dataset. The process is detailed in the accompanying Jupyter notebooks.

### Data Import and Setup

We begin by importing essential libraries, including Pandas, Numpy, Matplotlib, and Seaborn, along with several machine learning libraries such as `sklearn`, `CatBoost`, and `XGBoost`. The dataset is loaded into a Pandas DataFrame for further analysis.

### Model Training

We trained the following models:

- **K-Nearest Neighbors (KNN)**
- **Decision Tree Regressor**
- **Random Forest Regressor**
- **AdaBoost Regressor**
- **Support Vector Regressor (SVR)**
- **Linear Regression, Ridge, and Lasso**
- **CatBoost Regressor**
- **XGBoost Regressor**

Each model was carefully tuned using `RandomizedSearchCV` to optimize performance.

### Model Evaluation

The models were evaluated using the following metrics:

- **R² Score**: Measures how well the model explains the variance in the target variable.
- **Mean Squared Error (MSE)**: Indicates the average squared difference between the predicted and actual values.
- **Mean Absolute Error (MAE)**: Represents the average absolute difference between predicted and actual values.

These metrics helped us select the best-performing model for our dataset.

### Hyperparameter Tuning

Hyperparameters were fine-tuned using `RandomizedSearchCV` to enhance model accuracy and generalization.

For detailed code and execution steps, please refer to the Jupyter notebooks in this repository.

## Deployment

The trained machine learning model has been deployed using Microsoft Azure, providing a scalable and reliable solution for predicting student performance.

You can access the deployed model and make predictions using the following URL:

[Student Performance Prediction App](https://studentperformanceapp-c0fngqaydybbg2hf.eastus-01.azurewebsites.net/)



