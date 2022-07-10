# airflow-demo

[Running Airflow locally.](https://airflow.apache.org/docs/apache-airflow/stable/start/local.html)

## Install

Install from requirements:

```sh
pip install -r requirements.txt
```

## Setup

Initialize the database, make a user, and start all components:

```sh
airflow standalone
```

## Run

Run an all-in-one copy of Airflow:

```sh
airflow standalone
```

Or run Airflow scheduler and webserver:

```sh
airflow scheduler & airflow webserver
```

Kill Airflow processes that are running in the background:

```sh
kill -9 $(ps aux | grep airflow | grep -v "grep" | awk -F ' ' '{print $2}')
```

## Login

Login credentials:

| username | password |
| --- | --- |
| admin | `cat ~/airflow/standalone_admin_password.txt` |
