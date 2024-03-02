# Financial Question Answering(QA) with LangChain and OpenAI 
<a href="https://github.com/sienlonglim/LangChain"><img alt="Static Badge" src="https://img.shields.io/badge/github-black?style=flat-square&logo=github"></a> 
<a href="https://document-query-bot.streamlit.app/"><img alt="Static Badge" src="https://img.shields.io/badge/Streamlit%20App-red?style=flat-square&logo=streamlit&labelColor=white"></a> 

This project implements QA using OpenAI's embedding models and LangChain's Python library.  The aim is to make a user-friendly Financial QA application with the ability to ingest data from multiple sources (word, pdf, txt, json)

Dataset Used

- We used the dataset from this link
  https://github.com/czyssrs/finqa

Process -
- Upload the json files downloaded from the datasources. Because of open ai token constraint we read only 100 rows for now.
- Ask Question in the UI


Domain areas include:
- Document splitting
- Embeddings (OpenAI)
- Vector database (Chroma / FAISS)
- Semantic search types
- Retrieval chain

![Screenshot](images/framework.png)

## Upcoming works:
- Capability to create embeddings for any amount of data 
- In memory vector database to cloud-native vector database
- Introduce conversation retriever and memory states
- Fine tuning model on FinQA dataset



