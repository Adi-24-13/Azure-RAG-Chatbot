# Azure RAG Chatbot

An AI-powered chatbot built using **Retrieval-Augmented Generation (RAG)** that enables users to interact with custom data through natural language queries. This project combines **vector search** with **Azure OpenAI models** to deliver accurate, context-aware responses.

## Features

•  Chat with your own data
•  Semantic search using vector embeddings
•  Context-aware responses powered by LLMs
•  Document ingestion and processing pipeline
•  Fast retrieval using ChromaDB
•  Integrated with Azure OpenAI

## Architecture

The project follows a standard **RAG pipeline**:

1. **Data Ingestion**
   • Load documents
   • Split into chunks
   • Generate embeddings
2. **Vector Database**
   • Store embeddings in ChromaDB
3. **Query Processing**
   • Convert user query into embedding
4. **Retrieval**
   • Perform similarity search
   • Fetch relevant documents
5. **Generation**
   • Pass retrieved context + query to LLM
   • Generate final response

##  Tech Stack

• **Language:** Python
• **Libraries:** LangChain, ChromaDB
• **AI Models:** Azure OpenAI (GPT)
• **Cloud:** Microsoft Azure


## Project Structure

```
Azure-RAG-Chatbot/
│── app.py                # Main chatbot application  
│── ingest.py             # Document ingestion pipeline    
│── data/                 # Input documents  
│── chroma_db/            # Vector database storage  
```

## Installation

### Clone the repository

### Create virtual environment

python -m venv venv
venv\Scripts\activate   # Windows

### Install dependencies

• langchain
• langchain-openai
• langchain-chroma
• langchain-community
• langchain-text-splitters
• chromadb
• pypdf
• python-dotenv
• tiktoken

## Environment Variables

Create a `.env` file and add:

```
AZURE_OPENAI_API_KEY=your_api_key
AZURE_OPENAI_ENDPOINT=your_endpoint
AZURE_OPENAI_API_VERSION=2024-02-15-preview
AZURE_OPENAI_CHAT_DEPLOYMENT=your_chat_deployment
AZURE_OPENAI_EMBEDDING_DEPLOYMENT=your_embedding_deployment
```

## Usage

### Step 1: Ingest Data

ingest_data.py

### Step 2: Run Chatbot

Azure_RAG_Project.py


## Example Use Cases

•  Enterprise knowledge assistant
•  Document-based Q&A system
•  Customer support chatbot
•  Internal data search tool


## Key Learnings

• Built an end-to-end **RAG pipeline**
• Worked with **vector databases & embeddings**
• Integrated **Azure OpenAI with custom data**
• Improved LLM reliability by reducing hallucinations


## Author

**Aditya Sharma**
🔗 GitHub: https://github.com/Adi-24-13

