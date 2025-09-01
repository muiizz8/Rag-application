# 🤖 RAG Application with LangChain and IBM Watsonx

This repository contains a Jupyter Notebook that demonstrates how to build a Retrieval-Augmented Generation (RAG) application using LangChain and IBM's Watsonx AI. The application allows you to ask questions about a company policy document and get answers from a powerful Large Language Model.

## 📝 Description

The core of this project is the `Rag.ipynb` notebook, which walks you through the process of:
1.  Loading a text document (a sample company policy).
2.  Splitting the document into manageable chunks.
3.  Generating vector embeddings for the text chunks using Hugging Face models.
4.  Storing the embeddings in a Chroma vector store.
5.  Setting up a connection to IBM Watsonx AI to use powerful LLMs like Google's Flan-T5 or Meta's Llama.
6.  Building a Question-Answering (QA) chain to query the document.
7.  Creating a conversational agent that can remember the chat history.

## ✨ Features

*   **Document Loading:** Loads text files for processing.
*   **Text Splitting:** Splits documents into smaller chunks for efficient processing.
*   **Vector Embeddings:** Uses Hugging Face's sentence transformers to generate embeddings.
*   **Vector Store:** Utilizes ChromaDB for storing and retrieving vector embeddings.
*   **LLM Integration:** Integrates with IBM Watsonx AI to leverage state-of-the-art LLMs.
*   **Question Answering:** Implements a `RetrievalQA` chain for answering questions based on the document.
*   **Conversational AI:** Creates a `ConversationalRetrievalChain` to maintain conversation history.

## 🛠️ Technologies Used

*   **Python 3**
*   **Jupyter Notebook**
*   **LangChain:** A framework for developing applications powered by language models.
*   **IBM Watsonx AI:** A platform for building and deploying AI models.
*   **Hugging Face Transformers:** For accessing pre-trained models and embeddings.
*   **ChromaDB:** An open-source embedding database.
*   **wget:** For downloading files.

## 🚀 How to Use

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/jules-dot-ai/rag-app-example.git
    cd rag-app-example
    ```

2.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

3.  **Set up IBM Watsonx credentials:**
    In the `Rag.ipynb` notebook, you need to provide your IBM Cloud API key and project ID in the following section:
    ```python
    credentials = {
        "url": "https://eu-de.ml.cloud.ibm.com",
        "api_key" : "your-ibm-cloud-api-key",
    }

    project_id = 'your project-id'
    ```

4.  **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook Rag.ipynb
    ```
    Execute the cells in the notebook to see the RAG application in action.

## 📄 License

This project is licensed under the [MIT License](LICENSE).
