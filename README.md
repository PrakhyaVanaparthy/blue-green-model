# blue-green-deployment model

## Project Overview
In this project we need to work in aws to acheive the following:
Using Jenkins to implement Continuous Integration and Continuous Deployment
Building pipelines
Working with Ansible and CloudFormation to deploy clusters
Building Kubernetes clusters
Building Docker containers in pipelines

## Create Cluster
Once you have your Jenkins and AWS environments setup you will need to first run my #Create cluster pipeline# which can be found [here](https://github.com/sushma-sri/cluster-pipeline) 

## Branches
### Master:
- Lint HTML
- Build Docker Image
- Push Docker Image
- Set Kubectl Context to Cluster

### Blue:
- Lint HTML
- Build Docker Image
- Push Docker Image
- Set Kubectl Context to Cluster
- Create Blue Controller
- Create Green Controller
- Create Blue-Green service

### Green:
- Lint HTML
- Build Docker Image
- Push Docker Image
- Set Kubectl Context to Cluster
- Create Blue Controller
- Create Green Controller
- Create Blue-Green service

## Pipeline stages

### Lint HTML
This step is used to makes sure there is no syntax error in the .html files
### Build Docker Image
This step builds a new docker image of the website

### Push Docker Image
This step uploads the new docker image to [DockerHub](https://cloud.docker.com) 

### Set Kubectl Context to Cluster
This step switches to the correct cluster using the following command `kubectl config use-context arn:aws:eks:ap-southeast-2:984760320768:cluster/capstonecluster` 

### Create Blue Controller
This step creates the blue controller using the following command `kubectl apply -f ./blue-controller.json`

### Create Green Controller
This step creates the green controller using the following command `kubectl apply -f ./green-controller.json`

### Create Blue-Green service
This steps applies the change to load balancer by running `kubectl apply -f ./blue-green-service.json`

