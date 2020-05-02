# Disaster Response Pipeline Project
This project is to classify the messages that will popup on time of natural disaster. It will be useful for countries to tackle that disaster.

Here, this dataset is from FigureEight and I have done classification based on messages to classify category of message. Additionally, have made Web app using Flask to visualize data.

### Files:
app/templates/* -> Contains html css files
app/run.py -> contains code of flask to run on web browser

data/disaster_categories.csv & disaster_messages.csv -> dataset files
data/disaster_response.db -> SQLite DB that contains clean code
data/process_data.py -> code to clean data and save to DB

models/train_classifier.py -> loads data from DB, trains classifier and gives results
models/classifier.pkl -> saved model

disaster.png -> screenshot of web-app

### Instructions to run:
1. Run the following commands in the project's root directory to set up your database and model.

    - To run ETL pipeline that cleans data and stores in database
        `python data/process_data.py data/disaster_messages.csv data/disaster_categories.csv data/DisasterResponse.db`
    - To run ML pipeline that trains classifier and saves
        `python models/train_classifier.py data/DisasterResponse.db models/classifier.pkl`

2. Run the following command in the app's directory to run your web app.
    `python run.py`

3. Go to http://0.0.0.0:3001/ or you can change url in code.
