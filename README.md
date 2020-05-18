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


