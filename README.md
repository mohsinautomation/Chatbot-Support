# 🤖 AI Customer Support Chatbot

An AI-powered customer support chatbot built with **n8n, RAG, Google Gemini Embeddings, Groq LLM, WhatsApp, and Google Sheets**.

The system helps businesses automate customer support by answering questions from their own knowledge base, checking order information, creating orders, and handing conversations over to human agents when necessary.

---

## 🚀 Project Overview

Many businesses receive the same customer questions repeatedly, such as:

- Where is my order?
- What is your return policy?
- How long does delivery take?
- What products are available?
- Can I return this product?
- Can I place an order?

This project automates these support conversations using an **AI Agent + RAG architecture**.

The chatbot uses the company's own documents as its knowledge source instead of relying only on the LLM's general knowledge.

---

## 🏗️ Architecture

### Knowledge Base / RAG Pipeline

Customer
   ↓
WhatsApp Trigger
   ↓
AI Agent
   ↓
 ┌───────────────┬────────────────┬─────────────────┐
 ↓               ↓                ↓
FAQ Search    Product Catalog   Order Status
 ↓               ↓                ↓
Knowledge       Google Sheet    Google Sheet
Base
                  ↓
             Create Order
                  ↓
             Google Sheet

AI Agent
   ↓
Chat Logging
   ↓
WhatsApp Response

If needed
   ↓
Human Handoff
   ↓
Support Team
