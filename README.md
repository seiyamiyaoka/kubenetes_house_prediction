[![CircleCI](https://circleci.com/gh/seiyamiyaoka/kubenetes_house_prediction.svg?style=svg)](https://circleci.com/gh/seiyamiyaoka/kubenetes_house_prediction)

## Setup the Environment

* Create a virtualenv and activate it
* Run `make install` to install the necessary dependencies
* when you setup, need lint tool. please install [hadolint](https://github.com/hadolint/hadolint)

### Running `app.py`

1. Standalone:  `python app.py` if do not work this command, `python3.7 app.py`
2. Run in Docker:  `./run_docker.sh`
3. Run in Kubernetes:  `./run_kubernetes.sh`

### Kubernetes Steps

* Setup and Configure Docker locally
* Setup and Configure Kubernetes locally
* Create Flask app in Container
* Run via kubectl

### introduction this Makefile

circleci, kubernetes, minikube etc .. commands are so long.
i write basic command to Makefile.

- minikube-start => init minikube
- check_kubenetes_deployment => confirm kubenetes deployments
- minikubeboard => open minikube dashboard
- servicestart => attach service on house-prediction cluster
- validate-circleci => check circleci/config.yml
- rub-circleci-local => execute circleci in local environment

### memo
- sklearn downgrade(because does not working library)
- docker command list https://docs.docker.com/engine/reference/commandline/docker/
