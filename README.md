# Orchestration-Scaling
# AWS CLI and Boto3 Setup Guide

This guide provides step-by-step instructions on how to set up AWS Command Line Interface (CLI) and Boto3, a Python SDK for AWS. This setup will enable you to interact with AWS services directly from your command line and Python scripts.

## Prerequisites

Before you begin, ensure you have:
- An AWS account.
- Python installed on your system.

## 1. Setting Up AWS CLI

### Installation

1. **Download AWS CLI**: Visit the [AWS CLI installation page](https://aws.amazon.com/cli/) and download the appropriate version for your operating system.

2. **Install AWS CLI**: Follow the installation instructions provided on the download page for your OS.

### Configuration

1. **AWS Credentials**: You'll need your AWS Access Key ID and Secret Access Key. You can find these in your AWS Management Console under IAM.

2. **Configure AWS CLI**:
   - Open your terminal or command prompt.
   - Run the command `aws configure`.
   - Enter your Access Key ID, Secret Access Key, default region name, and default output format when prompted.

## 2. Setting Up Boto3

### Installation

1. **Install Boto3**: Run the command `pip install boto3` in your terminal or command prompt.

### Configuration

Boto3 uses the credentials stored by AWS CLI. If AWS CLI is configured, no additional steps are required for Boto3.

## 3. containerized using Docker
use
 ```bash
git clone  https://github.com/UnpredictablePrashant/SampleMERNwithMicroservices.git
```
### Front end
- Navigate to SampleMERNwithMicroservices/frontend.
- Use [Dockerfile](https://github.com/patilajayv/Orchestration-Scaling/blob/main/frontend/Dockerfile) create container
-Use commnad
 ```bash
Sudo docker build -t frontendimage . 
```
### Backend end
- Navigate to SampleMERNwithMicroservices/backend/helloService.
- Use [Dockerfile](https://github.com/patilajayv/Orchestration-Scaling/blob/main/backend/helloService/Dockerfile) create container
-Use commnad
 ```bash
Sudo docker build -t backendhelloimg .
```
- Navigate to SampleMERNwithMicroservices/backend/profile.
- Use [Dockerfile](https://github.com/patilajayv/Orchestration-Scaling/blob/main/backend/profile/Dockerfile) create container
-Use commnad
 ```bash
Sudo docker build -t backendprofileimg .
```
Create an Amazon ECR repository for each image.

Push the Docker images to their respective ECR repositories.

Hello Microservice: https://gallery.ecr.aws/c3w1m1q2/ajaybe11

Profile Microservice: https://gallery.ecr.aws/c3w1m1q2/ajaybe12

Frontend Microservice: https://gallery.ecr.aws/c3w1m1q2/fe1

