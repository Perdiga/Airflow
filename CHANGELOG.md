# Changelog

## 1.0.0 

[Full Changelog](https://github.com/Perdiga/Airflow/commits/1.0.0)

**Fixed bugs:**

- Fixed DAG folder mapping on `compose.yaml` file
- Fixed postgres user on `compose.yaml` file
- Fixed airflow webserver health check url on `compose.yaml` file
- Fixed function definition on `smooth.py` dag file

**Implemented enhancements:**

- Upgrade all images from `compose.yaml` file to the latest version. `:latest` was not used since it can create unpredictable behavior
- Changed the `_AIRFLOW_DB_UPGRADE` variable to `_AIRFLOW_DB_MIGRATE` due deprecation warning 
- Add `.gitignore` file to the project to avoid pushing unnecessary files to server
- Add `AIRFLOW__SCHEDULER__ENABLE_HEALTH_CHECK` to start a small web server for a scheduler health check
- Changed the `scheduler` service to use the heath web server instead of the `airflow jobs check` command
- Add vscode debug profile to facilitate debugging  the dags
- Add readme.md with project information 
