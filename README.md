
---

# 🍕 Pizza Restaurant QA Bot — LangChain + Ollama + Chroma

This is an intelligent Question-Answering (QA) chatbot that answers user queries about a pizza restaurant by leveraging realistic customer reviews. It uses **LangChain**, **Ollama**, and **Chroma vector store** to retrieve relevant context and generate accurate, source-based responses using the **LLaMA 3.2** model.

---

## 🚀 Features

- ✅ Retrieve relevant reviews based on user queries.
- ✅ Answer questions contextually using retrieved reviews.
- ✅ Built with `LangChain`, `Ollama`, and `Chroma`.
- ✅ Embeddings powered by `mxbai-embed-large`.
- ✅ Local vector storage using Chroma DB.
- ✅ Easily extensible for other domains or datasets.

---

## 🧠 How It Works

1. **Embeddings**: Each restaurant review is embedded using the `mxbai-embed-large` model.
2. **Vector Store**: Reviews are stored in a persistent `Chroma` vector database.
3. **Retriever**: Given a user question, relevant review chunks are retrieved using similarity search.
4. **Prompt + LLM**: A custom prompt is filled with the question and retrieved reviews and passed to `LLaMA 3.2` via Ollama for response generation.


---

## 📦 Requirements

Install the dependencies:

```bash
pip install langchain langchain-core langchain-ollama langchain-chroma pandas
```

Also, make sure:
- [Ollama](https://ollama.com/) is installed and running
- The required models (`llama3.2` and `mxbai-embed-large`) are available

---

## 🛠️ Setup

1. Clone the repo:

```bash
git clone https://github.com/yourusername/pizza-qa-bot.git
cd pizza-qa-bot
```

2. Run the app:

```bash
python app.py
```

3. Ask questions like:

```
"Is the service good?"
"How’s the pizza crust?"
"Are the staff friendly?"
```

Type `q` to quit.

---

## 🧩 Customization

To use this for another domain (e.g., tech product reviews or hotel feedback):

- Replace `realistic_restaurant_reviews.csv` with your own dataset.
- Adjust the prompt template in `app.py`.
- Rebuild the vector store (delete `chroma_db/` if needed).

---

## 🧠 Example Prompt

```
You are an expert in answering questions about a pizza restaurant 
here are some relevant reviews: {reviews}
here is the question to answer: {question}
```

---

## 📌 License

MIT License — feel free to use, modify, and share!

---

## ❤️ Acknowledgements

- [LangChain](https://github.com/langchain-ai/langchain)
- [Ollama](https://ollama.com)
- [Chroma](https://www.trychroma.com/)
- [MXBAI](https://huggingface.co/mxbai)

---

