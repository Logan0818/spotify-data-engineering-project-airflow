# Spotify Data Engineering Project (Airflow)
In this project, we will modify the previous [spotify project using python](https://github.com/Logan0818/spotify-end-to-end-data-engineering-project) we built and use Apache Airflow to build the pipeline.

## Architecture Diagram:
![Architecture Diagram](https://github.com/Logan0818/spotify-data-engineering-project-airflow/blob/main/spotify_project_airflow_architecture_diagram_v1.png)

## Airflow Graph
![Airflow Graph](https://github.com/Logan0818/spotify-data-engineering-project-airflow/blob/main/airflow%20Graph.png)

## Tech Stacks:
- Docker
- Apache Airflow

## High Level Steps and Notes
1. Update docker compose file to include (1) spotipy (2) apache-airflow-providers-amazon packages
2. Configure your spotify client id and secret in Airflow UI (under Variables)
3. write a dag to extract data from Spotify API
4. In order to save file in S3, you need to make connection to S3. Setup IAM to get S3 secret
5. Use S3CreateObjectOperator
6. Use XCom to pass data between tasks
7. Remember to remove the trigger in lambda function that we built in last project
