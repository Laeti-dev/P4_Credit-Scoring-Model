# Project4-Credit-Scoring-Model
Credit Scoring Model with Feature Engineering and Model Interpretability


## Summary
The goal of this project is to develop a credit scoring model for a consumer credit company. The model should be interpretable and include a measure of variable importance. The project follows a professional scenario, where, as a Data Scientist, I will work on building and evaluating different machine learning models in order to create a reliable credit scoring model.

## Business Objectives:
The business objective is to develop a credit scoring model that can effectively assess the creditworthiness of customers. This model will assist the company in making informed decisions on granting credit and managing risk. The model needs to be interpretable, meaning that the factors influencing the credit score should be clearly understood.

## Learning Objectives:
- supervised learning,
- categorical variable transformation,
- linear and non-linear model testing,
- feature engineering,
- model evaluation,
- model interpretability.


## Keywords
data analysis, feature engineering, model optimization, interpretability.

# How to run the notebook
## Use the notebook in colab
To use the notebook in colab, you need to load your data csv file in the /content directory

## Create a virtual environment (recommanded)
As Docker container doesn't offer enough capacities to run the notebook, I recommand to create a virtual environment directly
```bash
  python3 -m venv venv
  source venv/bin/activate
  pip install -r requirements.txt
```
## Build a Docker container


```bash
  docker build -f .devcontainer/Dockerfile -t my-container .
```
Note : the -f flag is to indicate that we are passing the path to Dockerfile


```bash
  docker run -it -p 8888:8888 -v $(pwd):/workspace my-container
```
Note : -it is for interactive and tty ; -p is to pass the port to use ; -v isto bind the directory on the host to a directory in the container
