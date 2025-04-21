# Dscan AI Agent

Dscan is a powerful, flexible open source document processing library that converts various document formats into a unified format. It has advanced document understanding capabilities powered by state-of-the-art AI models for layout analysis and table structure recognition.

The whole system runs locally on standard computers and is designed to be extensible - developers can add new models or modify the pipeline for specific needs. It's particularly useful for tasks like enterprise document search, passage retrieval, and knowledge extraction. With its advanced chunking and processing capabilities, it's the perfect tool for providing GenAI applications with knowledge through RAG (Retrieval Augmented Generation) pipelines.

## Getting Started with the Example

### Prerequisites

1. Install the required packages:

```bash
pip install -r requirements.txt
```

2. Set up your environment variables by add OpenAI API key in a `.env` file:

```bash
OPENAI_API_KEY=your_api_key_here
```

### Running the Example

Execute the files in order to build and query the document database:

1. Extract document content: `python 1-extraction.py`
2. Create document chunks: `python 2-chunking.py`
3. Create embeddings and store in LanceDB: `python 3-embedding.py`
4. Test basic search functionality: `python 4-search.py`
5. Launch the Streamlit chat interface: `streamlit run 5-chat.py`

Then open your browser and navigate to `http://localhost:8501` to interact with the document Q&A interface.

## Document Processing

### Supported Input Formats

| Format | Description |
|--------|-------------|
| PDF | Native PDF documents with layout preservation |
| DOCX, XLSX, PPTX | Microsoft Office formats (2007+) |
| Markdown | Plain text with markup |
| HTML/XHTML | Web documents |
| Images | PNG, JPEG, TIFF, BMP |
| USPTO XML | Patent documents |
| PMC XML | PubMed Central articles |

Check out this [page](https://ds4sd.github.io/docling/supported_formats/) for an up to date list.

### Processing Pipeline

The standard pipeline includes:

1. Document parsing with format-specific backend
2. Layout analysis using AI models
3. Table structure recognition
4. Metadata extraction
5. Content organization and structuring
6. Export formatting

## Documentation

For full documentation, visit [documentation site](https://ds4sd.github.io/docling/).

For example notebooks and more detailed guides, check out [GitHub repository](https://github.com/DS4SD/docling).
