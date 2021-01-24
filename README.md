# kubernetes project - machine learning prediction model

[![yashkankane007](https://circleci.com/gh/yashkankane007/kubernetes_project_udacity

.svg?style=svg)](https://app.circleci.com/pipelines/github/yashkankane007/kubernetes_project_udacity/3/workflows/f9b7f898-5321-4402-8b37-8ba29b7b4765/jobs/3)

## Description

The project is a Machine Learning based Micro-service to **predict the housing prices of a given city based on certain parameters**. This model is developed using python and its various pre-defined modules and converted to a web service using `flask`. One of the APIs `/predict` accepts a json as input, calculates the pricing and returns the predicted value. The project is configured and containerized to make it deployable in a Kubernetes cluster.

## Setup Instructions

You can run the below commands in sequence (after creating a virtual environment) to get it up and running in your local machine.

* `make install` to install the required dependencies
* install **docker, minikube and hadolint** separately
* configure docker and kubernetes (via minikube)
* `make lint` to check for any linting issues
* `python app.py` to run the model locally
* `./run_docker.sh` to build and run the container using project files
* `./run_kubernetes.sh` to deploy and run project using docker image
* `./make_prediction.sh` to test the model with sample values

## Project structure

The root folder contains most of the files critical for the application.

* The `app.py` contains the main code and developed using python.
* The `Dockerfile` contains the instructions to create an image for running our application
* The `Makefile` contains the set of commands that can be run in a batch to set up the environment.
* The `requirements.txt` contains all the python modules that needs to be installed before starting our application
* The `model_data` folder contains certain input values that are used to train our model.
* The `.circleci` folder configures our project for pipeline deployement


*Thanks for checking out my project!*