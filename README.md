# SynapseEd

The **SynapseEd** is an AI-powered, educational chatbot designed to answer academic queries with high accuracy and relevance. Built using a combination of advanced NLP technologies, the system integrates Deep Learning models with a custom frontend for an engaging user experience. 

---

## Project Overview

### Purpose
The system is created to provide users with precise, reliable answers to educational questions. It leverages multiple LLM models, a vector database for knowledge retrieval, We also developed our own Synapse LLM model and an intuitive web interface, making it an efficient tool for learning and exploring academic topics.

### Key Features
- **Education-focused chatbot**: Handles educational queries with accuracy.
- **Automated Summarization**: Responses are customized based on length, either summarized or expanded.
- **YouTube Content Retrieval**: Displays relevant YouTube videos alongside answers for multimedia learning.

---

## How It Works

The **SynapseEd** uses a combination of RAG (Retrieval-Augmented Generation) and LLM (Large Language Model) technologies to ensure that responses are accurate, educational, and context-aware.

1. **User Input**: The user submits a question via the search bar.
2. **Data Retrieval**: The query is processed by a vector database (FAISS) to find the most relevant data.
3. **Response Generation**: A Synapse model, combining **TinyLlama** or **Llama2**(based on system configuration) and **BART-Large-CNN**, generates an answer. If the response is short, it gets expanded; if it’s long, a summary is provided.
4. **YouTube Video Display**: Relevant video content is fetched and shown in a separate container.

---

### Technologies Used

1. **Flask**: Backend framework for handling web requests and data processing.
2. **RAG Model (BART-Large-CNN)**: Retrieves data and answers based on context, optimizing for relevance.
3. **Llama2 (Synapse Model)**: This efficient LLM was chosen to locally power the chatbot, integrated using Ollama.
4. **FAISS (Facebook AI Similarity Search)**: Manages and searches vectorized data for quick and relevant answer retrieval.
6. **Frontend (HTML/CSS/JavaScript)**: Engaging web interface with a dynamic search bar, answer container, and YouTube video integration.

---

Feel free to explore, contribute, and make this Synapse Learning Platform project even more valuable for Students and other users..!

### If you’re interested in learning more about this project or discussing potential collaborations, feel free to reach out at vinmaytondle@gmail.com (With the reference of project repository title in your message.).
    
## For more Info-
  visit -: vinmaytondle.netlify.app
