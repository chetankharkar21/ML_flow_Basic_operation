
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
