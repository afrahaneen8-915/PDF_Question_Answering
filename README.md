# PDF Question Answering System using LangChain

## Domain
AI in Education

## Project Overview
This project implements a PDF-based Question Answering System using LangChain, ChromaDB, Sentence Transformers, and Ollama.

The system extracts text from an educational PDF, divides it into smaller chunks, generates embeddings, and retrieves the top 5 relevant chunks for each question. It uses the Llama 3.2 model through Ollama to generate answers based on the retrieved information.

The project also compares answers generated with Retrieval-Augmented Generation (RAG) against answers generated without retrieval.

## Technologies Used
- Python 3.12
- LangChain
- ChromaDB
- Sentence Transformers
- Ollama
- Llama 3.2
- Pandas
- NumPy
- Jupyter Notebook

## Dataset
- Source: Artificial Intelligence and the Future of Teaching and Learning
- PDF pages processed: 15
- Total text chunks: 71
- Total questions: 15

## Project Workflow
1. Extract text from the PDF document.
2. Split the extracted text into smaller chunks.
3. Generate embeddings using Sentence Transformers.
4. Store embeddings in ChromaDB.
5. Retrieve the top 5 relevant chunks for each question.
6. Generate answers using Llama 3.2 through Ollama.
7. Generate answers without retrieval for comparison.
8. Export the results into CSV files.

## Project Structure
```text
PDF_Question_Answering/
│
├── dataset/
│   ├── sample.pdf
│   ├── queries.csv
│   ├── extracted_text.txt
│   ├── chunks.csv
│   └── answers.csv
│
├── notebook/
│   └── PDF_Question_Answering.ipynb
│
├── pdf_qa.py
├── requirements.txt
├── README.md
└── .gitignore
```

## Output Files
- `extracted_text.txt` – Extracted PDF content.
- `chunks.csv` – Text chunks created from the PDF.
- `answers.csv` – Questions, retrieved chunks, retrieval scores, and generated answers.

## How to Run
1. Install the required packages:
   `python -m pip install -r requirements.txt`
2. Make sure Ollama is installed and the Llama 3.2 model is available.
3. Run the program:
   `python pdf_qa.py`

## Conclusion
The project successfully demonstrates a PDF-based Question Answering System using Retrieval-Augmented Generation. It combines document processing, semantic search, vector storage, and local language model inference to answer questions from educational documents.