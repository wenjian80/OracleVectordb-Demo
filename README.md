# Oracle 23ai VectorDB Demo


This is a Python application that allows you to load a PDF and ask questions about it using natural language. The application uses a LLM to generate a response about your PDF. The LLM will not answer questions unrelated to the document.

## How it works

The application reads the PDF and splits the text into smaller chunks that can be then fed into a LLM. It uses OpenAI embeddings/Oracle GenAI  to create vector representations of the chunks and stored in Oracle23ai  Vector DB. The application then finds the chunks that are semantically similar to the question that the user asked and feeds those chunks to the LLM to generate a response.

The application uses Streamlit to create the GUI and Langchain to deal with the LLM.

## Installation



To install the repository, please clone this repository and install the requirements:

Install python   3.11 or higher. upgrade pip3 and use 

```
conda create -n aidemo python=3.12
conda activate aidemo
```

```
pip3 install -r requirements.txt
```

Add Hidden info

You will also need to add your OpenAI API key  Database username, password and connect string to the `.env` 

## Usage

To use the application, run the `app.py` file with the streamlit CLI (after having installed streamlit):

```
streamlit run app.py
```



