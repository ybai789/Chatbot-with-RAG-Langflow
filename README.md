# Building RAG and Agentic Applications with No-Code Using Langflow

This project demonstrates how to build a **Retrieval-Augmented Generation (RAG)** and **Agentic Application** from scratch without writing any code, using the powerful visual interface of **Langflow**. The entire knowledge base is dynamically created within Langflow, integrating with **Astra DB** to enable intelligent, contextual interactions. The chatbot utilizes Langflow's workflows to process documents, generate embeddings, and provide accurate, conversational responses to user queries.

------

## Features

1. **No-Code Knowledge Base Creation**:
   - Use LangFlow to upload, process, and store documents directly in a vector database.
   - Build the entire knowledge base dynamically without preloading or external scripts.
2. **Document Processing and Embedding Generation**:
   - LangFlow splits documents into manageable chunks and generates embeddings using **OpenAI's text-embedding models**.
   - Stores these embeddings seamlessly in **Astra DB** for efficient vector-based retrieval.
3. **Agentic Query and Retrieval**:
   - Dynamically retrieve relevant data from the knowledge base using LangFlow's no-code Retriever flow.
   - Empower the chatbot with contextual understanding for domain-specific queries.
4. **Interactive Chatbot**:
   - Build a chatbot capable of answering user queries by accessing the knowledge base created within LangFlow.
   - Ensure precise and contextually accurate responses tailored to user needs.

------

## Why Langflow?

Langflow simplifies the creation of RAG pipelines and agentic applications by providing a visual interface for workflow design. It eliminates the need for coding, enabling anyone—regardless of technical background—to create intelligent, dynamic knowledge-based applications.

------

## Architecture Overview

### **1. Knowledge Base Creation Flow (Load Data Flow)**

- **Input**: Documents uploaded directly into LangFlow (e.g., PDFs).
- Workflow:
  1. LangFlow's **Split Text** component processes the document into chunks.
  2. Generates embeddings for each chunk using **OpenAI API**.
  3. Stores embeddings in Astra DB, creating a fully searchable knowledge base.

<img src=".\images\load_data_flow.png" alt="arch" style="zoom:40%;" />

### **2. Retrieval Flow**

- **Input**: User's question.
- Workflow:
  1. Matches the query against the dynamically created knowledge base in Astra DB.
  2. Retrieves the most relevant information using Langflow's Retriever components.
  3. Responds with accurate and contextual answers to user queries.

<img src=".\images\retrieve_flow.png" alt="arch" style="zoom:40%;" />

------

## Getting Started

### Prerequisites

- **LangFlow**: Installed and configured for building no-code workflows.
- **OpenAI API Key**: For embedding generation.
- **Astra DB Application Token**: For vector database integration.

### Steps

1. **Create the Knowledge Base**:
   - Upload your document (e.g., `Dengue_Fever_An_Overview.pdf`) into Langflow.
   - Use Langflow's load data flow to process the document, generate embeddings, and store them in Astra DB.
2. **Run the Retrieve Flow**:
   - Input user queries through the chatbot interface.
   - Get responses dynamically fetched from the knowledge base.

------

## Example Interaction

- **User**: "What is this document about?"
- **Chatbot Response:**

<img src=".\images\response.png" alt="arch" style="zoom:40%;" />

------

## Use Cases

- **Medical Assistants**: Build a chatbot that retrieves information from dynamically created medical documents.
- **Interactive FAQ Systems**: Create a system that provides instant answers to user queries for businesses or organizations.
- **Knowledge Management**: Enable semantic search and retrieval for dynamically uploaded documents in enterprise environments.

------





