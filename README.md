# AI RAG Chatbot on Amazon Bedrock

This project guides you through building a powerful, personalized chatbot using a technique called Retrieval-Augmented Generation (RAG) on Amazon Web Services (AWS) with Amazon Bedrock. The chatbot is an expert on your provided documents, answering questions with accurate, domain-specific information.

## What is RAG?

RAG is an AI technique that combines a large language model (LLM) with a custom knowledge base. This enables the LLM to retrieve and use specific, up-to-date information to formulate a more informed and accurate response, moving beyond its pre-trained data.

## ![Project Architecture](/images/architecture.png)

The solution involves several key AWS services:

* **Amazon Bedrock:** The core managed service for building generative AI applications and accessing a variety of foundational models (FMs).

* **Knowledge Base:** Your chatbot's personal library for storing and processing documents.

* **Amazon S3:** The data source for your raw documents (e.g., text, PDFs).

* **OpenSearch Serverless:** The vector store that holds processed, numerical representations of your documents for fast and accurate semantic search.

* **AI Models:** The "brains" of the chatbot, including models for text embedding and generating human-like responses.

## Prerequisites

To get started, you will need:

* An **AWS Account**.

* Access to the **Amazon Bedrock** service (Needs IAM access, root won't work)

* Permissions to use the following Bedrock models:

    * `Titan Text Embeddings V2`

    * `Llama 3.1 8B Instruct` (or a similar text generation model)

## How to Get Started

1.  **Set Up:** Create a new Knowledge Base in Amazon Bedrock and configure an S3 bucket as its data source.

![s3](/images/s3.png)

![bedrock](/images/bedrock.png)

2.  **Access Models:** Request and gain access to the required foundation models in Bedrock.

![models](/images/baseModels.png)

3.  **Sync Documents:** Upload your documents to the S3 bucket and initiate the sync to ingest, chunk, and embed them, Here I put research papers on machine learning for testing.

4.  **Test:** Connect your Knowledge Base and AI model to test the chatbot's ability to answer questions.

![test](/images/chatbot.png)

![test](/images/chatbot_test.png)

![test](/images/chatbot_details.png)

## Learning Outcomes

* Implementing **Retrieval-Augmented Generation (RAG)**.

* Setting up an **AI Knowledge Base** on Amazon Bedrock.

* Using **Amazon S3** for data storage.

* Building a generative AI application by connecting various **AWS services**.