# Auto Forms ⚡️
**Intelligent Load Testing & Automated Payload Injection Engine**

![Version](https://img.shields.io/badge/version-1.0.0-blue.svg)
![Architecture](https://img.shields.io/badge/architecture-Decoupled_SPA-success.svg)
![Status](https://img.shields.io/badge/status-Active-brightgreen.svg)

## 📖 About
**Auto Forms** is a high-performance, intelligent data-injection tool engineered to automate and scale Google Form submissions. Designed with a premium, minimalist glassmorphism interface, it allows users to dynamically map form fields to static text, random arrays, JSON datasets, or dynamically generated AI text. 

Under the hood, Auto Forms utilizes a decoupled full-stack architecture with built-in asynchronous worker queues, exponential backoff, and AI rate-limit handling, ensuring robust, uninterrupted execution even under heavy load.

## ✨ Core Features
* **Intelligent DOM Scraping:** Automatically analyzes target endpoints to extract hidden input IDs and entry requirements.
* **Multi-Provider AI Generation:** Integrates LLM APIs (including Google Gemini and Pollinations) to generate context-aware, unique responses per iteration based on global and specific rule sets.
* **High-Speed JSON Injection:** Bypasses AI for maximum throughput, allowing users to map bulk datasets directly to target fields for rapid load testing.
* **Resilient Execution Engine:** Features built-in micro-throttling and exponential backoff to gracefully handle HTTP 429 (Too Many Requests) and API rate limits.
* **Live Console Telemetry:** A custom-built, auto-scrolling terminal UI provides real-time play-by-play logging of worker nodes, API statuses, and payload dispatches.

## 🏗️ Architecture & Logic Overview
To maintain security and proprietary logic, the source code for this engine remains private. However, the system is built on modern, scalable engineering principles:

* **Frontend (The Client Node):** Built entirely in highly optimized Vanilla HTML/CSS/JS. It operates as a Single Page Application (SPA), ensuring lightning-fast load times and zero dependency bloat. The UI features responsive glassmorphism design and custom toast notifications for seamless UX.
* **Backend (The Worker Node):** Powered by a lightweight Python/Flask server. It utilizes background threading to manage long-running execution queues without timing out client requests. 
* **The Injection Logic:** 1.  **Extraction:** Safely parses the target's public DOM to construct a required payload map.
    2.  **Assembly:** Iterates through user-defined rules (AI prompts, random lists, or JSON arrays) to build a unique HTTP POST payload.
    3.  **Dispatch & Retry:** Routes payloads through a secure worker thread. If the target server or AI provider throttles the connection, the engine dynamically calculates a cooldown period and retries the dispatch, ensuring zero data loss during bulk operations.
neered by **unskyit***
