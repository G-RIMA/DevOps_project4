[![CircleCI](https://dl.circleci.com/status-badge/img/gh/G-RIMA/DevOps_project4/tree/main.svg?style=svg)](https://dl.circleci.com/status-badge/redirect/gh/G-RIMA/DevOps_project4/tree/main)

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

---jobs

## Setup the Environment

* Create a virtualenv with Python 3.7 and activate it. Refer to this link for help on specifying the Python version in the virtualenv. 
```bash

## Solution
For this project I had to complete the tasks above and I did the following:

## Task 1
Created a cloud9 environment in AWS
Downloaded the files from the souce code and then created my own repository and uploaded the files
I then cloned my repository on to cloud 9

python3 -m pip install --user virtualenv
# You should have Python 3.7 available in your host. 
# Check the Python path using `which python3`
# Use a command similar to this one:
python3 -m virtualenv --python=<path-to-Python3.7> .devops
source .devops/bin/activate
```
* Run `make install` to install the necessary dependencies

### Running `app.py`

1. Standalone:  `python app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

Installed dependencies via project Makefile. Many of the project dependencies are listed in the file requirements.txt; these can be installed using pip commands in the provided Makefile. While in your project directory, type the following command to install these dependencies.
make install

### Then Installed Hadolint
By adding the link to install hadolint in make file and its was installed using the make file 

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

I run make install and my environment was complete

### Completed the Docker file:
I specified a working directory
Copy the app.py source code to that directory
Install any dependencies in requirements.txt (do not delete the commented # hadolint ignore statement).
Expose a port when the container is created; port 80 is standard.
Specify that the app runs at container launch.

### Task 2: Run a Container & Make a Prediction
I completed the run_docker.sh file
and then run it
i then in a separate terminal run make_prediction and got the desired output

## Task 3: Improve Logging & Save Output
Added a prediction log statement in app.py
Run the docker and the make prediction files
Then added the output in docker_out.txt
And took a screenshot of the result

## Task 4
completed the upload_docker.sh
addded the docker login to ask for my credentials when running
i the run bash upload_docker.sh and uploaded the image. I then took a screenshot

## Task 5 and 6 I did together
 I configured the minikube by running minikube start
 then completed the run_kubernetes.sh
 Then run bash run_kubernetes.sh and added the output to kuberenetes_out.txt
 
 ## Task 8 
 added .circleci/ config file
 added the provided config.yml file 
 then commited the file
 Then in CircleCI i setup the project and waited to see if the build would fail
 The build was successful
 went to project settings and copied the badge mark up and added to the README files
 
 ## Task 7
 I deleted the cluster and deleted the cloud 9 environment
 
 ### FILES
 * .circleci - containd the circleci config.yml file that tests the project
 * Dockerfile - file that runs the docker container
 * Makefile - contains the dependencies needed to install and installs them by running
            make install
 * app.py - contains the flask up and added a logging 
 * Improve Logging and save output.jpg - image of the output provided after logging
 * docker_out.txt - has the text shown by the output provided after improving logging
 * hadolint- the installed handolint acctivated by running make lint
 * resize.sh - helps to resize
 * run_docker - runs docker by using bash run_docker.sh
 * upload_docker.sh - uploads docker image when you run bash upload_docker.sh
 * run_kubernetes.sh - deploys the kuberenetes and output is saved u run it by bash run_kubernetes
 * kubernetes.txt - the output of deploying kubernetes is saved here
 
