# n8n_Workflows


## 1. Inventory Agent

A simple `Inventory Agent` that retrieves or updates inventory data stored in a Google Sheet based on user input.

Nodes used: 

AI Agent, OpenAI Chat Model, Simple Memory, Get Inventory (Tools), Update Inventory (Tools)

![Inventory_Agent1](https://github.com/user-attachments/assets/2ebd7090-60f8-4026-aa2f-51b87a21281c)

![Inventory_Agent2](https://github.com/user-attachments/assets/d12d8900-c4fb-433b-8cd5-33309f94f164)

---

## 2. Order Status via Email

A simple workflow that retrieves order data from a Google Sheet and automatically sends an email notification to the specified recipient, updating them on the order status.

Nodes used: 

Google Sheet (anyUpdate), OpenAI (to compose email), Gmail (send: message)

![image](https://github.com/user-attachments/assets/c13e6716-3e14-4902-b9f5-136de8da7dc6)

---

## 3. RAG - Uploading PDF to Pinecode Vector Database

This workflow demonstrates how to implement a Retrieval-Augmented Generation (RAG) pipeline by downloading a PDF from Google Drive, chunking its content, generating embeddings, and storing them in a Pinecone vector database. This setup enables efficient retrieval of relevant information in response to user queries.

Nodes Used:

Google Drive (download: file), Pineconde Vector Store, OpenAI Embeddings, Default Data Loader, Recursive Character Text Splitter

![Uploading PDF to Pinecode Vector Database](https://github.com/user-attachments/assets/4d59ef5d-8bdc-4eaa-a412-0c612111b03d)

---

## 4. RAG - AI Agent

An AI agent retrieves relevant information from the Pinecone vector database built in the prior workflow to answer user questions effectively. If the information is not availale in the database, it will make use of Wikipedia to answer the user's query

Nodes Used:

AI Agent, OpenAI Chat Model, Simple Memory, Pineconde Vector Store, OpenAI Embeddings, Wikipedia

![RAG - AI Agent](https://github.com/user-attachments/assets/cc034ea2-da02-43e2-91d7-e68e5b23a19a)

---

## 5. RAG with Supabase & Postgres

This workflow demonstrates how to implement a Retrieval-Augmented Generation (RAG) pipeline by downloading a PDF from Google Drive, chunking its content, generating embeddings, and storing them in a Supabase vector database. This setup enables efficient retrieval of relevant information in response to user queries. Also, an AI agent retrieves relevant information from the Supabase vector database built in the prior workflow to answer user questions effectively.

Nodes Used:

Google Drive (download: file), Supabase Vector Store, OpenAI Embeddings, Default Data Loader, Recursive Character Text Splitter, 

AI Agent, OpenAI Chat Model, Simple Memory, Supabase Vector Store, OpenAI Embeddings, Wikipedia

![image](https://github.com/user-attachments/assets/c0e325f4-9f59-49d6-aeb8-8664bde347fc)


---

