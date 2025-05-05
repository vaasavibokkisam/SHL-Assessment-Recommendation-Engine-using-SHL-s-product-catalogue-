# SHL-Assessment-Recommendation-Engine-using-SHL-s-product-catalogue-
his project is a web-based recommendation system that suggests the most relevant SHL assessments based on user input such as job roles, skills, or competency requirements. It is built using Streamlit, sentence-transformers, and ChromaDB, and follows a Retrieval-Augmented Generation (RAG) pattern to enhance relevance and interpretability.
# Create a Sample SHL Product Catalog
To simulate a real SHL assessment catalog, you'll create a simple CSV file with key fields such as:

product_name

description

competencies

job_roles
# Load and Use the Data
# Data Cleaning & Preprocessing
# Save Cleaned Data
### Build the Recommendation Engine (user query ➝ semantic search ➝ top matches)
# Embedding & Vector Store
->Used HuggingFace SentenceTransformer (all-MiniLM-L6-v2) to create embeddings from the full assessment text.

->Split the text into manageable chunks using LangChain’s RecursiveCharacterTextSplitter.

->Stored the vector embeddings in ChromaDB, enabling semantic search based on user input.
# LLM-Powered Recommendation
->Used LangChain + Groq LLaMA-3 to set up a RetrievalQA chain.

->When a user enters a query in the Streamlit UI:

->The model searches the most relevant assessments from ChromaDB.

->The result is passed to the LLM which provides a recommendation as a response.
#  Streamlit App
->Interactive front-end built with Streamlit.

->Users enter queries through a text box.

->The app returns recommended SHL assessments in real-time.
# Technologies Used:
Streamlit for UI

LangChain for chaining LLM and retriever

HuggingFace for embeddings

ChromaDB for vector search

Groq LLaMA3 for LLM responses

Optional deployment via localtunnel or ngrok

# How It Works
->Data Cleaning: Raw SHL catalog is cleaned and merged into a unified combined_text field.

->Embedding: Sentence embeddings are created using a lightweight transformer.

->Vector Storage: All text embeddings are stored in ChromaDB.

->User Query: User enters a free-form query like "Looking for a test to assess leadership potential for team leads."

->Semantic Retrieval: The app finds similar catalog items via vector search.

->LLM Recommendation: Groq LLaMA-3 provides a concise, context-aware recommendation.
#  API Key(groq,open ai)
 you must set your ChatGroq API key in your environment
->>>>>> GROQ_API_KEY="your-api-key-here"<<<-


