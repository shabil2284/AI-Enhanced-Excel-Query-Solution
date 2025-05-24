# 🧠 Simplified LangChain-Style Chatbot with Ollama and ChromaDB

This is a minimal chatbot implementation using SentenceTransformer, ChromaDB, and Ollama for local language model interaction. It's designed to handle document-based Q&A with a fully customizable dataset and locally pulled LLM.

---

## 🚀 Description

This project demonstrates a chatbot that loads data (like Excel, PDF, etc.), stores them as embeddings in a ChromaDB vector store, and interacts via a locally hosted LLM (like `mistral:7b`) using `ollama`. You can extend or train it with your own data and use other Hugging Face-compatible models as needed.

---

## 🛠 Setup Instructions

### 1. 📦 Install Dependencies

Make sure you have Python and pip (or Conda) installed. Then run:

```bash
pip install -r requirements.txt
```

### 2. 🚀 Ollama Setup

Install [Ollama](https://ollama.com/) to run local models.

#### Mac (via Homebrew)
```bash
brew install ollama
brew services start ollama  # to start on boot
brew services stop ollama   # to stop
```

#### Linux
```bash
curl -fsSL https://ollama.com/install.sh | sh
ollama serve &  # to run in background
```

#### Windows (via WSL or native binary)
Follow instructions from: https://ollama.com/download

### 3. 📥 Pull Mistral 7B (or any other) Model

To use the model (e.g., mistral:7b):

```bash
ollama pull mistral
```

Or if you have downloaded the model manually from Hugging Face, move it to your `~/.ollama/models` folder and register it.

---

## 📂 Notebook Interface

This project uses `.ipynb` files (Jupyter Notebooks) for modularity and interactive exploration.

> ✅ Tip: Use VS Code, JupyterLab, or Google Colab for a better experience.

---

## 🤖 Model Training

I downloaded the `mistral 7B` model from Hugging Face and pulled it into my local project. I fine-tuned the model based on my custom dataset and needs.

You can do the same with your own dataset. Just prepare your `.csv`, `.xls`, or `.pdf` file, clean the data, embed it using `SentenceTransformer`, and train the model accordingly.

### 💡 Notes
- The GPU should be compatible with the model.
- You can use **any model** with Ollama that supports your hardware.
- Model is optimized to give precise answers based on the embedded data.

---

## 📄 Example Usage

Inside the chat interface (`chat_loop`), you can:
- Ask: `"What is the revenue of XYZ Company?"`
- Use commands:
  - `exit` to quit
  - `clear` to reset memory
  - `history` to see past queries
  - `help` for suggestions

---

## 🔒 License

MIT License

---

Made with ❤️ for developers and data explorers.