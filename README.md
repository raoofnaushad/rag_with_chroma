# Retrieval Augmented Generation (RAG) Overview

## Introduction to RAG

Retrieval Augmented Generation (RAG) is a unified system designed to streamline the process from document extraction to answer generation, particularly in domain-specific question-answering applications. It addresses the limitations of Large Language Models (LLMs) such as hallucinations and the need for relevant context in domain-specific queries.

## RAG Components

RAG involves several key components:

1. **Text Splitter**: Splits documents to fit the context windows of LLMs.
2. **Embedding Model**: A deep learning model for generating document embeddings.
3. **Vector Stores**: Databases for storing and querying document embeddings and their metadata.
4. **LLM**: The Large Language Model, like OpenAI API, responsible for generating answers.
5. **Utility Functions**: Includes tools such as Web retrievers and document parsers for retrieval and pre-processing.

For our implementation, we use LlamaIndex and Chroma Store along with OpenAI's API as the LLM.

## Llama Index (GPTIndex)

Llama Index is a Python-based framework for building LLM applications. It provides:

- Data ingestion from various sources.
- Vector databases for indexing.
- Query interfaces for large documents.

Llama Index is versatile, integrating with other applications like Langchain, Flask, Docker, etc.

More information: [Llama Index GitHub Repository](https://github.com/run-llama/llama_index)

## Chroma

Chroma is an open-source embedding database aimed at enhancing LLM apps by providing:

- Storage for embeddings and metadata.
- Tools to embed documents and queries.
- Embedding search functionality.

Chroma focuses on simplicity, developer productivity, and efficient search, with an emphasis on analysis over search results.
More information: [Chroma Documentation](https://docs.trychroma.com/)

# LLaMAindex and Chroma Vector Store Integration

A dynamic exploration of LLaMAindex with Chroma vector store, leveraging OpenAI APIs. This repository contains four distinct example notebooks, each showcasing a unique application of Chroma Vector Stores ranging from in-memory implementations to Docker-based and server-based setups.

## Example Notebooks Overview

### Example 1: In-Memory Chroma Vector Store

Demonstrates setting up and using an in-memory Chroma Vector Store, ideal for basic functionalities and rapid prototyping.

### Example 2: Persistent Chroma Vector Store

Illustrates writing a Chroma Vector Store to disk for persistent storage, crucial for maintaining vector store data between sessions.

### Example 3: ChromaDB with Docker

A guide to running ChromaDB in a Docker container, suitable for containerized solutions. Prerequisites:

```bash
git clone git@github.com:chroma-core/chroma.git
docker-compose up -d --build
```

### Example 4: ChromaDB Running as a Server

Explores running ChromaDB as a server for scalable applications. Steps to get started:

```bash
pip install chromadb
chroma run --path /db_path
```

Each notebook provides practical, hands-on experience, ensuring a comprehensive understanding of integrating LLaMAindex with the Chroma vector store.
