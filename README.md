# RAG Legal Documents Analysis

_Executive PG Program in Data Science - Course 5: Generative AI (DL Track)_  
_Module 6: RAG Assignment | DS 70 | IIIT Bangalore_

## 📋 Project Overview

This repository contains a comprehensive Retrieval-Augmented Generation (RAG) implementation for legal document analysis, developed as part of the Executive Post Graduate Program in Data Science at IIIT Bangalore. The project demonstrates advanced techniques in document processing, vector embeddings, and generative AI for legal text analysis.

## 🎯 Objectives

- **Data Loading & Analysis**: Process and analyze legal documents across multiple categories
- **Vector Database Creation**: Build efficient vector embeddings for document retrieval
- **RAG Chain Implementation**: Develop end-to-end RAG pipeline for legal Q&A
- **Performance Evaluation**: Assess system performance using industry-standard metrics

## 📊 Dataset Description

### Legal Document Categories

- **ContractNLI**: Non-disclosure agreements and contract documents (87 documents)
- **CUAD**: Contract Understanding Atticus Dataset (510 documents)
- **MAUD**: M&A Understanding Dataset (134 documents)
- **Privacy QA**: Privacy policy documents (7 documents)

### Dataset Statistics

- **Total Documents**: 698 legal documents
- **Total Chunks**: 70,483 processed chunks
- **Processing Success Rate**: 100%
- **Average Document Length**: 16,058 words
- **Vector Database Size**: 1.17 GB

## 🔧 Technical Architecture

### Technology Stack

- **Language**: Python 3.8+
- **Vector Database**: ChromaDB
- **Embeddings**: OpenAI Embeddings (text-embedding-ada-002)
- **LLM**: OpenAI GPT models
- **Framework**: LangChain
- **Data Processing**: Pandas, NumPy
- **Visualization**: Matplotlib, Seaborn

### Key Components

1. **Document Loader**: Multi-format legal document processing
2. **Text Chunking**: Recursive character-based splitting with overlap
3. **Vector Store**: ChromaDB with OpenAI embeddings
4. **RAG Chain**: Custom implementation with context retrieval
5. **Evaluation Framework**: RAGAS-based assessment metrics

## 📁 Project Structure

```
rag-legal-documents/
├── notebooks (zipped)/
│   └── RAG_Assg_Legal_NGUYEN VAN THUONG.zip
├── rag_legal/
│   ├── corpus/
│   │   ├── contractnli/
│   │   ├── cuad/
│   │   ├── maud/
│   │   └── privacy_qa/
│   └── benchmarks/
├── legal_vector_db (Google drive)/
└── README.md
```

## 🚀 Getting Started

### Prerequisites

```bash
pip install openai
pip install chromadb
pip install langchain
pip install pandas numpy matplotlib seaborn
pip install jupyter notebook
```

### Installation

1. Clone this repository

```bash
git clone [repository-url]
cd rag-legal-documents
```

2. Install dependencies

```bash
pip install -r requirements.txt
```

3. Set up environment variables

```bash
export OPENAI_API_KEY="your-openai-api-key"
```

### Vector Database Access

Pre-built vector database is available at:
📂 [Google Drive Vector Database](https://drive.google.com/drive/folders/1hD_BGQBUsDPrQzHbJygUew22I8CVkCCY?usp=sharing)

## 📈 Performance Metrics

### Vector Database Creation

- **Processing Time**: 87 minutes 13.4 seconds
- **Embedding Cost**: $1.409 USD
- **Success Rate**: 100% (0 failed batches)
- **Storage Efficiency**: ~1GB for 70K+ chunks

### Document Analysis Results

- **First 10 Documents Similarity**: 0.255 (high semantic coherence)
- **Random 10 Documents Similarity**: 0.146 (diverse content validation)
- **Chunk Distribution**: Balanced across all categories

## 🔍 Key Features

### 1. Document Loading & Analysis

- Multi-format document processing (TXT, PDF support)
- Comprehensive EDA with statistical analysis
- Document similarity analysis using cosine similarity
- Category-wise distribution analysis

### 2. Vector Database Implementation

- ChromaDB integration with persistent storage
- OpenAI embeddings for semantic representation
- Efficient batch processing with error handling
- Scalable architecture for large document collections

### 3. RAG Chain Development

- Context-aware document retrieval
- Prompt engineering for legal domain
- Response generation with source attribution
- Performance optimization techniques

### 4. Evaluation Framework

- RAGAS-based evaluation metrics
- Context relevance assessment
- Answer faithfulness validation
- Performance benchmarking

## 📊 Results & Insights

### Document Distribution Analysis

- **ContractNLI**: 12.46% (87 documents)
- **CUAD**: 73.07% (510 documents) - Dominant category
- **MAUD**: 19.20% (134 documents)
- **Privacy QA**: 1.00% (7 documents)

### Similarity Analysis Findings

- Sequential documents show higher similarity (0.255) indicating thematic clustering
- Random documents show lower similarity (0.146) confirming dataset diversity
- Optimal chunk size balances context preservation and retrieval efficiency

## 🎓 Academic Context

**Course Information:**

- **Program**: Executive PG Program in Data Science
- **Institution**: IIIT Bangalore
- **Course**: Course 5 - Generative AI (Deep Learning Track)
- **Module**: Module 6 - RAG Assignment
- **Cohort**: DS 70

**Learning Outcomes:**

- Advanced understanding of RAG architecture
- Practical experience with legal document processing
- Vector database design and optimization
- Evaluation methodologies for generative AI systems

## 📝 Usage Examples

### Basic RAG Query

```python
from enhanced_rag_chain_v2 import create_rag_chain

# Initialize RAG chain
rag_chain = create_rag_chain("legal_vector_db")

# Query the system
response = rag_chain.invoke({
    "question": "What are the key terms in a non-disclosure agreement?"
})
print(response["answer"])
```

### Custom Document Analysis

```python
# Load and analyze specific document category
legal_docs = load_legal_documents("contractnli")
similarity_matrix = calculate_document_similarity(legal_docs)
visualize_similarity_heatmap(similarity_matrix)
```

## 🔄 Future Enhancements

- [ ] Integration with additional legal document types
- [ ] Advanced prompt engineering techniques
- [ ] Multi-language support for international law
- [ ] Real-time document updates and incremental indexing
- [ ] Enhanced evaluation metrics for legal domain
- [ ] Web interface for interactive legal Q&A

## 📚 References

1. Lewis, P., et al. (2020). "Retrieval-Augmented Generation for Knowledge-Intensive NLP Tasks"
2. Karpukhin, V., et al. (2020). "Dense Passage Retrieval for Open-Domain Question Answering"
3. Hendrycks, D., et al. (2021). "CUAD: An Expert-Annotated NLP Dataset for Legal Contract Review"

## 📄 License

This project is developed for academic purposes as part of the IIIT Bangalore Executive PG Program in Data Science.

## 👨‍💼 Author

**Nguyen Van Thuong**  
Executive PG Program in Data Science, DS 70  
IIIT Bangalore

---

_This project demonstrates the application of advanced RAG techniques in the legal domain, showcasing expertise in generative AI, vector databases, and legal document analysis._
