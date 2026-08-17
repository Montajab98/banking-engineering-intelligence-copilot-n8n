# Banking Engineering Intelligence Copilot

An Agentic RAG prototype designed to explore relationships across banking software engineering artifacts including business requirements, API specifications, regression test cases, known defects, and production incidents.

> This repository represents the V1 n8n architecture prototype.  
> The production-oriented V2 is being implemented using Python and FastAPI.

---

## Project Overview

Modern banking engineering teams work across multiple disconnected sources:

- Business Requirements Documents
- OpenAPI / Swagger specifications
- Regression test suites
- Known defect registers
- Production incident logs

This prototype creates a unified AI-assisted knowledge layer across these sources using Retrieval-Augmented Generation (RAG).

The system allows an AI agent to retrieve relevant engineering context and answer questions grounded in the indexed banking documents.

---

## Architecture

![Workflow Architecture](screenshots/workflow-architecture.png)

### Ingestion Pipeline

```text
Source Documents
      ↓
File Type Routing
      ↓
PDF / CSV / XLSX / TXT / JSON Extraction
      ↓
Metadata Enrichment
      ↓
Document Merge
      ↓
Text Chunking
      ↓
Embeddings
      ↓
Qdrant Vector Database
