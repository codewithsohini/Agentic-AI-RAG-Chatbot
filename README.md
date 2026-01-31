# Agentic AI RAG Assistant 🤖🧠

A stateful RAG (Retrieval-Augmented Generation) application built to answer queries based on the **Agentic AI eBook**. This project demonstrates advanced orchestration using LangGraph and a strictly grounded retrieval pipeline.

## 🏗️ Technical Architecture
- **Orchestration:** **LangGraph** – Manages a stateful workflow between retrieval and generation nodes, ensuring the system is modular and "agent-ready."
- **Vector Database:** **ChromaDB** – A persistent local vector store containing pre-indexed embeddings of the eBook.
- **Embeddings:** **HuggingFace (`all-MiniLM-L6-v2`)** – Localized embeddings for efficient semantic search without external API costs.
- **LLM Reasoning:** **Gemini 2.5 Flash** – Utilized for high-speed synthesis and grounded response generation.
- **Interface:** **Streamlit** – A professional chat UI providing full transparency of the RAG process.

## 🚀 Key Features
- **Strict Grounding:** The assistant is restricted to answering only from the provided document.
- **Confidence Scoring:** Every response includes a confidence score (0.0 - 1.0) evaluating context relevance.
- **Source Transparency:** Users can expand a section to view the exact retrieved context chunks used for the answer.

## 🛠️ Setup & Local Execution
1. **Clone the repository.**
2. **Install dependencies:**
   ```bash
   pip install -r requirements.txt

## 🧪 Sample Queries
To test the chatbot's performance and grounding, you can use the following example queries:

1. **Architecture:** "What are the core building blocks of an Agentic AI system?"
2. **Comparison:** "What is the difference between proactiveness and reactiveness in AI agents?"
3. **Logic:** "How does the 'Reasoning' component influence an agent's decision-making?"
4. **Use Cases:** "How can Agentic AI be applied to optimize supply chain management?"
5. **Memory:** "What is the role of memory in enabling an agent to learn from interactions?"
6. **Constraint Test:** "What does the book say about the history of the internet?" *(This should return "I don't know" to prove strict grounding).*
