# Airflow Tutorial
A Git Repository to demonstrate a simple data validation job using Airflow. If you would like to replicate this environment on your own machine, you can follow the steps below. 

## 1. Install Docker
The first thing to do is to install docker (if already installed, you can move to step 2).
Go to https://www.docker.com/get-started/ and follow the instructions based on your OS.

## 2. Install Astro
Now, we will install Astro which is an environment manager for Airflow and Docker. It will make our life easier by setting up the environment and managing the connection between Docker and Airflow.
Go to below link and follow instructions based on your OS. Once installation is finished move to step 3. 
https://docs.astronomer.io/astro/cli/install-cli

## 3. Set up Astro
Move to your directory where you created your repo and at the root, in terminal, do in order:

```
mkdir airflow
```

```
cd airflow
```

Once you are inside the airflow directory execute the below command. It will initialize your Astro environment:
```
astro dev init
```

You should now see new files and folders added to the airflow directory. Please note that by default astro will add the airflow folder to the .gitignore file.

## 4. Create the Airflow DAG
In your aiflow directory, go to the 'dags' folder and save here the 'data_validation_dag.py' file available at: https://github.com/julienguyet/airflow-tutorial/blob/main/airflow/dags/data_validation_dag.py

## 5. Execute the DAG
In your terminal, at the level of the airlfow folder, run the below:

```
astro dev start
```

This will start Airflow and a new tab will open in your browser. Connect by using the default credentials (admin / admin). 
You should see the dag in the list on the first page. Click on the left button to activate it and voilà! You now have a dag running every one minute to check the quality of your data!
