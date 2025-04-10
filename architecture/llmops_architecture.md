# LLMOps Architecture (Cloud-Native)

## Stack Overview

- LangChain or LlamaIndex for RAG-based orchestration
- Vector DBs: FAISS (local), OpenSearch (managed), Pinecone (SaaS)
- AWS Step Functions or GCP Workflows for retraining pipelines
- Lambda / Cloud Functions for serverless inference APIs
- GitHub Actions for ML CI/CD + automated testing

## Flow Summary

1. Document uploaded to cloud storage (S3/GCS)
2. Triggers ingestion → retraining pipeline
3. Embeddings updated in vector DB
4. API endpoint refreshed with new chain
