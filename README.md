# Agent CFO — Performance Optimization & Design

## Overview

Agent CFO is an intelligent assistant designed for finance/operations Q&A using Retrieval-Augmented Generation (RAG) and agentic reasoning. The system is optimized for low-latency responses and valid citations, supporting financial analysis for a listed company.

## Features

- **RAG Pipeline:** Combines vector search (FAISS) and keyword search (BM25) for efficient retrieval.
- **Agentic Reasoning:** Supports calculator, table extraction, and multi-document comparison tools.
- **Optimizations:** Batched embeddings, caching, dynamic k, hybrid retrieval, parallel extraction.
- **Instrumentation:** Logs timings (T_ingest, T_retrieve, etc.), tokens, cache hits, and tool usage.
- **Safety:** Input/output validation, rate limiting, sensitive info masking.


## Setup

1. **API Key:**  
   Add your OpenAI API key to `.env`:

## Usage

- **Run the notebook:**  
  - Ingests documents, builds indexes, and runs standardized benchmark queries.
  - Compares baseline vs optimized pipeline (latency and accuracy).
  - Results and metrics are saved in `data/index/`.

## Benchmark Queries

1. Gross Margin Trend (or NIM if Bank)
2. Operating Expenses YoY for 3 Years
3. Operating Efficiency Ratio

## Results

- Latency and accuracy plots are generated for baseline and optimized agents.
- Metrics and citations are logged for each query.

## Optimizations Implemented

- Hybrid retrieval (FAISS + BM25)
- Dynamic k adjustment
- Batched embeddings
- Query and ratio caching
- Agentic plan-then-act flow
- Safety guardrails and rate limiting


