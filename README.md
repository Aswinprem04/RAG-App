# RAG-based Chatbot Application

## Introduction
------------
The RAG-based Chatbot Application is a Python application that allows you to chat with multiple PDF documents. You can ask questions about the PDFs using natural language, and the application will provide relevant responses based on the content of the documents. This app utilizes a language model to generate accurate answers to your queries. Please note that the app will only respond to questions related to the loaded PDFs.

![RAG-based Chatbot Application](/image/image.png)

## How It Works
------------

1. PDF Loading: The app reads multiple PDF documents and extracts their text content.

2. Text Chunking: The extracted text is divided into smaller chunks that can be processed effectively.

3. Language Model: The application utilizes a language model to generate vector representations (embeddings) of the text chunks.

4. Similarity Matching: When you ask a question, the app compares it with the text chunks and identifies the most semantically similar ones.

5. Response Generation: The selected chunks are passed to the language model, which generates a response based on the relevant content of the PDFs.

## Dependencies and Installation
----------------------------
To install the Chatbot Application, please follow these steps:

1. Clone the repository to your local machine.

2. Install the required dependencies by running the following command:
   ```
   pip install -r requirements.txt
   ```

3. Obtain an API key from Groq and add it to the `.env` file in the project directory.
```commandline
GROQ_API_KEY=your_secrit_api_key
```

4. Download & install [Ollama](https://ollama.com/download) to your local machine.

## Usage
-----
To use the Chatbot Application, follow these steps:

1. Ensure that you have installed the required dependencies and added the GROQ API key to the `.env` file.

2. Run the command to initialize the embedding (only once).
   ```
   ollama pull nomic-embed-text
   ```

3. Run the `app.py` file using the Streamlit CLI. Execute the following command:
   ```
   streamlit run app.py
   ```

4. The application will launch in your default web browser, displaying the user interface.

5. Load multiple PDF documents into the app by following the provided instructions.

6. Ask questions in natural language about the loaded PDFs using the chat interface.
