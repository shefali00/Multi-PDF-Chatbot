# Multi-PDF Chatbot Using FAISS and LangChain

This repository contains a Multi-PDF Chatbot application that enables intelligent and context-aware querying of multiple PDF documents. The system leverages Google Gemini Pro, LangChain, and FAISS for efficient vector embeddings, similarity search, and conversational AI capabilities.

---

## Features

- **PDF Parsing**: Extracts text content from multiple PDF files.
- **Contextual Querying**: Generates context-aware responses using LangChain and Google Gemini Pro.
- **Efficient Search**: Utilizes FAISS for fast similarity searches and document indexing.
- **Interactive Interface**: Built using Streamlit for an intuitive user experience.

---

## Prerequisites

Ensure you have the following installed:
- Python 3.8+
- pip (Python package installer)
- Google API Key with access to Google Gemini Pro

---

## Setup and Usage

Follow these steps to set up and run the project:

1. Clone the repository and navigate to the project directory:
    ```bash
    git clone https://github.com/shefali00/Multi-PDF-Chatbot.git
    cd Multi-PDF-Chatbot
    ```

2. Create and activate a virtual environment:
    ```bash
    python -m venv venv
    ```
    - **Windows**:  
      ```bash
      venv\Scripts\activate
      ```
    - **macOS/Linux**:  
      ```bash
      source venv/bin/activate
      ```

3. Install the required dependencies:
    ```bash
    pip install -r requirements.txt
    ```

4. Configure your environment variables:
    - Create a `.env` file in the project root and add your Google API Key:
      ```env
      GOOGLE_API_KEY=your_google_api_key
      ```

5. Run the application:
    ```bash
    streamlit run app.py
    ```

6. Use the application:
    - Upload one or more PDF files via the sidebar.
    - Click "Submit & Process" to process the PDFs.
    - Ask your question in the text box to receive context-aware responses.

---

## How It Works

1. **PDF Parsing**: Reads and extracts text from uploaded PDFs using `PyPDF2`.
2. **Text Chunking**: Splits large PDF content into manageable chunks using `RecursiveCharacterTextSplitter`.
3. **Vector Embeddings**: Generates embeddings using Google Gemini Pro's `GoogleGenerativeAIEmbeddings`.
4. **Document Indexing and Search**: Uses FAISS to store and perform similarity searches on document embeddings.
5. **Conversational Chain**: Processes user queries with a LangChain QA chain and generates context-aware responses.

