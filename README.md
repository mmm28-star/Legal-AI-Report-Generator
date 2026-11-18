# Legal AI Report Generator

## Overview

This project is a smart legal document analyser that reads PDF files, extracts relevant information, and builds detailed legal reports. The system uses advanced NLP techniques, vector search, and LLM integration to provide accurate legal document analysis.

## Features

- **PDF Document Processing**: Extract text and metadata from legal documents
- **Intelligent Search**: Vector-based semantic search using FAISS
- **Legal Report Generation**: Automated generation of legal reports with proper formatting
- **Multi-Document Analysis**: Process multiple documents simultaneously
- **Citation Tracking**: Track sources and citations in generated reports
- **Professional Output**: Generate properly formatted legal documents

## Quick Start

### Prerequisites

- Python 3.8+
- PostgreSQL (for database setup)
- Required Python packages (see requirements.txt)

### Installation

1. **Clone the repository**
   ```bash
   git clone <repository-url>
   cd Legal-AI-Report-Generator
   ```

2. **Create virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up database**
   ```bash
   # Run the database setup script
   python setup_database.py
   ```

5. **Process documents**
   ```bash
   # Process sample documents
   python process_documents.py
   ```

6. **Generate report**
   ```bash
   # Generate legal report
   python generate_report.py
   ```

## Project Structure

```
Legal-AI-Report-Generator/
├── sample_docs/           # Sample legal documents
├── database_setup_pg.sql  # PostgreSQL setup
├── database_setup_sample.sql # Sample data
├── doc_id_map.pkl        # Document mapping
├── faiss_index.bin       # Vector search index
├── process_documents.py   # Document processing script
├── generate_report.py     # Report generation script
├── llm_integration.py    # LLM integration
├── requirements.txt       # Python dependencies
└── README.md            # This file
```

## Usage

### Document Processing

The system processes legal documents in the following format:
- **Police Reports**: Incident details, parties involved, location, date/time
- **Medical Records**: Treatment details, expenses, provider information
- **Insurance Correspondence**: Policy details, claim information
- **Other Legal Documents**: Various legal documents with structured data

### Report Generation

The system generates comprehensive legal reports including:
- **Statement of Facts**: Chronological account of events
- **Medical Records Analysis**: Injury details and treatment summary
- **Legal Analysis**: Professional legal assessment
- **Citations**: Proper source attribution

### Search Functionality

- **Semantic Search**: Find relevant documents using natural language queries
- **Vector Search**: Fast similarity-based document retrieval
- **Citation Tracking**: Maintain proper source attribution

## Configuration

### Database Configuration

The system uses PostgreSQL for data storage. Configure your database connection in the setup scripts.

### LLM Configuration

The system integrates with language models for enhanced text generation. Configure the LLM settings in `llm_integration.py`.

## API Endpoints

The system provides the following main functions:

- `process_documents()`: Process and index legal documents
- `search_documents(query)`: Search for relevant documents
- `generate_legal_report(case_id)`: Generate comprehensive legal report
- `extract_case_data(documents)`: Extract structured data from documents

## Performance

- **Document Processing**: ~2-3 seconds per document
- **Search Response**: <1 second for semantic search
- **Report Generation**: ~5-10 seconds for comprehensive reports
- **Memory Usage**: Optimized for large document collections

## Troubleshooting

### Common Issues

1. **Database Connection Error**
   - Ensure PostgreSQL is running
   - Check database credentials in setup scripts

2. **Memory Issues**
   - Reduce batch size in document processing
   - Use smaller FAISS index for large document collections

3. **LLM Integration Issues**
   - Check model availability and memory requirements
   - Verify API credentials if using external LLM services
