# RAG Project

This project implements a Retrieval-Augmented Generation (RAG) pipeline for domain-specific knowledge retrieval and question answering. The workspace is organized to support multiple knowledge domains, each with its own vector database for efficient semantic search.

## Project Structure

- `rag_pipeline.ipynb` — Main Jupyter notebook for running and experimenting with the RAG pipeline.
- `books/` — Directory for storing source documents (books, guides, etc.) to be ingested into the vector databases.
- `db_books/` — Contains vector databases for each knowledge domain:
  - `chess_guide/`
  - `cricket_guide/`
  - `medical_basics/`
  - `stock_market_basics/`
  Each subfolder contains a `chroma.sqlite3` file and associated data for the domain.
- `.gitignore` — Specifies files and folders to be ignored by git.

## How It Works

1. **Document Ingestion:**
   - Source documents are placed in the `books/` directory.
   - Each domain (e.g., chess, cricket, medical, stock market) has its own vector database under `db_books/`.

2. **Vector Database:**
   - Uses ChromaDB (SQLite-based) for storing and retrieving document embeddings.
   - Each domain's database is isolated for efficient and relevant retrieval.

3. **RAG Pipeline:**
   - The pipeline in `rag_pipeline.ipynb` demonstrates how to query the vector databases and generate answers using retrieved context.

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/Ranjitpython1991/RAG_project.git
   ```
2. Install required Python packages (see notebook for details).
3. Run `rag_pipeline.ipynb` in Jupyter Notebook or JupyterLab.

## Customization
- Add new knowledge domains by creating a new folder under `db_books/` and placing a ChromaDB database inside.
- Add new documents to `books/` and update the ingestion process as needed.

## License
Specify your license here (e.g., MIT, Apache 2.0, etc.).

## Author
Ranjitpython1991
