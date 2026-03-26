# 🏍️ MotoPartsBot

**Telegram E-Commerce Bot with AI Search & Warehouse Sync**

![Python](https://img.shields.io/badge/Python-3.11-3776AB?style=flat-square&logo=python&logoColor=white)
![aiogram 3](https://img.shields.io/badge/aiogram-3-2CA5E0?style=flat-square&logo=telegram&logoColor=white)
![FastAPI](https://img.shields.io/badge/FastAPI-Backend-009688?style=flat-square&logo=fastapi&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-DB-4169E1?style=flat-square&logo=postgresql&logoColor=white)
![OpenAI](https://img.shields.io/badge/OpenAI-GPT-412991?style=flat-square&logo=openai&logoColor=white)

> Full-cycle e-commerce Telegram bot for motorcycle parts. AI-powered natural language search, real-time warehouse sync with MoySklad API, and automated order processing.

---



## 🎨 Project Presentation

![Full Showcase](f_82769ba88f78128b.png)


## ✨ Key Features

### 🤖 AI-Powered Search (GPT)
Users search in natural language — "I need an oil filter for Yamaha MT-07" — and the bot understands intent, extracts product attributes, and returns relevant matches from the warehouse database.

### 📦 MoySklad API Integration
Real-time synchronization with the MoySklad (warehouse management system). Stock levels, prices, and product data are automatically pulled and cached via scheduled API polling.

### 🛒 Automated Order Flow
Complete purchase pipeline: product search → cart management → order confirmation → payment. Built with aiogram 3 FSM (Finite State Machine) for reliable conversation state tracking.

### ⚡ Redis Caching & FSM
Redis handles both conversation state (FSM) and data caching. Product catalogs are cached to minimize API calls to MoySklad, ensuring sub-second response times.

### 📊 Multi-Platform
Originally built for Telegram, the bot's architecture also supports Avito marketplace integration for cross-platform sales automation.

---

## 🏗️ Architecture

```
┌─────────────────────────────────────────────────┐
│            Telegram Bot (aiogram 3)              │
│  FSM States · Inline Keyboards · Cart Logic     │
├─────────────────────────────────────────────────┤
│              Backend (FastAPI)                    │
│  REST API · Webhook Handler · Order Processor   │
├─────────────────────────────────────────────────┤
│                 AI Layer                          │
│  OpenAI GPT · Intent Recognition                │
│  Natural Language → Product Query Parser        │
├─────────────────────────────────────────────────┤
│                Data Layer                         │
│  PostgreSQL · Redis (Cache + FSM)               │
│  MoySklad API Sync · Product Catalog            │
└─────────────────────────────────────────────────┘
```

---

## 🛠️ Tech Stack

| Layer | Technology |
|---|---|
| **Bot Framework** | aiogram 3 (Python) |
| **Backend** | FastAPI |
| **Database** | PostgreSQL |
| **Cache / FSM** | Redis |
| **AI** | OpenAI GPT (NL search) |
| **Warehouse** | MoySklad REST API |
| **Deployment** | Docker |

---

## 🔒 Source Code

> **Note:** This repository serves as a portfolio showcase. The full source code is closed/commercial, but the architecture and implementation details can be reviewed upon request during technical interviews.
---

## 📄 License

MIT © 2026 [gajsin](https://github.com/gajsin)
