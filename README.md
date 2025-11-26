#ABOUT
#A RAG pipleine integrated with MCP server to help high school students in science. More subjects can be added into the pipeline easily into the data folder inside the server folder for expansion of the application usage.
#This model uses LLMs from Grok and is accesed via Grok API. The programming language used is PYTHON (version 3.10.8).

#SETUP USING DOCKER:
#Create a .env file and add a variable "GROQ_API_KEY" with the API key from Grok as its value and save it in the root folder. Now launch Docker desktop, open terminal from the root folder and execute the following command:
docker compose up --build

#SETUP WITHOUT DOCKER:
#Create a .env file and add a variable "GROQ_API_KEY" with the API key from Grok as its value and save it in the root folder. Now open terminal from the root folder and execute the following command:
pip install requirements.txt
uvicorn server.main:app --reload
python -m streamlit run streamlit_app/app.py
