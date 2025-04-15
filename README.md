# HybirdSerach


Here’s a clean and informative `README.md` file for your hybrid search project using Pinecone, HuggingFace, BM25, and LangChain:

---

### 📁 `README.md`

```markdown
# 🔍 Hybrid Search with Pinecone, HuggingFace, BM25 & LangChain

This project demonstrates a **hybrid semantic search system** that combines:
- **Dense embeddings** using HuggingFace transformers
- **Sparse retrieval** using BM25 encoding
- **Pinecone** as the vector database
- **LangChain** to build a powerful retriever

---

## 🚀 Features

- ✅ Semantic search using sentence-transformers (MiniLM)
- ✅ Keyword-aware sparse retrieval using BM25
- ✅ Efficient hybrid search in Pinecone
- ✅ Easy integration with LangChain pipelines

---

## 🛠️ Setup

### 1. Clone the repo

```bash
git clone https://github.com/your-username/hybrid-search-langchain-pinecone.git
cd hybrid-search-langchain-pinecone
```

### 2. Create and activate a virtual environment

```bash
python -m venv venv
source venv/bin/activate    # or venv\Scripts\activate on Windows
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Set environment variables

Create a `.env` file or set them manually:

```env
PINECONE_API_KEY=your-pinecone-api-key
HF_TOKEN=your-huggingface-access-token
```

---

## 📄 How It Works

1. Initializes a **Pinecone index** with dotproduct similarity and 384-dimensional vectors.
2. Loads dense embeddings using `sentence-transformers/all-MiniLM-L6-v2`.
3. Encodes a sample corpus with BM25 for sparse retrieval.
4. Combines dense + sparse representations for hybrid search.
5. Wraps it all with `PineconeHybridSearchRetriever` for use in LangChain.

---

## 🧠 Example Usage

```python
query = "Places I visited in 2024"
results = retriever.get_relevant_documents(query)

for doc in results:
    print(doc.page_content)
```

---

## 📦 Requirements

See [`requirements.txt`](./requirements.txt), but core libraries include:

- `pinecone>=6.0.2`
- `pinecone-text`
- `langchain`
- `langchain-huggingface`
- `sentence-transformers`
- `transformers`
- `torch`



---

## 📄 License

[Apache 2.0 License](LICENSE)
```