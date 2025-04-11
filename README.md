# 🤖 Customer Support Router Agentic RAG System

An intelligent customer support system built with **AI Agents** and **Retrieval-Augmented Generation (RAG)** that classifies, analyzes, and routes queries based on their category and sentiment, backed by a dynamic knowledge base.

---

## 🧠 Overview

This project demonstrates how to build a smart **Agentic RAG System** for routing customer queries using a hybrid of OpenAI’s GPT-4o, LangGraph, LangChain, and a Vector DB.

The system performs:
- Query categorization (e.g., Billing, Technical, General)
- Sentiment detection (Positive, Neutral, Negative)
- Intelligent routing to the correct resolution path
- RAG-based knowledge injection for response generation
- Escalation to humans if sentiment is negative

---

## 🔍 Features

### 🧾 1. Query Categorization & Sentiment Detection
- Uses GPT-4o to identify:
  - **Category** (Billing, Technical, General)
  - **Sentiment** (Positive, Neutral, Negative)

### 🔀 2. Intelligent Routing
Routes based on category & sentiment:
- 🔁 Billing → Automated Billing Response Generator
- 🛠️ Technical → Technical Response Generator
- 💬 General → General Response Generator
- 🚨 Negative Sentiment → Escalate to Human Agent

### 🔎 3. Knowledge Base Integration (RAG)
- Integrates with a **Vector Database** (e.g., ChromaDB)
- Retrieves relevant context to augment GPT responses

### ⛑️ 4. Escalation System
- Negative sentiment or complex cases trigger human takeover

---

## 🛠️ Tech Stack

- **OpenAI GPT-4o**
- **LangGraph**
- **LangChain** (`langchain`, `langchain-openai`, `langchain-community`, `langchain-chroma`)
- **ChromaDB**
- **Vector Search & RAG**
- **Python 3.10+**

---

## 📦 Installation

Install all required libraries:

```bash
pip install langchain==0.3.14
pip install langchain-openai==0.3.0
pip install langchain-community==0.3.14
pip install langgraph==0.2.64
pip install langchain-chroma==0.2.0
```

⚠️ **Note:** Dependency conflicts may occur. It is recommended to use a virtual environment.

---

## 🧩 System Architecture

```text
[User Query]
      ↓
[GPT-4o Agent]
      ↓
[Categorization & Sentiment Analysis]
      ↓
+----------------------------+
| Routing Based on Outcome  |
+----------------------------+
| Billing → Billing Agent   |
| Technical → Tech Agent    |
| General → General Agent   |
| Negative → Escalate Human |
+----------------------------+
      ↓
[Final Response via RAG + GPT]
```

---

## 🚀 Getting Started

1. Clone the repository
2. Install dependencies
3. Prepare your OpenAI API key and knowledge base (ChromaDB)
4. Run the main agent script to start handling queries

---

## 📚 Use Cases

- Automate Tier-1 Customer Support
- Reduce load on human agents
- Improve first-response resolution
- Provide empathetic handling of negative cases

---

## ✅ Example Workflow

```text
User: "I was charged twice on my credit card. Very disappointed."

→ GPT detects: Category = Billing | Sentiment = Negative  
→ Route: Escalation to Human  
→ Response: "We're sorry to hear that. Connecting you with a support agent now."
```

---

## 🤝 Contributing

Open to collaboration! Feel free to:
- Improve prompt strategies
- Add agents for new categories
- Optimize vector search

---

## 📜 License

This project is open-source and available under the [MIT License](LICENSE).

---

⭐ **Star this project** if you like it — it helps others discover it too!
```