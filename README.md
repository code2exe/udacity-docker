[![<code2exe>](https://circleci.com/gh/code2exe/udacity-docker.svg?style=svg)](https://circleci.com/gh/code2exe/udacity-docker)

# Udacity Cloud DevOps Engineer Nanodegree, Project IV: Operationalize a Machine Learning Microservice API

This project tests the ability to apply the skills acquired in the nanodegree course to operationalize a Machine Learning Microservice API.

A model that has been pre-trained to predict housing prices in Boston according to several factors is given and the task is to operationalize/deploy it using containerization technologies like Docker and Kubernetes.

## Steps:

- **Setup the environment**: (I am on Amazon Linux with python 3 installed)
  1. `git clone https://github.com/code2exe/udacity-docker.git`
  2. `cd udacity-docker`
  3. `python3 -m venv ~/.udocker`
  4. `source ~/.udocker/bin/activate`
- **Running app.py**: (Ensure that Docker and Kubectl with Minikube are properly installed)
  - Run with Docker: `./run_docker.sh`
  - Run with Kubernetes: 
    - `minikube start`
    - `.\run_kubernetes.sh`

## Contents of the Repository:

- `.circleci` - CircleCI intergration for testing
- `model_data`- Contains pre-trained model data
- `output_txt_files`- Contains log output
- `Dockerfile` - Docker configuration
- `Makefile`- Makefile for local testing
- `app.py` - Our Flask app
- `make_prediction.sh`- Contains the payload to generate our prediction
- `run_docker.sh` - A script to automate our docker deployment
- `run_kubernetes`- A script to automate our Kubernetes deployment
- `upload_docker`- A script to build and push our Docker container to Dockerhub