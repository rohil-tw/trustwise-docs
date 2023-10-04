# Starter Tutorial

```{tip}
Make sure you've followed the [installation](installation.md) steps first.
```

In this starter example, we will show how to log and monitor LLM evaluation metrics using Trustwise's Hallucinations Observability Plugin (HOP).


## What is HOP?

HOP is an extension designed to help you evaluate your Large Language Models RAG pipelines. RAG pipelines can be built using various tools like llamaindex, langchain etc. But in this example, we will show how to use HOP with llamaindex.

## Prerequisites
To use HOP, you should already be familiar with the basics of the llamaindex including loading documents, parsing them into nodes, constructing an index, and querying the index to get responses.


## 1. Load documents
Firstly, load documents through a data loader. Create a folder called `data` and place your docs (in this example, we will use a `.pdf` file) in it. Use llamaindex's `SimpleDirectoryReader` to load the docs.

```
<code snippet>
```

## 2. Create an index from the documents
Create an index from your documents using llamaindex `VectorStoreIndex` class This step will convert the documents into nodes and create an index.

```
<code snippet>
```

## 3. Query the Index
Query the index with a sample query to receive a response. Ensure that you have already completed the basic llamaindex flow up to this point.
```
<code snippet>
```

## 4. Evaluate LLM response

```
<code snippet>
```
