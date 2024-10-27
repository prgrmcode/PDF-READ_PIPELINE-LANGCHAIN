# LLM Pipeline for PDF Processing

This project demonstrates a pipeline for processing PDF documents using a Large Language Model (LLM) and various NLP tools. The pipeline includes steps for loading a model, loading and transforming documents, creating embeddings, storing embeddings in a vector store, retrieving relevant documents, managing memory, and deploying a conversational retrieval chain.

## Features

- Load and use a Large Language Model (LLM) for text generation.
- Load and split PDF documents into manageable chunks.
- Create embeddings for document chunks.
- Store embeddings in a vector store for efficient retrieval.
- Retrieve relevant documents based on user queries.
- Manage conversation history with memory.
- Deploy a conversational retrieval chain for interactive querying.

## Requirements

- Python 3.x
- Transformers
- Einops
- Accelerate
- Langchain
- Bitsandbytes
- Sentence Transformers
- PyPDF
- Huggingface_hub
- Langchain_huggingface
- Chroma

## Installation

1. Install Python 3.x if you haven't already.
2. Install the required packages using pip:

"""
pip install transformers einops accelerate langchain bitsandbytes sentence_transformers pypdf huggingface_hub langchain_huggingface chroma
"""

## Usage

### 01. Load the Large Language Model

Load the Large Language Model (LLM) using the `HuggingFacePipeline` from the `langchain.llms` module.

### 02. Load the Document

Load the PDF document using the `PyPDFLoader` from the `langchain.document_loaders` module.

### 03. Document Transform

Split the document into manageable chunks using the `CharacterTextSplitter` from the `langchain.text_splitter` module.

### 04. Embeddings

Create embeddings for the document chunks using the `HuggingFaceEmbeddings` from the `langchain_huggingface` module.

### 05. Storage

Store the embeddings in a local database (vector store) using the `Chroma` vector store from the `langchain.vectorstores` module.

### 06. Retrieval

Retrieve relevant documents based on user queries using the retriever interface from the vector store.

### 07. Memory

Manage conversation history with memory using the `ConversationBufferMemory` from the `langchain.memory` module.

### 08. Chain

Combine multiple components to create a single, coherent application using the `ConversationalRetrievalChain` from the `langchain.chains` module.

### 09. Deploying

Deploy the conversational retrieval chain for interactive querying. Continuously prompt the user for input and retrieve relevant responses from the chain.

## License

This project is licensed under the MIT License.

## Acknowledgments

- [LangChain](https://github.com/hwchase17/langchain) for providing the framework for building applications with LLMs.
- [Hugging Face](https://huggingface.co/) for providing the models and tools for NLP tasks.
