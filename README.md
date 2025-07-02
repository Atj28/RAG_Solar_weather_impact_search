🔍 RAG-Based Semantic Search on Solar Power Generation Data 🌞
This project demonstrates how to build a semantic search application using the Retrieval-Augmented Generation (RAG) approach to explore solar power generation datasets.

Rather than manually analyzing CSVs, users can ask natural language questions and receive contextual, accurate responses based on embedded tabular data.

📌 Project Overview
🔎 Data Source: Solar Power Generation Data from Kaggle

🧠 LLM: OpenAI gpt-3.5-turbo

📈 Embeddings: all-MiniLM-L6-v2 (SentenceTransformers)

⚡ Semantic Search: FAISS

📄 Input Data: CSV files for:

Plant 1 & 2 Generation Data

Plant 1 & 2 Weather Sensor Data

🧰 Features
✅ Convert tabular rows to human-readable summaries
✅ Embed those summaries into a vector space
✅ Perform top-k semantic search using FAISS
✅ Use GPT to generate a final answer from retrieved chunks
✅ Process generation and weather data separately due to different time intervals

🔄 RAG Pipeline Steps
Load CSVs
Load plant generation and weather CSV files separately.

Summarize Rows
Convert each row into a natural language chunk (e.g., "At 12:30, Plant X generated 1200W AC...").

Embed Summaries
Use SentenceTransformers (MiniLM) to create vector embeddings for each summary.

Index with FAISS
Store all embeddings in a FAISS index for fast similarity search.

Search + Retrieval
Encode the user's query and search for top-k similar chunks.

Answer with GPT
Pass the retrieved chunks as context to GPT and generate a natural language response.

💡 Sample Questions
How does temperature affect energy output?

Why does DC power output fluctuate throughout the day?

What time of day consistently gives the maximum AC power?

How does performance vary between Plant 1 and Plant 2?
