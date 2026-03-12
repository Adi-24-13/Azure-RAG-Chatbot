--> Azure OpenAI RAG Chatbot

It is an enterprise style Retrieval-Augmented Generation (RAG) system built using Azure OpenAI, Langchain and Chroma Vector Database to
answer questions from PDF documents.
This project demonstrates how to build a document question-answering system using modern LLM architecture used in real-world AI applications.

--> Project Overview

The system allows users to:
• Convert the document into embeddings using Azure OpenAI
• Store embeddings in a Chroma vector database
• Retrieve relevant document chunks
• Generate accurate answers using Azure GPT models

The chatbot answers questions only using the information present in the document, reducing hallucinations.

--> Architecture

PDF → Text Chunking → Azure Embeddings → Vector Database (Chroma) → Retriever → Azure GPT → Answer

--> Tech Stack

• Python
• Azure OpenAI
• LangChain (LCEL pipeline)
• Chroma Vector Database
• PyPDF Loader
• Dotenv for environment variables

--> Project Structure
azure-openai-rag-chatbot
│
├── ingest.py        # Loads PDF, splits text, creates embeddings
├── chat.py          # Runs the RAG chatbot
├── data/            # Place PDFs here
└── db/              # Vector database created after ingestion

--> Setup Instructions

1. Install Dependencies

   - langchain
   - langchain-openai
   - langchain-chroma
   - langchain-community
   - langchain-text-splitters
   - chromadb
   - pypdf
   - python-dotenv
   - tiktoken

2. Configure Environment Variable

Create a .env file in the root directory.

AZURE_OPENAI_API_KEY=your_api_key
AZURE_OPENAI_ENDPOINT=https://your-resource.openai.azure.com/
AZURE_OPENAI_API_VERSION=2024-02-15-preview
AZURE_OPENAI_CHAT_DEPLOYMENT=your_chat_deployment
AZURE_OPENAI_EMBEDDING_DEPLOYMENT=your_embedding_deployment

3. Add PDF Documents

   Place your document inside the data folder.
   Example:
           data/
               document.pdf

4. Create the Vector Database

Run the ingestion script:
  ingest_data.py

This will:
• Load the document
• Split text into chunks
• Create embeddings
• Store vectors in Chroma

5. Start the Chatbot
    Azure_RAG_Project.py

--> Example Use Case
This system can be used for:

• Company knowledge assistants
• Research document Q&A
• Legal document analysis
• Internal documentation chatbots
