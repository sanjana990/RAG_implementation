# 💬 RAG-Based Chatbot for Piping Design Manual

This is a Retrieval-Augmented Generation (RAG) chatbot built during my internship. It is designed to answer engineering-specific questions using the **Piping Design Manual** as a knowledge base. The chatbot retrieves relevant content from the manual and generates helpful, context-aware responses using a local language model.

---

## 📌 Project Objective

To enable domain-specific Q&A by combining:

- Document parsing and chunking
- Semantic search using vector embeddings
- Local language model response generation

This system was specifically tested using the **Piping Design Manual PDF**, making it useful for engineers and technical professionals.

---

## ⚙️ Tech Stack

- **Python**
- **Streamlit** – for the user interface  
- **LangChain** – for RAG architecture and prompt chaining  
- **Ollama** – to run local LLMs  (Used Llama3.2 model here)
- **pdfplumber** – to extract text from PDF  
- **ChromaDB** – as the vector store  
- **Unstructured** – to clean and segment text into chunks  
- **NumPy** – for utility functions and display

---

## 🧠 How It Works

1. **PDF Parsing**: The Piping Design Manual is read using `pdfplumber` and processed using `unstructured`.
2. **Chunking**: The document is split into manageable chunks.
3. **Embedding**: Chunks are embedded and stored in `ChromaDB`.
4. **Retrieval**: When a query is entered, the top relevant chunks are retrieved.
5. **Generation**: A local LLM via Ollama generates a final response using the retrieved content.
6. **Interface**: The interaction happens through a `Streamlit` app.

---

##  Installation & Usage

1. **Clone the Repository**

```bash
git clone https://github.com/your-username/rag-piping-chatbot.git
cd rag-piping-chatbot
```

2. **Install Dependencies**

```bash
pip install -r requirements.txt
```

3. **Add the PDF**

   Place the Piping Design Manual PDF inside the data/ folder.


4. **Run the Streamlit App**
```bash
streamlit run streamlit_app.py
```


---



## Example Queries

Here are some sample questions you can ask the chatbot:


 1. What are the standard pipe sizes for industrial plants?

 2. Explain the spacing rules for flanges.

 3. What materials are used in high-pressure pipe systems?

 4. What are the recommended design guidelines for pipe supports?


---   

   
## 🗂️ Folder Structure

```bash
├── streamlit_app.py               # Main Streamlit chatbot app
├── updated_rag_notebook.ipynb     # RAG pipeline in notebook format
├── requirements.txt               # Required Python packages
├── data/                          # Folder to place the PDF

```

