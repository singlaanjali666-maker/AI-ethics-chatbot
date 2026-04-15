#  RAG Chatbot using MistralAI & Gemini Embeddings

##  Overview
This project implements a **Retrieval-Augmented Generation (RAG) Chatbot** that allows users to interact with documents using natural language. It combines document retrieval with LLM-based responses to provide accurate and context-aware answers.

The chatbot is built using a modular pipeline including text splitting, embeddings, vector storage, and conversational AI.

---

##  Features
-  Upload and process PDF documents  
-  Semantic search using embeddings  
- Conversational AI powered by MistralAI  
-  Context-aware responses using memory  
-  Fast retrieval with in-memory vector store  
- End-to-end RAG pipeline  

---

 Architecture

The workflow consists of the following components:

1. **Text Splitter**
   - Recursive Character Text Splitter
   - Chunk Size: 1000
   - Overlap: 200

2. **File Loader**
   - Loads PDF document
   - Connects with text splitter

3. **Embeddings**
   - Google Gemini Embeddings (`gemini-embedding-001`)
   - Converts text into vector representations

4. **Vector Store**
   - In-Memory Vector Store
   - Stores embeddings for retrieval

5. **Retriever**
   - Fetches top relevant chunks (Top K = 4)

6. **LLM (Chat Model)**
   - MistralAI (`mistral-tiny`)
   - Generates responses based on retrieved context

7. **Memory**
   - Buffer Memory for conversation tracking

8. **Conversational Retrieval QA Chain**
   - Combines retriever + LLM + memory
   - Produces final chatbot response

---

 Workflow
PDF → Text Splitter → Embeddings → Vector Store → Retriever
→ MistralAI → Conversational QA Chain → Chatbot Response
<img width="1847" height="873" alt="rag(2)" src="https://github.com/user-attachments/assets/38dc6d16-5e66-4f8b-a4d7-dae5ccd2a256" />


---

 Tech Stack
- **LLM:** MistralAI  
- **Embeddings:** Google Gemini  
- **Framework:** LangChain / Flow-based AI tool  
- **Vector Store:** In-Memory  
- **Language:** Python  

---

 Use Case

This chatbot is designed to answer questions from the document:

**"AI Ethics: Integrating Transparency, Fairness, and Privacy in AI Development"**

It helps users:
- Understand AI ethics concepts  
- Explore fairness, transparency, and privacy  
- Analyze global AI frameworks (EU, US, China)  

---

 Example Query
What is the document about?

 Output:
- Ethical concerns in AI  
- Key principles: transparency, fairness, privacy  
- Global AI policy comparisons  
- Bias mitigation strategies  

---

 Setup Instructions

1. Clone the repository:
```bash
git clone https://github.com/your-username/rag-chatbot.git
cd rag-chatbot
2.Install dependencies:
pip install -r requirements.txt
Add API Keys:
MistralAI API Key
Google Gemini API Key
3.Run the project:
python app.py
4. Future Improvements
 Persistent vector database (FAISS / Pinecone)
 Web UI integration
 Multi-document support
 Authentication & user sessions
5. Contributing

Contributions are welcome! Feel free to fork this repo and submit a pull request.

License

This project is for educational purposes.
 Author

Anjali singla
