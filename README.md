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

The `backend` folder contains the configuration for the S3 bucket and DynamoDB which will be used as backend and lock for storing the state of the terraform deployment.

The `infrastructure` folder contains the terraform files for deploying the required infrastructure to AWS. It includes the network components like VPC, IGW, NAT-GW, Elastic IPs, Route tables and routes, subnets and security group. It also includes configurations for IAM roles, CloudWatch Log group, EKS node group and EKS cluster.

The `deployment` folder contains the scripts used for deploying the two applications to the AWS infrastructure. Terraform Kubernetes manifest, deployment and service resources were used to deploy the `portfolio` and `socks shop` apps. It also contains configuration for the subdomains, `portfolio.abdulbarri.online` and `socks.abdulbarri.online`.

The `monitoring` folder contains the scripts used to deploy prometheus and grafana to the cluster. This will be used for monnitoring and observing the performance and uptime of the applications.

## CI/CD Pipeline

CI/CD was implemented for this project using Git Actions.  

