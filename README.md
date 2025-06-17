# agentic-pharma-assistant
📘 Agentic Pharma Assistant
An interactive, autonomous agent designed to assist with pharmacology questions using:

✅ Retrieval-Augmented Generation (RAG) from Lippincott Illustrated Reviews: Pharmacology

🌐 Web search with DuckDuckGo

💬 Reasoning with  LLMs 

🧠 Validation loop before generating the final response

🔧 Features
Supervisor Node: Controls execution flow based on validation.

Router Node: Chooses between LLM, Web Search, and RAG based on query content.

RAG Node: Answers using textbook chunks indexed by ChromaDB.

LLM Node: Calls Groq's API for generic completions.

Web Node: Uses DuckDuckGo to fetch real-time web content.

Validator Node: Ensures output quality; re-routes if not confident.

🗃️ Project Structure
bash
Copy
Edit
.
├── agentic_pharma.ipynb        # Main notebook with workflow
├── data/
│   └── lippincott-illustrated-reviews-pharmacology_compress.pdf
├── chroma_db/                  # Vectorstore for PDF chunks (generated at runtime)
├── requirements.txt            # Python dependencies
└── README.md                   # This file
📦 Installation
Clone this repo:

bash
Copy
Edit
git clone git@github.com:yourusername/agentic-pharma.git
cd agentic-pharma
Create a Conda environment:

bash
Copy
Edit
conda create -n pharma-agent python=3.10
conda activate pharma-agent
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
🔑 API Keys Required
Set these as environment variables or load via .env:


(Optional) HUGGINGFACEHUB_API_TOKEN — for embedding models

(Optional) SERPER_API_KEY — if switching from DuckDuckGo to Google-based web search

🚀 How to Run
Launch the notebook:

bash
Copy
Edit
jupyter notebook agentic_pharma.ipynb
Run all cells to initialize the pipeline and start chatting with the agent.

✅ Use Cases
Pharmacology tutoring or self-assessment

Quick drug mechanism lookups

Literature-augmented clinical reasoning

Chatbot integration for FNP or RN students

📚 Sources
Lippincott Illustrated Reviews: Pharmacology (7th ed.)

Groq LLMs

DuckDuckGo Search

LangChain

