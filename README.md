
# ML_flow_Basic_operation

## For Dagshub:

import dagshub
dagshub.init(repo_owner='chetankharkar21', repo_name='ML_flow_Basic_operation', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)

```bash 

$env:MLFLOW_TRACKING_URI = "https://dagshub.com/chetankharkar21/ML_flow_Basic_operation.mlflow"
$env:MLFLOW_TRACKING_USERNAME = "chetankharkar21"
$env:MLFLOW_TRACKING_PASSWORD = "4d6584b697c03a8d1f682a054efbee4a7264d047"

```

# MLFLOW on AWS 

## MLFLOW on AWS setup

1. login to AWS console 
2. create IAM users with Administration Access
3. explore the credentials with your AWS CLI by running 'AWS configure'
4. create a S3 bucket '
5. create EC2 machine and add security groups 5000 ports 

run the following command on EC2 machine 

bucket name : mlflow-buc2001 

* commands: 

sudo apt update
sudo apt install python3-pip 
sudo apt install pipenv
mkdir mlflow
cd mlflow
pipenv install mlflow
pipenv install awscli
pipenv install boto3
pipenv shell
aws configure

* optional:
"sudo apt install python3.12-venv
python3 -m venv mlflow_env (create)
source mlflow_env/bin/activate (activate)"

* finally(Public IPv4 DNS): 
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-buc2001

* seturi in local terminal for linux
export MLFLOW_TRACKING_URI=http://ec2-3-149-230-242.us-east-2.compute.amazonaws.com:5000/

* for windows powershell
$env:MLFLOW_TRACKING_URI = "http://ec2-3-149-230-242.us-east-2.compute.amazonaws.com:5000/"




