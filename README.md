# Fully Local PDF Question Answering System

This application allows you to ask questions about your PDF documents and get relevant answers. It uses AI to understand your PDFs and provide accurate responses based on their content.

## 📋 Prerequisites

Before you start, you'll need to:
1. Have Python installed on your computer (version 3.8 or higher)
2. Have Ollama installed on your computer

### Installing Ollama

1. Visit [Ollama's website](https://ollama.ai/)
2. Download and install Ollama for your operating system (Windows/Mac/Linux)

## 🚀 Getting Started

### Step 1: Setup

1. Create a new folder called `knowledge_base` in the same directory as the program
2. Copy your PDF files into the `knowledge_base` folder
   - These are the documents the AI will use to answer your questions

### Step 2: Install Required Models

Open your terminal/command prompt and run these commands:

```bash
ollama pull nomic-embed-text
ollama pull gemma3:1b
```

This might take a few minutes depending on your internet connection.

### Step 3: Install Python Requirements

In your terminal/command prompt, navigate to the program directory and run:

```bash
pip install -r requirements.txt
```

### Step 4: Run the Program

1. Open the `rag.py` file in a text editor
2. Find this line near the bottom:
   ```python
   response = rag_system.query("What is the purpose of the MCP?")
   ```
3. Replace `"What is the purpose of the MCP?"` with your own question
4. Save the file
5. Run the program:
   ```bash
   python rag.py
   ```

## 📝 Example Questions

Here are some example questions you can ask (replace these with questions relevant to your PDFs):
- "What are the main points of chapter 1?"
- "Can you summarize the conclusion?"
- "What does the document say about X?"

## ⚠️ Important Notes

- The first time you run a query, it might take a few minutes as the system processes your PDFs
- Make sure your PDFs are readable (not scanned images)
- The quality of answers depends on chosen llm
- Keep your questions clear and specific

## 🔍 Troubleshooting

If you encounter issues:
1. Make sure Ollama is running
2. Check that your PDFs are in the `knowledge_base` folder
3. Ensure all installation steps were completed
4. Try restarting your computer if Ollama isn't responding

## 📁 Folder Structure

```
your_folder/
│
├── knowledge_base/     (Put your PDFs here)
│   └── your_pdf.pdf
│
├── rag.py             (Main program)
└── requirements.txt   (Required packages)
```

Need help? Feel free to reach out to the development team!
