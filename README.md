# n8n_Workflows


## 1. Inventory Agent

A simple `Inventory Agent` that retrieves or updates inventory data stored in a Google Sheet based on user input.

``Nodes used:`` 

AI Agent, OpenAI Chat Model, Simple Memory, Get Inventory (Tools), Update Inventory (Tools)

![Inventory_Agent1](https://github.com/user-attachments/assets/2ebd7090-60f8-4026-aa2f-51b87a21281c)

![Inventory_Agent2](https://github.com/user-attachments/assets/d12d8900-c4fb-433b-8cd5-33309f94f164)

---

## 2. Order Status via Email

A simple workflow that retrieves order data from a Google Sheet and automatically sends an email notification to the specified recipient, updating them on the order status.

``Nodes used:``

Google Sheet (anyUpdate), OpenAI (to compose email), Gmail (send: message)

![image](https://github.com/user-attachments/assets/c13e6716-3e14-4902-b9f5-136de8da7dc6)

---

## 3. RAG - Uploading PDF to Pinecode Vector Database

This workflow demonstrates how to implement a Retrieval-Augmented Generation (RAG) pipeline by downloading a PDF from Google Drive, chunking its content, generating embeddings, and storing them in a Pinecone vector database. This setup enables efficient retrieval of relevant information in response to user queries.

``Nodes Used:``

Google Drive (download: file), Pineconde Vector Store, OpenAI Embeddings, Default Data Loader, Recursive Character Text Splitter

![Uploading PDF to Pinecode Vector Database](https://github.com/user-attachments/assets/4d59ef5d-8bdc-4eaa-a412-0c612111b03d)

---

## 4. RAG - AI Agent

An AI agent retrieves relevant information from the Pinecone vector database built in the prior workflow to answer user questions effectively. If the information is not availale in the database, it will make use of Wikipedia to answer the user's query

``Nodes Used:``

AI Agent, OpenAI Chat Model, Simple Memory, Pineconde Vector Store, OpenAI Embeddings, Wikipedia

![RAG - AI Agent](https://github.com/user-attachments/assets/cc034ea2-da02-43e2-91d7-e68e5b23a19a)

---

## 5. RAG with Supabase & Postgres

This workflow demonstrates how to implement a Retrieval-Augmented Generation (RAG) pipeline by downloading a PDF from Google Drive, chunking its content, generating embeddings, and storing them in a Supabase vector database. This setup enables efficient retrieval of relevant information in response to user queries. Also, an AI agent retrieves relevant information from the Supabase vector database built in the prior workflow to answer user questions effectively.

``Nodes Used:``

Google Drive (download: file), Supabase Vector Store, OpenAI Embeddings, Default Data Loader, Recursive Character Text Splitter, 

AI Agent, OpenAI Chat Model, Simple Memory, Supabase Vector Store, OpenAI Embeddings, Wikipedia

![image](https://github.com/user-attachments/assets/c0e325f4-9f59-49d6-aeb8-8664bde347fc)

---

## 6. Customer Support AI Agent

This workflow is triggered when a new email arrives in your Gmail inbox.
The email is automatically classified into one of two categories: Customer Support or Other.

``Customer Support:``

The email is forwarded to an AI Agent, which uses a Pinecone vector store to reference your knowledge base and generate a well-formatted response. This response is then sent to the customer via the Gmail node.

``Other:``

No action is taken for emails classified as "Other."

``Nodes Used:``

Gmail (Email: Received), Email Classifier, Email Classifier - OpenAI Chat Model, AI Agent, Agent (OpenAI) Chat Model, OpenAI Embeddings, Pinecone Vector Store, Gmail (Email: Reply)

![image](https://github.com/user-attachments/assets/c8112324-b616-44e9-b049-19b41b616660)

---

## 7. LinkedIn Content Creator Agent

This workflow is triggered manually. It reads topics listed in a Google Sheet stored in your Google Drive.
For each topic, it performs a web search and retrieves at least three relevant results.
An AI agent then analyzes the search results and generates a concise summary for each topic.
Finally, the generated information is updated back into the same Google Sheet from which the topics were originally fetched.

``Nodes Used:``

Manual Trigger using a Click, Get topic from Google Sheet, Tavily Search using HTTP request, AI Agent, Agent (OpenAI) Chat Model, Updating the Google Sheet

![image](https://github.com/user-attachments/assets/dc8a4e1b-23b7-4c86-8b76-21d8a78d50d9)

---

## 8. RAG with Vectorize

In this project, I’ve created an AI agent using n8n that interacts with a Pinecone vector store as its knowledge base. The vector store was prepopulated using Vectorize, ensuring high-quality, semantically relevant data retrieval. The agent can effectively answer user questions by fetching and reasoning over the most relevant context from the vector store.

``Nodes Used:``

AI Agent, OpenAI Chat Model, Simple Memory, Pinecone Vector Store, OpenAI Embeddings

Vectorize Platform is a RAG-as-a-Service that handles the messy, complex parts of AI development—so you can focus on building intelligent applications.

![Screenshot 2025-04-12 164109](https://github.com/user-attachments/assets/ea7d346d-2cff-4d53-b8c8-4088fa4538fe)

![image](https://github.com/user-attachments/assets/99cbba46-2d7f-4aad-8b92-b28d5dd3173f)

---

## 9. Firecrawl for Webpage Data Extraction

1. **Extract website data** using Firecrawl APIs from one or multiple pages.

2. **Poll (Wait) for completion**, ensuring extraction is finished before proceeding.

3. **Save the extracted data** directly into an existing Google Sheet.

4. **Handle failures gracefully** by sending an automated email notification to the tool owner.

``Nodes Used:``

Manual Trigger node, HTTP requests to Firecrawl API Endpoints, Switch based on response, Wait if response is processing, Code for data refinement, Google Sheet to Save the response, Gmail to Send Message for Failure and Cancel.

![image](https://github.com/user-attachments/assets/a0d41ffe-33e2-4324-b6ff-7fa57ece2215)

---
