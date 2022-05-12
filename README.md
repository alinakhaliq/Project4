[![CircleCI](https://circleci.com/gh/alinakhaliq/Project4/tree/main.svg?style=svg)](https://circleci.com/gh/alinakhaliq/Project4/tree/main)

## Project Overview

In this project, you will apply the skills you have acquired in this course to operationalize a Machine Learning Microservice API. 

You are given a pre-trained, `sklearn` model that has been trained to predict housing prices in Boston according to several features, such as average rooms in a home and data about highway access, teacher-to-pupil ratios, and so on. You can read more about the data, which was initially taken from Kaggle, on [the data source site](https://www.kaggle.com/c/boston-housing). This project tests your ability to operationalize a Python flask app—in a provided file, `app.py`—that serves out predictions (inference) about housing prices through API calls. This project could be extended to any pre-trained machine learning model, such as those for image recognition and data labeling.

### Project Tasks

Your project goal is to operationalize this working, machine learning microservice using [kubernetes](https://kubernetes.io/), which is an open-source system for automating the management of containerized applications. In this project you will:
* Test your project code using linting
* Complete a Dockerfile to containerize this application
* Deploy your containerized application using Docker and make a prediction
* Improve the log statements in the source code for this application
* Configure Kubernetes and create a Kubernetes cluster
* Deploy a container using Kubernetes and make a prediction
* Upload a complete Github repo with CircleCI to indicate that your code has been tested

You can find a detailed [project rubric, here](https://review.udacity.com/#!/rubrics/2576/view).

**The final implementation of the project will showcase your abilities to operationalize production microservices.**

---

### Files contained

.circleci/config.yml contains circle ci jobs and builds<br/>
Docker_out.txt - contains terminal output from running ./run_docker.sh<br/>
Kubernetes_out.txt - contains terminal output from running ./run_kubernetes.sh<br/>
Dockerfile - contains instructions to build docker image<br/>
Makefile - installs the dependencies for the project<br/>
app.py - source code which also contains an additional prediction log statement<br/>
Make_prediction.sh - sends input data to the containerised port via the port listed<br/>
Requirements.txt - includes project dependencies<br/>
Run_docker.sh - contains instructions to run and build the docker image outlined in the Dockerfile<br/>
Run_kubernetes.sh - deploys the application to kubernetes<br/>
Upload_docker.sh - uploads the built image to docker<br/>

### Setup the Environment

Change to working directory
python3 -m venv ~/.devops
source ~/.devops/bin/activate
make install <- to install dependencies
install docker
brew install hadolint <- install hadolint on mac
brew install virtualbox --cask <- install virtual box on mac
install minikube following instructions: https://minikube.sigs.k8s.io/docs/start/

### Running app.py

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

