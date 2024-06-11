# NLP as a Webservice
 A langchain project with OpenAI API that takes data from the user in pdf format and enables the user to chat with an AI within the scopes of the data.


# First Time Setup

## Using Pipenv 

# Install dependencies
pipenv install

# Create a virtual environment
pipenv shell

# Initialize the database
flask --app app.web init-db

# Install dependencies
pip install -r requirements.txt

# Initialize the database
flask --app app.web init-db

# Running the app

Three separate processes need to be running for the app to work: the server and the worker.

If you stop any of these processes, you must start them back up!

Commands to start each are listed below. If you need to stop them, select the terminal window the process is running in and press Control-C

### To run the Python server

Open a new terminal window and create a new virtual environment:

pipenv shell

Then:

inv dev


### To run the worker

Open a new terminal window and create a new virtual environment:

pipenv shell


Then:

inv devworker


### To reset the database

Open a new terminal window and create a new virtual environment:

pipenv shell


Then:

flask --app app.web init-db
