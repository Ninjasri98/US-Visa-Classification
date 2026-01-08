# US Visa Approval Prediction

![Build Status](https://img.shields.io/badge/build-passing-brightgreen)
![Python Version](https://img.shields.io/badge/python-3.12-blue)
![License](https://img.shields.io/badge/license-MIT-green)

## What the Project Does

This project provides a production-ready machine learning pipeline for US Visa approval prediction. It includes data ingestion, EDA, feature engineering, transformation, validation, hyperparameter tuning, model training,  evaluation, and deployment. The project is designed to be modular, scalable, and easy to integrate into real-world applications.

## Why the Project is Useful

- **End-to-End Workflow**: Covers all stages of the machine learning lifecycle.
- **Cloud Integration**: Supports AWS for storage and deployment.
- **Data Drift Detection**: Uses EvidentlyAI for monitoring data drift(MLOPs).
- **FastAPI Integration**: Provides a REST API for predictions.
- **CICD Pipeline**: Automates deployment using GitHub Actions and AWS.

## How Users Can Get Started

### Prerequisites

- Python 3.12
- Anaconda
- Docker
- AWS Account
- MongoDB Atlas Account

### Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/Ninjasri98/US-Visa-Classification.git
   cd US-Visa-Classification
   ```

2. Create and activate a virtual environment:

   ```bash
   conda create -n visa python=3.12 -y
   conda activate visa
   ```

3. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

4. Set up environment variables:

   ```bash
   export MONGODB_URL="mongodb+srv://<username>:<password>@cluster.mongodb.net"
   export AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>
   export AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>
   ```

### Running the Application

1. Start the FastAPI server:

   ```bash
   python app.py
   ```

2. Access the API at `http://localhost:8000`.

### Training the Model

Run the training pipeline:

```bash
python demo.py
```

## Key Features

- **Data Ingestion**: Automated data collection and preprocessing.
- **Model Training**: Supports multiple algorithms like XGBoost, CatBoost, and Scikit-learn.
- **Model Deployment**: Dockerized application with AWS EC2 and ECR integration.
- **Monitoring**: Data drift detection using EvidentlyAI.
- **API Integration**: REST API for real-time predictions.


## How to run?

```bash
conda create -n visa python=3.8 -y
```

```bash
conda activate visa
```

```bash
pip install -r requirements.txt
```

## Workflow:

1. constants
2. entity
3. components
4. pipeline
5. Main file

### Export the  environment variable

```bash
export MONGODB_URL="mongodb+srv://<username>:<password>...."

export AWS_ACCESS_KEY_ID=<AWS_ACCESS_KEY_ID>

export AWS_SECRET_ACCESS_KEY=<AWS_SECRET_ACCESS_KEY>
```

# AWS-CICD-Deployment-with-Github-Actions

## 1. Login to AWS console.

## 2. Create IAM user for deployment

	#with specific access

	1. EC2 access : It is virtual machine

	2. ECR: Elastic Container registry to save your docker image in aws


	#Description: About the deployment

	1. Build docker image of the source code

	2. Push your docker image to ECR

	3. Launch Your EC2 

	4. Pull Your image from ECR in EC2

	5. Lauch your docker image in EC2

	#Policy:

	1. AmazonEC2ContainerRegistryFullAccess

	2. AmazonEC2FullAccess

	
## 3. Create ECR repo to store/save docker image
    - Save the URI: 315865595366.dkr.ecr.us-east-1.amazonaws.com/visarepo

	
## 4. Create EC2 machine (Ubuntu) 

## 5. Open EC2 and Install docker in EC2 Machine:
	
	
	#optinal

	sudo apt-get update -y

	sudo apt-get upgrade
	
	#required

	curl -fsSL https://get.docker.com -o get-docker.sh

	sudo sh get-docker.sh

	sudo usermod -aG docker ubuntu

	newgrp docker
	
# 6. Configure EC2 as self-hosted runner:
    setting>actions>runner>new self hosted runner> choose os> then run command one by one


# 7. Setup github secrets:

   - AWS_ACCESS_KEY_ID
   - AWS_SECRET_ACCESS_KEY
   - AWS_DEFAULT_REGION
   - ECR_REPO




