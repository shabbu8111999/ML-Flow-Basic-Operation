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


## NOTE: In Command Prompt use : set 
##       In Linux/Mac Command use : export
##       In Powershell Terminal use : $env:


```bash

set MLFLOW_TRACKING_URI="https://dagshub.com/shabbu8111999/ML-Flow-Basic-Operation.mlflow"

set ML FLOW_TRACKING_USERNAME=shabbu8111999

set ML FLOW_TRACKING_TOKENS=929d2e7e19d6a84f2682135c783b813c29e24089

```