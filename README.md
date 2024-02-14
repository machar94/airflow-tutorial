# airflow-tutorial

*Note*: Exploring Airflow 2.2.5. The latest version of python that works with 2.2.5 is python3.9. See [Requirements](#requirements) to install the proper python version.

## Instructions

1. Create a virtual environment within the repository. The second arg creates the virtual environment in *project/.venv*.

    ```
    python3.9 -m venv .venv
    ```

2. Activate the virtual environment. To deactivate later, `deactivate`.

    ```
    source .venv/bin/activate
    ```

3. Upgrade `pip`. Note this refers to the `pip` in the virtual env.

    ```
    python3 -m pip install --upgrade pip
    python3 -m pip --version # Confirm location of pip in .venv
    ```

4. Install airflow (take a look at *requirements.txt*)

    ```
    pip install -r requirements.txt
    ```

5. Export AIRFLOW_HOME to the current directory.

    ```
    export AIRFLOW_HOME=$(pwd)/airflow
    ```

6. Initialize the database.

    ```
    airflow db init
    ```

7. Create a user.

    ```
    airflow users create \
        --username admin \
        --password admin \
        --firstname admin \
        --lastname admin \
        --role Admin \
        --email admin@gmail.com
    ```

## Running the Webserver and Scheduler

1. Open two new terminals. In each, activate the venv and export AIRFLOW_HOME. Start the scheduler and webserver.

    ```
    # Terminal 1
    source .venv/bin/activate
    export AIRFLOW_HOME=$(pwd)/airflow
    airflow scheduler

    # Terminal 2
    source .venv/bin/activate
    export AIRFLOW_HOME=$(pwd)/airflow
    airflow webserver
    ```

## Requirements

Setting up the proper python environment.

1. Install [python3.9](https://askubuntu.com/questions/1318846/how-do-i-install-python-3-9)

2. Install venv

    ```
    sudo apt-get install python3.9-dev python3.9-venv
    ```
