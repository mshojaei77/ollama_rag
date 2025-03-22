# Fully Local PDF Question Answering System

This application allows you to ask questions about your PDF documents and get relevant answers. It uses AI to understand your PDFs and provide accurate responses based on their content.

## 🚀 Quick Start

Clone the repository:
```bash
git clone https://github.com/mshojaei77/ollama_rag.git
cd ollama_rag
```

The cloned repository includes a sample PDF and embedding cache about MCP for testing.

## 📋 Prerequisites

Before you start, you'll need to:
1. Have Python installed on your computer (version 3.8 or higher)
2. Have Ollama installed on your computer

### Installing Ollama

1. Visit [Ollama's website](https://ollama.ai/)
2. Download and install Ollama for your operating system (Windows/Mac/Linux)

## 🛠️ Setup & Installation

### Step 1: Install Required Models

Open your terminal/command prompt and run:

```bash
ollama pull nomic-embed-text
ollama pull gemma3:1b
```

### Step 2: Install Python Requirements

In your terminal/command prompt, run:

```bash
pip install -r requirements.txt
```

### Step 3: Prepare Your Documents
- Place your PDF files in the `knowledge_base` folder
- The repository includes a sample PDF about MCP for testing

### Step 4: Run the Program

1. Open `rag.py` in a text editor
2. Modify this line near the bottom:
   ```python
   response = rag_system.query("What is the purpose of the MCP?")
   ```
3. Replace with your question
4. Run the program:
   ```bash
   python rag.py
   ```

## 📝 Example Questions

Try these questions with the sample MCP document:
- "What is the purpose of the MCP?"
- "What are the main components of MCP?"
- "How does MCP handle process scheduling?"

Or use your own questions for your PDFs:
- "What are the main points of chapter 1?"
- "Can you summarize the conclusion?"
- "What does the document say about X?"

## ⚙️ System Configuration

The system uses these default settings (configurable in `RAGConfig`):
- Embedding Model: nomic-embed-text
- LLM Model: gemma3:1b
- Chunk Size: 1000
- Chunk Overlap: 50
- Top K Results: 2
- Batch Size: 10

## 📁 Project Structure

```
ollama_rag/
│
├── knowledge_base/     (PDF documents)
│   └── mcp.pdf        (Sample PDF)
│
├── embeddings/        (Cached embeddings)
├── rag.py            (Main program)
└── requirements.txt   (Required packages)
```

## ⚠️ Important Notes

- First-time queries may take longer due to PDF processing
- PDFs must be text-based (not scanned images)
- Answer quality depends on the chosen LLM
- Keep questions clear and specific

## 🔍 Troubleshooting

If you encounter issues:
1. Ensure Ollama is running
2. Verify PDFs are in the `knowledge_base` folder
3. Check all installation steps are complete
4. Try restarting your computer if Ollama isn't responding

## 🤝 Contributing

Feel free to:
- Open issues
- Submit pull requests
- Fork the repository
- Star the project if you find it useful
