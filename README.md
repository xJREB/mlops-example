# MLOps Example

Necessary steps to arrive at this example:
```bash
# copy requirements.txt and install the Python dependencies
pip install -r requirements.txt

# initialize DVC in the git repo
dvc init

# list all DVC artifacts in the data folder of the named repo (3 in total)
dvc list https://github.com/xJREB/se4ai-lecture-dvc-artifacts data

# import the correct data set from the repo
dvc import https://github.com/xJREB/se4ai-lecture-dvc-artifacts data/winequality-red.csv

# copy and run the training script
python src/train.py

# open the MLflow web interface --> sort the experiment table by r2 score and look which alpha and l1_ratio the highest value has (r2 of 0.358 for alpha=0.01 and l1_ratio=0.01)
mlflow ui

# lastly, build a CI pipeline with GitHub actions (see `.github/workflows/ml-pipeline.yml`)
```