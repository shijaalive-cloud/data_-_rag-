# data_-_rag-
# Nigerian Food Composition Data Ingestion & RAG Pipeline

This repository contains the data preprocessing and document construction notebook (`data&rag.ipynb`) for the **Nigerian Dish Recognition & Nutrition Logging System**. It transforms tabular Nigerian food composition records into structured LangChain `Document` objects ready for embedding, vector indexing, and Retrieval-Augmented Generation (RAG).

## Overview

The pipeline reads nutritional records from the Nigerian Food Composition Table (`WCT_Nigeria.xlsx`), filters out incomplete or header rows, and formats each valid food item into a descriptive natural-language prose summary containing macronutrient and micronutrient profiles.

## Features

- **Excel Data Ingestion:** Loads and validates tabular food composition data using `pandas`.
- **Data Sanitization:** Automatically skips malformed or header rows missing valid `Code` or `Food Item description in English` entries.
- **Prose Synthesis for RAG:** Converts structured nutritional columns (energy, protein, fat, carbohydrates, fiber, calcium, etc.) into human-readable context strings optimized for semantic search and LLM retrieval.
- **LangChain Integration:** Wraps each formatted nutritional profile into `langchain_core.documents.Document` objects.

## Prerequisites

- Python 3.8+
- Google Colab or local Jupyter environment

### Required Libraries

```bash
pip install pandas openpyxl langchain-core
