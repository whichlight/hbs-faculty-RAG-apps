# HBS Faculty Directory RAG Apps

These are two prototypes to explore the [HBS Faculty Directory](https://www.hbs.edu/faculty/Pages/browse.aspx?faculty=Current) using retrieval augmented generation (RAG).

The backend under `app.py` is a llamaindex chat engine that queries a vector store in `chroma_db`

The main prototype is `user-query-form/` which uses a form input to build the RAG query, and then LLM-driven suggested questions for follow up responses.

`chat-app/` contains a chat app that takes the input and uses that for queries to the llamaindex chat engine, and directly displays the responses.

## Installation

Install git-lfs, which is used to store the vector DB. Then clone this repo.

Make a copy of `.env-example` to `.env` and add your OpenAI key.

Start a virtual environment with `venv` and install with pip `pip3 install -r requirements.txt`.

In each of the prototype directories `user-query-form` and `chat-app`, install the respective app with `npm install`.

## Running

Start the server with `python app.py` and navigate to `user-query-form` and start the client with `npm start`