# Prerequisites

- Python 3.8 or higher (recommended)
- [Anaconda](https://www.anaconda.com/products/distribution) or [Miniconda](https://docs.conda.io/en/latest/miniconda.html) (optional, for easy environment management)
- JupyterLab or Jupyter Notebook
- Git (for cloning the repository)

## Environment Setup

You can use Anaconda/Miniconda to create and manage your Python environment:

```bash
conda create -n langchain-env python=3.10
conda activate langchain-env
```
Or use Python's built-in venv:
```bash
python -m venv venv
source venv/bin/activate
```
Then install dependencies:
```bash
pip install -r requirements.txt
```

# LangChain Project

This project demonstrates how to use LangChain and related tools for document loading, text splitting, embeddings, vector search, and retrieval-augmented generation (RAG) workflows. It includes examples using OpenAI, Ollama, Hugging Face, Faiss, and Chroma.

## Structure
- `speech.txt` — Sample text file for document loaders.
- `.env` — Store API keys (e.g., `OPENAI_API_KEY`, `HUGGING_FACEHUB_API_KEY`).
- `requirements.txt` — Python dependencies for the project.
- `*.ipynb` — Jupyter notebooks for each workflow:
  - `DataIngestion.ipynb` — Document loading (PDF, text, web, arXiv, Wikipedia).
  - `TextSplitter.ipynb` — Text splitting techniques.
  - `embedding.ipynb` — Embedding with OpenAI and Ollama.
  - `OllamaEmbedding.ipynb` — Embedding with Ollama models.
  - `HuggingFaceEmbedding.ipynb` — Embedding with Hugging Face models.
  - `Faiss.ipynb` — Vector search with Faiss.
  - `Chroma.ipynb` — Vector search and persistence with Chroma.
  - `RecursiveJsonSplitter.ipynb` — Splitting large JSON files.
  - `HTMLTextSpliter.ipynb` — Splitting HTML documents.

## Setup
1. Clone the repository or copy the project files.
2. Create and activate a Python virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate
   ```
3. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
4. Add your API keys to `.env`:
   ```
   OPENAI_API_KEY=your_openai_key
   HUGGING_FACEHUB_API_KEY=your_hf_key
   ```
5. Start JupyterLab or Jupyter Notebook:
   ```bash
   jupyter lab
   ```

## Usage
- Open the notebooks and run cells to see examples of document loading, text splitting, embedding, and vector search.
- Modify parameters (e.g., chunk size, model name) to experiment with different workflows.

## Notes
- For Ollama and Hugging Face embeddings, ensure the required models are downloaded and API keys are set.
- For Faiss, use `faiss-cpu` on macOS or unsupported Python versions.
- For Chroma, vector databases can be persisted to disk for reuse.

## References
- [LangChain Documentation](https://python.langchain.com/)
- [Ollama](https://ollama.com/)
- [Hugging Face](https://huggingface.co/)
- [Faiss](https://github.com/facebookresearch/faiss)
- [Chroma](https://docs.trychroma.com/)

## License
MIT
