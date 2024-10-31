Colab Model Development
The model was initially developed in Google Colab. Below are the details:

Models and Dataset
Hugging Face LLM (GPT-2):

Parameters: 1.5 billion
Dataset: lucadiliello/wikipedia_512_pretraining, a tokenized Wikipedia dataset used for pretraining, helping the model grasp general knowledge and context on various topics.
Vector Database:

Tool: FAISS (Facebook AI Similarity Search)
Purpose: Stores vector embeddings for fast, relevant data retrieval, ensuring that the model can quickly find relevant text based on user queries.
Ollama TinyLlama (Synapse Model):

Size: Lightweight, with optimized response speed for local systems.
Purpose: Used as the primary LLM in the chatbot to manage answer generation effectively.
RAG Model Integration
BART-Large-CNN:
Parameters: 406 million
Purpose: Enables retrieval-augmented generation (RAG) to enhance response relevance by combining retrieved content with generated answers.
Integration: RAG model pulls relevant data from FAISS to provide accurate, contextually rich answers based on user queries.
Usage Guide
Enter Your Query: Use the search bar to type in an academic question.
Receive Answer and Video: The chatbot will respond with an answer in the middle section, while the left side displays either a summary or an extended response.
View Relevant Videos: The right side shows related YouTube videos based on your query.
Contribution
Contributions are welcome if aligned with the project’s educational goals. Please ensure familiarity with Reflex, FAISS, and Flask before contributing.

License
This project is licensed under a proprietary license, with permissions limited to educational and non-commercial research use.

Credits
Project developed by Mr. Vinmay Tondle, Mr. Rushikesh Bobale, and Miss Priyanka Kapade. Special thanks for the integration of Synapse and the RAG model.
