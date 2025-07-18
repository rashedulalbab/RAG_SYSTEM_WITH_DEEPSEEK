# 🧠 Simple RAG System using DeepSeek and LangChain

This project implements a simple **Retrieval-Augmented Generation (RAG)** system that uses `LangChain` and `DeepSeek` LLMs to answer questions based on the content of a given PDF document. It utilizes semantic chunking, FAISS vector search, and a RetrievalQA chain.

---

🚀 How It Works
📄 Document Loading
The system uses PDFPlumberLoader from langchain_community to extract text from a PDF file.

🧩 Semantic Chunking
The extracted text is broken into semantically meaningful chunks using SemanticChunker, improving contextual retrieval.

🔢 Embedding Generation
Each chunk is converted into a high-dimensional vector using HuggingFaceEmbeddings.

📦 Vector Store Creation
The embedded chunks are stored in a FAISS vector database, allowing fast similarity searches.

🤖 Retrieval-Augmented Generation (RAG)

A retriever is built from the FAISS vector store.

The retriever fetches the most relevant chunks based on the input query.

A language model (e.g., DeepSeek or any LLM) answers the query using retrieved context through a RetrievalQA chain.


