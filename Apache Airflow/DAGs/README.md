# My First DAG
This repository contains a simple DAG (Directed Acyclic Graph) using Airflow to extract, transform, and load data.

## Prerequisites
Before running this DAG, you need to make sure that you have Airflow installed and configured properly. Also, you need to have access to the /etc/passwd file on the system where Airflow is installed.

## DAG Details
This DAG has two tasks, which are defined below:

### Extract Task
This task extracts data from the /etc/passwd file, selects the first, third, and sixth columns using the cut command, and saves the extracted data to a file named extracted-data.txt in the directory /home/project/airflow/dags/.

### Transform and Load Task
This task transforms the data extracted by the previous task by replacing the colons with commas using the tr command and saves the transformed data to a file named transformed-data.csv in the same directory.

## DAG Configuration
This DAG has the following configurations:

**owner**: Ramesh Tony
**start_date**: The DAG will start running immediately after it is created.
**email**: ['ramesht@somemail.com']
**email_on_failure**: False
**email_on_retry**: False
**retries**: 1
**retry_delay**: 5 minutes
**schedule_interval**: 1 day

## Usage
To use this DAG, you need to copy the code and paste it into a new Python file in your Airflow DAGs directory. Make sure to update the **owner** and **email** fields to match your own information.

After that, you can run the DAG using the Airflow web interface or the Airflow CLI. Once the DAG is running, you can monitor its progress in the Airflow UI or in the logs.
