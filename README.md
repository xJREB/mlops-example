# MLOps Example

Necessary steps to solve the example:
```bash
# install the Python dependencies
pip install -r requirements.txt

# initialize DVC in the git repo
dvc init

# list all DVC artifacts for the repo
dvc list ...
# import the data sets from the repo
dvc import ...

# run the training script
python ./src/train.py

# open the MLflow web interface
mlflow ui

```