# ML-Flow-Basic-Operation



...
## For Dagshub:

ML FLOW_TRACKING_URI=https://dagshub.com/shabbu8111999/ML-Flow-Basic-Operation.mlflow \

ML FLOW_TRACKING_USERNAME=shabbu8111999 \

ML FLOW_TRACKING_TOKENS=929d2e7e19d6a84f2682135c783b813c29e24089 \


#                                OR                          #

### Use this Code
import dagshub
dagshub.init(repo_owner='shabbu8111999', repo_name='ML-Flow-Basic-Operation', mlflow=True)

import mlflow
with mlflow.start_run():
  mlflow.log_param('parameter name', 'value')
  mlflow.log_metric('metric name', 1)


## NOTE:
1. In Command Prompt Terminal(cmd) use : set 
2. In Linux/Mac Command use : export
3. In Powershell Terminal use : $env:


```bash

set MLFLOW_TRACKING_URI="https://dagshub.com/shabbu8111999/ML-Flow-Basic-Operation.mlflow"

set ML FLOW_TRACKING_USERNAME=shabbu8111999

set ML FLOW_TRACKING_TOKENS=929d2e7e19d6a84f2682135c783b813c29e24089

```


# ML Flow on AWS

## Ml Flow on AWS Setup

1. Login in to AWS Console.
2. Create IAM User with AdministratorAccess
3. Export the credentials in your AWS CLI by running "aws configure"
4. create a s3 bucket
5. Create EC2 Machine (Ubuntu) & add Security groups 5000 port


## Run the following command on EC2 Machine AWS (Ubuntu)

```bash

sudo apt update

sudo apt install python3.12-venv -y

python3 -m venv mlflow

source mlflow/bin/activate

pip install pipenv

mkdir mlflow

cd mlflow

pipenv install mlflow

pipenv install awscli

pipenv install boto3

pipenv shell


# Set your AWS Credentials
aws configure


# Finally
mlflow server -h 0.0.0.0 --default-artifact-root s3://mlflow-buk-0001


# open public IPv4 DNS to the port 5000


# set uri in your local terminal and your code
set MLFLOW_TRACKING_URI=http://ec2-13-203-66-132.ap-south-1.compute.amazonaws.com:5000/

```