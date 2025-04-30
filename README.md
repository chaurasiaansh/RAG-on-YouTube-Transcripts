# 🎥 YouTube-RAG-Assistant

A LangChain-powered Retrieval-Augmented Generation (RAG) system that allows you to ask questions about YouTube videos using their transcripts. This project leverages vector embeddings, FAISS vector store, and Google Gemini to generate accurate and context-aware answers.

---

## 📌 Features

- 🔍 Extracts transcripts from YouTube videos.
- ✂️ Splits long transcripts into manageable chunks.
- 🧠 Generates vector embeddings using `nomic-embed-text`.
- 📚 Stores and retrieves relevant content using FAISS.
- 🤖 Uses **Google Gemini 2.0 Flash** to answer questions based on retrieved context only.
- 🛡️ Prevents hallucinations by restricting the model to the transcript content.

---

## 🚀 How It Works

1. **Transcript Ingestion**: Extracts captions from a YouTube video using `youtube_transcript_api`.
2. **Text Splitting**: Splits the transcript into overlapping chunks using `RecursiveCharacterTextSplitter`.
3. **Embedding Generation**: Converts text chunks into embeddings using Ollama's `nomic-embed-text`.
4. **Vector Storage**: Stores embeddings in a FAISS vector store.
5. **Retrieval & Prompting**: Retrieves relevant chunks for a given question and builds a prompt.
6. **Answer Generation**: Uses Google Gemini to answer the question based only on the retrieved content.

---

## 🛠️ Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/YouTube-RAG-Assistant.git
   cd YouTube-RAG-Assistant
