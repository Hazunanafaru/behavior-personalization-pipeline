# Behavior Personalization Pipeline with AWS

## Description

Build batch processing pipelines to do behavior analytics with AWS.

## Technology

[Apache Airflow](https://airflow.apache.org/), [AWS](https://aws.amazon.com/) (S3, EMR, IAM, Redsfhit), [Docker](https://www.docker.com/), and [PySpark](https://spark.apache.org/docs/latest/api/python/index.html)

## Prerequisets

1. Docker
2. PostgreSQL
3. AWS Account
4. AWS CLI Configured

## Usage

This code run in Windows 10 (Powershell 5.1) while the reference [[1]](https://www.startdataengineering.com/post/data-engineering-project-for-beginners-batch-edition/) run in linux/macOS (bash shell).

To setup the infrastructure needed, run infra_setup.ps1 with `bucket_name` as an argument.

Example : `infra_setup.ps1 name-of-bucket`

Make python environment using venv and install requirement packages

```
    # Make
    python -m venv bp-env
    
    # Activate
    .\bp-env\Scripts\Activate.ps1
    
    # Install
    pip install -r requirements.txt
```

To destroy infrastructure, run infra_teardown.ps1 with `bucket_name` as an argument.

Example : `infra_teardown.ps1 name-of-bucket`

## References

[1] [Data Engineering Project for Beginners - Batch edition](https://www.startdataengineering.com/post/data-engineering-project-for-beginners-batch-edition/)

[2] [Getting started with Amazon Redshift Spectrum ](https://docs.aws.amazon.com/redshift/latest/dg/c-getting-started-using-spectrum.html)

[3] [Changing PowerShell's default output encoding to UTF-8](https://stackoverflow.com/questions/40098771/changing-powershells-default-output-encoding-to-utf-8)

[4] [authorize-security-group-ingress](https://docs.aws.amazon.com/cli/latest/reference/ec2/authorize-security-group-ingress.html)

[5] [S3DistCp (s3-dist-cp)](https://docs.aws.amazon.com/emr/latest/ReleaseGuide/UsingEMR_s3distcp.html)

[6] [StepConfig](https://docs.aws.amazon.com/emr/latest/APIReference/API_StepConfig.html)