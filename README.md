# 📘 Similarity Search using ChromaDB

*A hands-on mini-project demonstrating vector storage, embedding generation, and similarity search with ChromaDB.*

---

## 🔍 Overview

This project implements a **text similarity search pipeline** using **ChromaDB**, a lightweight open-source vector database designed for AI and LLM applications.

You will learn how to:

* Create and manage a ChromaDB collection
* Store documents with metadata and unique IDs
* Generate embeddings using `SentenceTransformerEmbeddingFunction`
* Query the vector store using cosine similarity
* Retrieve top-k most similar documents

The main script in this project is:

```
similarity_search.py
```

---

## 🧠 Features

### ✔️ Create a ChromaDB collection

Defines an embedding function and initializes a persistent vector collection.

### ✔️ Add documents with auto-generated embeddings

Text inputs are embedded automatically using **all-MiniLM-L6-v2** from SentenceTransformers.

### ✔️ Perform similarity search

Given a query word or list of queries, the script retrieves the most semantically similar documents.

### ✔️ Supports multiple queries

The implementation handles both single and batch queries.

### ✔️ End-to-end working example

Shows the full workflow from setup → indexing → querying → output.

---

## 📂 Project Structure

```
.
├── similarity_search.py       # Main script: collection creation, embedding, querying
├── README.md                  # Project documentation
└── LICENSE                    # MIT License (or your chosen license)
```

---

## 🚀 How to Run This Project

### 1️⃣ Install dependencies

```bash
pip install chromadb==1.0.12
pip install sentence-transformers==4.1.0
```

### 2️⃣ Run the script

```bash
python3 similarity_search.py
```

### 3️⃣ Expected Output

The script prints:

* The created collection name
* Number of stored documents
* Query results (IDs, documents, similarity scores)

Example output:

```
Top 3 similar documents to "apple":
 - ID: food_1, Text: "fresh red apples", Score: 0.1234
 - ID: food_13, Text: "golden apple", Score: 0.2341
 - ID: food_14, Text: "red fruit", Score: 0.2892
```

---

## 🧪 Practice Extensions

You can extend this project by:

* Adding metadata filtering
* Using transformer models like `all-mpnet-base-v2`
* Storing larger datasets (articles, recipes, FAQ data, etc.)
* Integrating with a Retrieval-Augmented Generation (RAG) pipeline
* Switching from local Chroma to a client–server architecture

---

## 🛠️ Technologies Used

| Component                | Purpose                                  |
| ------------------------ | ---------------------------------------- |
| **Python 3.11**          | Main language                            |
| **ChromaDB**             | Vector storage and querying              |
| **SentenceTransformers** | Generating embeddings                    |
| **HNSW Indexing**        | Fast approximate nearest-neighbor search |

---

## 📜 Example Snippet

```python
results = collection.query(
    query_texts=["apple"],
    n_results=3
)

print(results["documents"])
print(results["ids"])
print(results["distances"])
```

---

## 🧑‍💻 Author

**Gautham N Vijayan**
Aspiring AI/ML Engineer • Data Scientist
Building portfolio-ready projects one step at a time 🚀

---

## 📄 License

This project is licensed under the MIT License — feel free to use it in your own projects.

