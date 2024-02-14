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





pip install "apache-airflow[celery]==2.2.5" --constraint "https://raw.githubusercontent.com/apache/airflow/constraints-2.2.5/constraints-3.9.txt"

## Requirements

Setting up the proper python environment.

1. Install [python3.9](https://askubuntu.com/questions/1318846/how-do-i-install-python-3-9)

2. Install venv

    ```
    sudo apt-get install python3.9-dev python3.9-venv
    ```

# Setup a virtual environment with a specific version of python

