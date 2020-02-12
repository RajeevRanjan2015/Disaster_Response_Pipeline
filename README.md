# Disaster Response Pipeline Project

<a id='overview'></a>

## 1. Project Overview

In this project, I'll apply data engineering to analyze disaster data from "Figure Eight" to build a model for classifies disaster messages.

_data_ directory contains a data set which are real messages that were sent during disaster. The task is to create a machine learning pipeline to categorize these events so that appropriate disaster relief agency can be reached out for help.

This project will include a web app where an emergency worker can input a new message and get classification results in several categories. Also, it has visualization related with.

<a id='components'></a>

## 2. Project Components

There are three components of this project:

1. ETL Pipeline

    File _data/process_data.py_ contains data cleaning pipeline that has below functionalities:
    Loads the messages and categories datasets
    Merges the two datasets
    Cleans the data
    Stores it in a SQLite database
    
2. ML Pipeline

    File _models/train_classifier.py_ contains machine learning pipeline
    
    
3. Flask Web App


## 3. Instructions to run:

1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl models/vocabulary_stats.pkl models/category_stats.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/


## 4. Files in the Repo:

<pre>
.
├── app
│   ├── run.py------------------------# FLASK FILE THAT RUNS APP
│   |
│   │   
│   └── templates
│       ├── go.html-------------------# CLASSIFICATION RESULT PAGE OF WEB APP
│       └── master.html---------------# MAIN PAGE OF WEB APP
├── data
│   ├── DisasterResponse.db-----------# DATABASE TO SAVE CLEANED DATA TO
│   ├── disaster_categories.csv-------# DATA TO PROCESS
│   ├── disaster_messages.csv---------# DATA TO PROCESS
│   └── process_data.py---------------# PERFORMS ETL PROCESS
|
├── models
│   └── train_classifier.py-----------# PERFORMS CLASSIFICATION TASK
|
|-- README.md : You can say document about the project

</pre>


