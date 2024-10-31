# SMART LEARNING SYSTEM - Model Development (Colab)

This README describes the process and components involved in developing the **Synapse** model within Google Colab. The Colab environment was used to train and prepare a custom model focused on educational query responses, integrating multiple components such as pre-trained language models, vector databases, RAG Methods and fine-tuning strategies.

---

## Project Objective

The primary goal of the model development was to create a chatbot focused on answering educational queries accurately and contextually. This was achieved by leveraging pre-trained language models and enhancing them with a **Retrieval-Augmented Generation (RAG)** setup to ensure responses are relevant, concise, and rich in information.

---

## Key Components

### 1. Language Models

- **Hugging Face GPT-2 (Pre-trained)**
  - **Parameters**: 1.5 billion
  - **Purpose**: Used for tokenizing and encoding the dataset, allowing the chatbot to understand context and generate coherent responses.
  - **Dataset**: Trained on the `lucadiliello/wikipedia_512_pretraining` dataset from Hugging Face, which is a collection of tokenized Wikipedia entries segmented into 512-token blocks.

- **Ollama LLama2 (Synapse Model)**
  - **Parameters**: Configurable, optimized for effective educational response generation.
  - **Purpose**: LLaMA2 serves as the core language model in our chatbot, providing reliable and contextually rich answers while balancing memory usage and performance.
    
- **BART-Large-CNN (Facebook’s BART)**
  - **Parameters**: 406 million
  - **Role in RAG**: Serves as the Retrieval-Augmented Generation (RAG) model, which retrieves contextually relevant information and combines it with GPT-2 generated responses to ensure answer depth.
  - **Usage**: Enhanced generation process through its pre-trained summarization capabilities, which allows for both summary and extended responses.

### 2. Dataset

- **`lucadiliello/wikipedia_512_pretraining`**:
  - **Source**: Hugging Face
  - **Size**: Wikipedia entries tokenized into 512-token segments.
  - **Purpose**: Trains the model to understand general academic topics and provides a broad context for answering a variety of educational questions.

### 3. Vector Database

- **FAISS (Facebook AI Similarity Search)**
  - **Role**: Manages and retrieves vectors for query-based searches, allowing quick and relevant retrieval of data embeddings related to the user’s question.
  - **Storage**: Vector embeddings are stored in FAISS to ensure rapid and accurate access to relevant content when generating responses.

---

## Model Development Process

### 1. Initial Dataset Preparation
   - The `lucadiliello/wikipedia_512_pretraining` dataset from Hugging Face was used to pretrain the GPT-2 model, providing the chatbot with a base knowledge of general topics. Tokenization was handled by Hugging Face’s `transformers` library.

### 2. RAG Model Integration
   - **BART-Large-CNN** was integrated into a **Retrieval-Augmented Generation** setup. By combining BART with FAISS, the chatbot could retrieve relevant contextual data and feed it into the Llama2 model for answer generation.
   - This process enables responses that are both coherent and contextually appropriate to educational topics.

### 3. FAISS Indexing
   - The vector embeddings created from the Wikipedia dataset were stored in a FAISS index, allowing for rapid retrieval based on user queries.
   - **Pickle Storage**: Vector data and FAISS indices were serialized and stored in pickle files for easy loading and deployment.

### 4. Model Testing and Evaluation
   - Extensive testing was conducted in Colab, ensuring that the model generates relevant, accurate responses based on sample educational queries.
   - The output was evaluated for accuracy, coherence, and educational relevance, with refinements applied as needed.

---

## Output and Usage Summary

The Colab notebook provided a proof-of-concept implementation of the chatbot’s functionality, simulating real-world educational queries and generating precise answers using the combined capabilities of Llama and BART-Large-CNN in the RAG setup. FAISS indexing further enhanced the retrieval speed and relevance of the model’s responses.

---

## Deployment Notes

Upon successful testing in Colab, the trained models, FAISS index, and custom logic were exported to be integrated within the Flask application in `app.py`. This setup enables the **SynapseEd** to function seamlessly in a web-based environment, ready for user interaction and real-time educational assistance.

---

## Summary

The Colab model development provided a robust foundation for the **Synapse** chatbot, combining multiple technologies to create an efficient, educational response system that is optimized for fast, accurate answers.
