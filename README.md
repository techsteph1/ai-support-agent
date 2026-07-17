# AI Support Agent

An AI-powered customer support agent that uses tool-calling to look up orders, answer policy questions, and handle refund requests — built to replace a first-line support rep.

## The Problem

Customers expect instant answers about their orders, but manually checking order status, answering repetitive policy questions, and processing refund requests takes up significant support team time.

## The Solution

This agent uses an AI model that decides which tool to call based on the customer's message — looking up real order data, answering from a knowledge base, or flagging a refund for human approval — instead of following a fixed conversation script.

## Features

- 🔍 Real-time order lookup by order number
- 🤖 AI decides which tool to use based on the question (true tool-calling, not a scripted flow)
- 📚 FAQ answers pulled from a knowledge base (RAG)
- 💰 Refund eligibility checks with human-approval gate for sensitive actions
- 💬 Built-in chat interface for easy testing/demo

## Tech Stack

| Layer | Tool |
|---|---|
| Automation | n8n |
| Database | Supabase (Postgres) |
| AI Model | OpenAI (via n8n AI Agent) |
| Knowledge Base | Supabase Vector Store |

## Architecture

Chat Message → AI Agent
Look Up Order (Supabase)
FAQ Tool (Vector Store)
Refund Tool (Supabase + human approval)
The AI Agent reads the customer's message and decides which tool (if any) it needs to call to answer accurately — no fixed script, no manual routing.

## Project Status

✅ Core system complete — order lookup, FAQ answers, and refund handling with human-approval gate all working end-to-end.

## Roadmap

- Order lookup tool
- FAQ tool (RAG)
- Refund tool with approval gate
- Full conversation testing
- Add architecture diagram
- Add demo screenshots/GIF

## Setup

Coming soon — full setup guide will be added as this project progresses.

## License

MIT
