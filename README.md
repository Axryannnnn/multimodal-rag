# Multimodal RAG

A Python notebook that extracts text, tables, and images from a company report, uses Groq to summarize visuals, and stores Hugging Face embeddings in Pinecone for retrieval.

Open [multimodal_rag.ipynb](multimodal_rag.ipynb) in Google Colab or Jupyter. The sample [NovaCore report](NovaCore_Multimodal_Company_Report_2026.pdf) must be in the notebook's working directory; upload it to the Colab runtime if using Colab.

Run the installation cells before importing dependencies. Provide `GROQ_API_KEY` and `PINECONE_API_KEY` through the runtime's secure environment settings, or use the notebook's hidden input prompts. API keys and saved cell outputs have been removed from this copy. Rotate any keys previously embedded in the original notebook.

Review cells before running them: the namespace-clearing cell deletes all records in the `fy2026-demo` Pinecone namespace. Skip it if that namespace contains data you want to keep. Index creation and model calls require working API credentials and may incur provider charges.

Local validation passed for notebook imports and extraction from the supplied report: 9 text documents, 8 tables, and 7 unique images. Remote vision summaries, embedding generation, and Pinecone retrieval have not yet been verified in the cloud environment.
