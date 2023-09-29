# Trustwise HOP with LlamaIndex example

## Introduction

Welcome to TW Hallucinations Obserability Plug-in (HOP), an extension designed to help you evaluate your Large Language Models RAG pipelines when using the Llama Index project. This documentation will guide you through the steps to use HOP effectively.

## Getting Started
To use HOP, you should already be familiar with the basics of the Llama Index project, including loading documents, parsing them into nodes, constructing an index, and querying the index to get responses.

## 1. Load Documents
You can load documents manually or through a data loader. Make sure you have your documents ready for processing.

Using a SimpleDirectoryReader from Llama Index to load documents from a directory called 'data'
```
from llama_index import VectorStoreIndex, SimpleDirectoryReader
documents = SimpleDirectoryReader('data').load_data()
```

## 2. Parse the Documents into an Index
Use the Llama Index functionality to create Vector Stores to parse your loaded documents into nodes and create an index.

```
index = VectorStoreIndex.from_documents(documents)
```

## 3. Query the Index
Query the index with a sample query to receive a response. Ensure that you have already completed the basic Llama Index flow up to this point.

```
query_engine = index.as_query_engine()

query = ""

response = query_engine.query(query)
```

## 4. Import TW Functionalities
Trustwise Functionalities allow you to parse the response from the index. 
```
git clone https://github.com/tw-gtm/tw-api-testing.git
```
```
import tw_functions as tw
```

## 5. Evaluate

```
result = tw.Functions.evaluate(query, response)
```