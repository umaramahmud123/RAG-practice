# RAG-practice

RAG Practice: Question Answering Over Lecture Notes
Overview

This project demonstrates how to build a Retrieval-Augmented Generation (RAG) pipeline to retrieve and answer questions from lecture notes. The system processes internal documents, generates vector embeddings for each document chunk, stores them in a vector database, and retrieves the most relevant chunks when a user asks a question.

The project focuses on RAG architecture and vector search to efficiently answer questions grounded in document data.

Project Objectives

This project aims to achieve:

Implement a RAG pipeline to answer questions based on document data.

Apply structure-aware chunking and semantic search techniques.

Understand embeddings, vector databases, and retrieval-based QA systems.
Technologies Used
Embedding Model:

sentence-transformers/all-MiniLM-L6-v2

A lightweight, fast, and open-source model for generating semantic vector embeddings.

Vector Database:

FAISS (Facebook AI Similarity Search)

Used for efficient similarity search, storing and retrieving embeddings quickly.

Environment:

Python

Google Colab / Jupyter Notebook

sentence-transformers

FAISSRAG Pipeline Architecture

This is the core structure of the Retrieval-Augmented Generation (RAG) system:

Document Loading

The system loads internal lecture notes from DOCX files.

Chunking

Documents are split into smaller chunks using structure-aware chunking based on headings and paragraphs.

Embedding Generation

Each chunk is converted into a vector embedding using sentence-transformers/all-MiniLM-L6-v2.

Vector Indexing

Embeddings are indexed and stored in FAISS for efficient similarity search.

Query Processing

User queries are converted into embeddings using the same model.

Retrieval

The FAISS index retrieves the most similar document chunks to the query.

Answer Retrieval

The most relevant chunks are returned as the contextual answer.
