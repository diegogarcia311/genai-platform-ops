# LLMOps Architecture (Cloud-Native)

## Stack Overview

- LangChain or LlamaIndex for RAG-based orchestration
- Vector DBs: FAISS (local), OpenSearch (managed), Pinecone (SaaS)
- AWS Step Functions or GCP Workflows for retraining pipelines
- Lambda/Cloud Functions for serverless inference APIs
- GitHub Actions for ML CI/CD + testing

## System Flow

1. Document uploaded to cloud storage (S3 or GCS)
2. Triggered ingestion → retraining pipeline
3. Vector DB is refreshed with updated embeddings
4. LLM chain updated and deployed to endpoint
