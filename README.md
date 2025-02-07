# RAG with LangChain

## Overview

This project implements a **Retrieval-Augmented Generation (RAG)** system using **LangChain**, leveraging vector databases to improve the accuracy and contextual relevance of AI-generated responses. The system combines document chunking, embedding generation, metadata management, and retrieval strategies to enhance large language model (LLM) capabilities with external knowledge sources.

## Key Concepts

### 1. **Chunking**

- Breaks large text documents into smaller, meaningful segments.
- Ensures context retention while optimizing retrieval efficiency.
- Supports multiple chunking strategies (e.g., paragraph-based, sentence-based, or special-character-defined splitting).

### 2. **Embeddings & Vector Databases**

- Converts text into dense vector representations.
- Uses **FAISS** for efficient similarity-based retrieval.
- Metadata (e.g., document titles, chunk numbers) enhances search precision.

### 3. **Retrieval Mechanism**

- Stores pre-processed text embeddings in a **vector database**.
- Uses similarity search to fetch the most relevant information based on user queries.
- Employs LangChain’s `as_retriever()` function to integrate search results into response generation.

### 4. **LLM Integration**

- Utilizes **OpenAI GPT models** to generate responses based on retrieved documents.
- Incorporates prompt engineering techniques for structured and contextual output.

## Functionality

- **Pre-process documents**: Chunking, embedding, and metadata storage.
- **Store embeddings** in a vector database (**FAISS**).
- **Retrieve relevant chunks** using similarity search.
- **Generate answers** based on retrieved knowledge via an LLM.
- **Cite sources** by including metadata in responses.

## Setup Instructions

### Prerequisites

Ensure you have the following installed:

- **Python 3.11+**
- **Virtual environment (venv)**

### 1. Clone the Repository

```sh
git clone https://github.com/AntQua/rag-langchain.git
cd rag-langchain
```

### 2. Create & Activate Virtual Environment

```sh
python -m venv venv
source venv/bin/activate  # For macOS/Linux
venv\Scripts\activate    # For Windows
```

### 3. Install Dependencies

```sh
pip install -r requirements.txt
```

### 4. Set Up Environment Variables

Create a `.env` file in the project root and add:

```
OPENAI_API_KEY=your_openai_api_key
```

### 5. Link IPython Kernel to Virtual Environment

If you're running this project in **Jupyter Notebook**, execute the following commands to link the IPython kernel to your virtual environment:

```sh
pip install ipykernel
python -m ipykernel install --user --name=venv --display-name "Python (venv)"
```

Then, restart Jupyter Notebook and select **Python (venv)** as the kernel.





