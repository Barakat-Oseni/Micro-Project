# ALT SCHOOL CLOUD ENGINEERING 3RD SEMESTER EXAMINATION PROJECT

# An utility service app that uploads/download images and files.

This is an utility service app that handles uploads/downloads of images and files.


## Tools used and Required

* Git Actions
* Docker and dockerhub
* Kubernetes
* Git and Github
* Maven
* Helms Chart


## Infrastructure and Deployment Automation

This project entails developing a single microservice-based application, packaging the application using Helm, and deploying it via CI/CD pipeline. The pipeline is meant to utilize Helm Charts for the deployment of the application.


## CI/CD Pipeline

CI/CD was implemented for this project using Git Actions.  

# Creating Helm Charts and installations

helm create emp-helm-charts

# Helm install
# dry run

helm template emp-helm-charts # you'll see the actual yaml files
helm install helm-release emp-helm-charts
helm list
helm history helm-release
kubectl get pod
kubectl --namespace default port-forward $POD_NAME 8080:8080
http://localhost:8080/v1/service

# Helm Upgrade to revision 2 


helm upgrade helm-release emp-helm-charts
helm list
helm history helm-release
kubectl get pod
kubectl --namespace default port-forward $POD_NAME 8080:8080
http://localhost:8080/v2/service

# with Helm Rollback to revision 1
helm rollback helm-release 1
helm list
helm history helm-release
kubectl get pod
kubectl --namespace default port-forward $POD_NAME 8080:8080
http://localhost:8080/v1/service

# finally unistall the deployment
helm uninstall helm-release
3 - Helm Repo
helm repo list
helm repo add $name $uri
helm repo add jenkins https://charts.jenkins.io
helm repo update

