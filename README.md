This project uses Pinecone, Langchain, Flask, Langfuse, SQlite and OpenAI API. It takes data from the user in PDF format and enables the user to talk with an AI within the PDF data's scope.
It has a chat history and multiple chat features.




# First Time Setup
 
#Create a .env file inside of langchain-project folder.
inside this file write:
SECRET_KEY=[Define a powerful key]

SQLALCHEMY_DATABASE_URI=sqlite:///sqlite.db

UPLOAD_URL=http://localhost:8050

OPENAI_API_KEY=[Your OpenAI API Key]

REDIS_URI=[Your Redis URI]

PINECONE_API_KEY=[Your Piecone API KEY]

PINECONE_ENV_NAME=[Your Pinecone Region Name]

PINECONE_INDEX_NAME=[index name]

LANGFUSE_PUBLIC_KEY=

LANGFUSE_SECRET_KEY=

PYTHONIOENCODEING=utf-8

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
