# gcp-iam-collector
Python scripts for collecting and visualising [Google Cloud Platform](https://cloud.google.com/) IAM permissions

## Features

GCP IAM collector iterates over projects using [Google Cloud Resource Manager API](https://cloud.google.com/resource-manager/reference/rest/v1/projects/list) and dumps to CSV files:
* all available GCP projects,
* projects IAM permissions,
* projects service account and their keys,
* BigQuery dataset ACLs,
* Cloud Storage bucket ACLs

IAM graph currently supports:
* GCP projects and their permissions,
* Service accounts and their permissions

# Setup

1. Install dependencies:
```
pip install -r requirements.txt
```
2. Install [gcloud](https://cloud.google.com/sdk/gcloud/) CLI tool.
3. Setup [Google Application Default Credentials](https://developers.google.com/identity/protocols/application-default-credentials):
```
gcloud auth application-default login
```

# Run Instructions

Command below dumps all IAM to csv files
```
python collector.py
```

Creating interactive graph:
```
python create_iam_graph.py
```