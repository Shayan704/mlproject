# Machine Learning Project: Student Performance Analysis and Prediction

## Introduction
Student performance analysis and prediction using datasets has become an essential component of modern education systems. With the increasing availability of data on student demographics, academic history, and other relevant factors, schools and universities are using advanced analytics and machine learning algorithms to gain insights into student performance and predict future outcomes.

## Motivation
The motivation behind this project stems from the need to enhance educational outcomes by identifying areas of improvement, personalizing learning experiences, and providing targeted support to struggling students. By leveraging data-driven insights, educators can make informed decisions that help students achieve their full potential. Additionally, this approach aids school administrators and policymakers in allocating resources more effectively, ensuring that interventions are timely and impactful.

## Problem Statement
Accurately predicting student performance is challenging due to the complex interplay of various factors such as socio-economic background, learning habits, and psychological factors. Traditional methods of assessment often fail to capture these nuances, leading to suboptimal educational interventions. This project aims to address this issue by developing a robust machine learning model that can predict student performance with high accuracy, enabling educators to implement more effective and personalized educational strategies.

## Features
- Data preprocessing and visualization
- Exploratory data analysis (EDA)
- Model building and evaluation
- Performance prediction

## Tools and Technologies
- **Python**
- **Pandas**
- **NumPy**
- **Scikit-learn**
- **Matplotlib**
- **Seaborn**
- **CatBoost** (specific information stored in `catboost_info`)

## Data
The dataset used in this project includes various student-related features such as demographic factors, social influences, and academic performance indicators.

## Project Structure
The project is organized into the following directories:

```plaintext
notebook/
    catboost_info/               # Information related to CatBoost models
    data/
        1. EDA STUDENT PERFORMANCE.ipynb  # Notebook for Exploratory Data Analysis (EDA)
        2. MODEL TRAINING.ipynb           # Notebook for Model Training
src/
    components/                   # Reusable components for the project
    logs/                         # Log files for tracking execution
    pipeline/
        __init__.py               # Initialization for the pipeline package
        predict_pipeline.py       # Pipeline for model prediction
        train_pipeline.py         # Pipeline for training the model
    __init__.py                   # Initialization for the main src package
    exception.py                  # Custom exception handling
    logger.py                     # Logging setup
    utils.py                      # Utility functions
templates/
    home.html                     # HTML file for the home page
    index.html                    # HTML file for index page
venv/                             # Virtual environment files (not tracked in Git)
.github/
    workflows/
        main.yaml                 # Workflow configuration for CI/CD
artifacts/
    model.pkl                     # Pickled model file
    preprocessor.pkl              # Pickled preprocessor file
    raw.csv                       # Raw data file
    test.csv                      # Test data file
    train.csv                     # Training data file
.gitignore                        # Files and directories to be ignored by Git
app.py                            # Main application entry point
Dockerfile                        # Dockerfile for containerizing the application
README.md                         # Project documentation
requirements.txt                  # Python dependencies
setup.py                          # Setup script for packaging
```

## Installation

### 1. Create a Conda Environment
Ensure you have Conda installed. Then, create and activate a conda environment with Python version 3.8:

```bash
conda create --name myenv python=3.8
conda activate myenv
```

### 2. Clone the Repository
Clone the repository from GitHub:

```bash
git clone https://github.com/Shayan704/mlproject.git
cd mlproject
```

### 3. Install Required Packages
Use the following command to install the dependencies:

```bash
pip install -r requirements.txt
```

## Usage

- **Data Exploration and Model Training**: Open and run the Jupyter notebooks provided in the `notebook` directory to explore the data and train the models.
- **Model Deployment**: To deploy the models, use Flask and Gunicorn. You can set up a server to serve your models for predictions.

### Run the Application
Use the following command to run the project:

```bash
python app.py
```

## CI/CD with GitHub Actions

This project uses CI/CD pipelines and is built in a completely modular way. It uses GitHub Actions for continuous integration and deployment. To enable this, add the following GitHub secrets to your repository:

- `DOCKERHUB_PASSWORD`
- `DOCKERHUB_USERNAME`
- `RENDER_API_KEY`
- `RENDER_SERVICE_ID`

These secrets are required to ensure the CI/CD pipeline can build, test, and deploy your application automatically.

The project is deployed and can be accessed live at [Student Performance Prediction](https://student-marks-prediction-0mks.onrender.com).
**Note:** Before accessing the deployed project, please reach out via email at **shayanmandal100@gmail.com** to request the project activation. This will ensure the deployment is up and running for your use.