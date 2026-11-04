# AI Engineer Learning Path

From backend developer to AI engineer: about 8-10 months, 8-10 hours a week.

## Overview

AI engineering is mostly strong software engineering plus a new set of tools, so 2 years of backend experience is a real head start. This path ends with a production-grade capstone to show in interviews.

- **Goal:** build and ship products on top of LLMs and ML models
- **Timeline:** about 34 weeks across four phases
- **Your edge:** APIs, databases, queues, deployment and monitoring, which matter most in Phase 4

## Phase 1: Foundations (Weeks 1-6)

Get fluent in the Python data stack, learn only the math you need, and understand classic machine learning.

- **Python for AI:** NumPy, Pandas, async Python and Pydantic. Learn FastAPI too, since it is the standard for serving AI backends.
- **Math, only what you need:** linear algebra (vectors, matrices, dot product), basic probability and statistics, and the intuition for gradient descent. 3Blue1Brown's "Essence of Linear Algebra" and neural network series are enough.
- **ML basics:** Andrew Ng's Machine Learning Specialization or fast.ai Part 1. Cover supervised vs unsupervised learning, overfitting, train/test splits, and metrics (precision, recall, F1). Practice with scikit-learn.

## Phase 2: Deep Learning and Transformers (Weeks 7-12)

The goal is to understand what happens under the hood so you can debug and make good decisions, not to become a researcher.

- Neural networks, backpropagation, and PyTorch (build a small network from scratch)
- Andrej Karpathy's "Neural Networks: Zero to Hero" series, including building GPT from scratch
- How transformers work: attention, tokenization, embeddings, pretraining vs fine-tuning
- Hugging Face basics: loading models, tokenizers, and the transformers library

## Phase 3: Core LLM Engineering (Weeks 13-24)

This is where most AI engineer jobs actually live.

- **Prompting and structured outputs:** system prompts, few-shot examples, JSON/schema-constrained outputs, tool/function calling.
- **RAG (Retrieval-Augmented Generation):** chunking strategies, embeddings, vector databases (pgvector, Qdrant, Pinecone), hybrid search (BM25 + vectors), reranking.
- **Agents:** tool-use loops, planning, memory, multi-step workflows, and MCP (Model Context Protocol) for connecting tools.
- **Evaluation:** eval datasets, LLM-as-judge, regression tests for prompts. This is what separates juniors from seniors.
- **Fine-tuning:** LoRA/QLoRA with PEFT. Know when to fine-tune vs when RAG or prompting is enough.
- **Frameworks:** try LangChain/LangGraph or LlamaIndex, but also build with the raw provider SDKs so you understand what the frameworks hide.

## Phase 4: Production and MLOps (Weeks 25-34)

This is where your backend experience gives you an edge.

- **Serving:** FastAPI, streaming responses, queues, caching, rate limiting
- **Inference:** vLLM or Ollama for open-source models, plus cost and latency optimization
- **Observability:** tracing and monitoring (Langfuse, LangSmith or OpenTelemetry) and token cost tracking
- **Infrastructure:** Docker, Kubernetes basics, CI/CD, and a cloud (AWS, GCP or Azure) with its managed AI services
- **Safety:** prompt injection, guardrails, PII handling, and access control in RAG systems

## Where to Learn

Most of this is free or cheap. Pick one primary resource per phase rather than collecting everything, and check that each course is still available before you commit.

### Phase 1: Foundations

- **Python and FastAPI:** the official FastAPI tutorial and the Pydantic docs. Practice NumPy and Pandas with Kaggle's free Learn micro-courses.
- **Math:** 3Blue1Brown on YouTube ("Essence of Linear Algebra" and the neural networks series). Khan Academy for probability and statistics gaps.
- **ML basics:** Andrew Ng's Machine Learning Specialization on Coursera (can be audited free) or fast.ai's Practical Deep Learning for Coders. Use the scikit-learn user guide for hands-on practice.

### Phase 2: Deep Learning and Transformers

- Andrej Karpathy's "Neural Networks: Zero to Hero" on YouTube. The single best resource here, ending with GPT built from scratch.
- **PyTorch:** the official tutorials at pytorch.org.
- **Hugging Face:** the free LLM Course and the Transformers docs.
- Optional: Jay Alammar's "The Illustrated Transformer" for intuition.

### Phase 3: LLM Engineering

- **Prompting, tool use and agents:** the Anthropic docs and prompt engineering guide, plus the OpenAI and Google provider docs. Reading several shows what is common across them.
- **Short courses:** DeepLearning.AI's free hour-long courses on RAG, agents, function calling, evals and LangGraph.
- **RAG:** the LlamaIndex and LangChain docs, plus the pgvector and Qdrant docs for the vector database side.
- **Agents and MCP:** modelcontextprotocol.io and the LangGraph docs.
- **Evaluation:** Hamel Husain's writing on LLM evals, and the Langfuse and Braintrust docs.
- **Fine-tuning:** the Hugging Face PEFT and TRL docs, and Unsloth's tutorials for running QLoRA cheaply on a free Colab GPU.

### Phase 4: Production and MLOps

- **Docker and Kubernetes:** the official docs and TechWorld with Nana on YouTube.
- **Serving models:** the vLLM and Ollama docs.
- **Observability:** Langfuse (open source, easy to self-host) and the OpenTelemetry docs.
- **Cloud:** AWS, GCP or Azure free tiers and their AI services (Bedrock, Vertex AI, Azure AI). Pick the one your target employers use.

### Communities and Staying Current

- **Papers and news:** Hugging Face Daily Papers, and newsletters such as The Batch (DeepLearning.AI) and Latent Space.
- **Communities:** the Hugging Face Discord, r/LocalLLaMA and the fast.ai forums.
- **Practice:** Kaggle competitions and hackathons for building under a deadline.

### How to Use These

- Pick one primary resource per phase: Ng or fast.ai, then Karpathy, then DeepLearning.AI short courses, then the docs.
- Build while learning. After each phase, do the matching project before moving on.
- Prefer docs over video courses once you pass Phase 2. The tools change fast and docs stay current.

## Projects (in Order of Difficulty)

Seven projects take you from a first RAG pipeline to a deployed multi-agent app.

| # | Project | What you learn |
|---|---------|----------------|
| 1 | Chat with your documents: upload PDFs, ask questions, get cited answers (FastAPI + pgvector) | Core RAG pipeline |
| 2 | Structured data extractor: turn invoices, resumes or emails into validated JSON | Prompting, Pydantic, schema outputs |
| 3 | Eval harness for Project 1: 50+ test questions, automated scoring, a dashboard of quality across changes | Evaluation, the most valuable skill |
| 4 | SQL/analytics agent: natural-language questions answered by querying a real database, with safety limits | Tool use, agents, security |
| 5 | Build GPT from scratch: a tiny transformer trained on a small dataset (following Karpathy) | Deep understanding |
| 6 | Fine-tune a small open model (a 1-8B model with QLoRA) for a narrow task and compare it against prompting | Fine-tuning tradeoffs |
| 7 | Capstone: a production multi-agent app (customer-support or code-review assistant) with auth, streaming UI, tracing, cost dashboards, evals in CI and cloud deployment | Everything end to end |

> **Tip:** build the capstone around a problem from your current job's domain. It makes a much stronger portfolio piece and interview story than a generic chatbot.

## Make Yourself Hireable

Proof of real work counts more than certificates.

- Put every project on GitHub with a clear README: architecture diagram, eval results, cost and latency numbers, lessons learned.
- Write 2-3 short blog posts on what you learned. "How I improved RAG accuracy from 62% to 81%" beats "I built a chatbot".
- Bring AI into your current job, even as a small internal tool. Real production experience counts most.
- Optionally, contribute to open-source AI tools (LangChain, LlamaIndex, vLLM) or join Kaggle and Hugging Face community events.

## Suggested Weekly Rhythm

- 2-3 sessions of structured learning (courses and reading)
- 1-2 sessions of building, always with a project in progress
- 1 session to read one paper or technical blog and keep up with new releases, since the field moves fast
