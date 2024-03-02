# Financial QA with LangChain and OpenAI 
<a href="https://github.com/sienlonglim/LangChain"><img alt="Static Badge" src="https://img.shields.io/badge/github-black?style=flat-square&logo=github"></a> 
<a href="https://document-query-bot.streamlit.app/"><img alt="Static Badge" src="https://img.shields.io/badge/Streamlit%20App-red?style=flat-square&logo=streamlit&labelColor=white"></a> 

This project implements FinQA using OpenAI's embedding models and LangChain's Python library.  The aim is to make a user-friendly Financial QA application with the ability to ingest data from multiple sources (word, pdf, txt, json)

## Application URL
https://gr8nishan-finrag.streamlit.app/

## Problem Statement

The sheer volume of financial statements makes it difficult for humans to access and analyze a business's financials. Robust numerical reasoning likewise faces unique challenges in this domain. In this work, we focus on answering deep questions about financial data, aiming to automate the analysis of a large corpus of financial documents. In contrast to existing tasks in the general domain, the finance domain includes complex numerical reasoning and an understanding of heterogeneous representations. To facilitate analytical progress, we propose a new large-scale dataset, FinQA, with Question-Answering pairs over Financial reports, written by financial experts.

## Dataset Used

- We used the dataset from this link
  https://github.com/czyssrs/finqa
- Data is present in below format
  - "pre_text": the texts before the table;
  - "post_text": the text after the table;
  - "table": the table;
  - "id": unique example id. composed by the original report name plus example index for this report.
  - "qa": {
    "question": the question;
     "program": the reasoning program;
     "gold_inds": the gold supporting facts;
     "exe_ans": the gold execution result;
     "program_re": the reasoning program in nested format;
  }

## Process
- Upload the json files downloaded from the datasources. Because of open ai token constraint we read only 100 rows for now.
- When the data is uploaded the data is cleaned. We remove all the irrevelant characters and fields before creating embeddings.
- Ask Question in the UI

## Domain areas include:
- Document splitting
- Embeddings (OpenAI)
- Vector database (Chroma / FAISS)
- Semantic search types
- Retrieval chain

![Screenshot](images/framework.png)

## Upcoming work:
- Capability to create embeddings for any amount of data 
- In memory vector database to cloud-native vector database
- Introduce conversation retriever and memory states
- Fine tuning model on FinQA dataset



