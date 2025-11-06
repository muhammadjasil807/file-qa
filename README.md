File-QA: Document Question Answering System

This project allows users to ask questions and get answers from documents such as PDFs, DOCX, and TXT files.
It leverages embeddings, vector stores, and large language models to retrieve relevant chunks and generate answers.

Overview
The system works as follows:

1. Users upload a document (PDF, DOCX, or TXT).
2. The document is split into smaller chunks for better processing.
3. Each chunk is converted into embeddings using sentence-transformers.
4. Chunks are stored in a FAISS vectorstore for fast similarity search.
5. A HuggingFace LLM (Flan-T5) generates answers based on retrieved chunks.
6. Users can query the document interactively.

Features
- Supports multiple document types: PDF, DOCX, TXT
- Splits documents into chunks with overlap for context
- Embeddings using Sentence Transformers
- Fast semantic search with FAISS
- Question-answering powered by HuggingFace Flan-T5
- Interactive CLI for querying documents

Tech Stack
Programming Language: Python 3
Libraries: langchain, langchain-community, faiss-cpu, pypdf, python-docx, sentence-transformers, transformers
Model: google/flan-t5-base (text2text-generation)
Vector Store: FAISS

Project Structure
file-qa
│
├── file_qa_notebook.ipynb      (Colab notebook with full code)
├── requirements.txt            (Dependencies)
├── README.md                   (Project documentation)
└── example_docs/               (Optional folder for sample PDFs, DOCX, or TXT)

Installation and Running
Step 1 — Clone the Repository
git clone https://github.com/YOUR-USERNAME/file-qa.git
cd file-qa

Step 2 — Install Dependencies
pip install -r requirements.txt

Step 3 — Run the Notebook
Upload your document and run all cells.
Ask questions interactively or get a summary of the document.

Example Usage
- Upload: report.pdf
- Query: "Give me a short summary of the document"
- Output: "The document covers X, Y, and Z..."

Future Improvements
- Integrate with Streamlit for a web interface
- Use larger LLMs for more detailed answers
- Add support for multi-document QA
- Cache embeddings for faster repeated queries


Conclusion
File-QA demonstrates the power of combining embeddings, vector databases, and LLMs
to make documents interactive and searchable.
It’s a strong portfolio example for NLP, LangChain, and modern AI applications.

