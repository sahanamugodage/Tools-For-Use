# 🛠️ Tools-For-Use

> **A curated collection of standalone, zero-setup, high-utility developer tools and browser-based workspaces — designed for human developers and optimized for AI-assisted workflows.**

[![Status](https://img.shields.io/badge/Status-Active%20Development-10B981?style=for-the-badge)](#)
[![Zero Setup](https://img.shields.io/badge/Setup-Zero%20Dependencies-007acc?style=for-the-badge)](#)
[![AI Ready](https://img.shields.io/badge/AI-Ready%20%26%20Optimized-8B5CF6?style=for-the-badge)](#)
[![License](https://img.shields.io/badge/License-MIT-blue?style=for-the-badge)](#)

---

## 📖 Overview

**`Tools-For-Use`** is an open-source hub of lightweight, self-contained, browser-executable utilities built to eliminate daily developer friction. Each tool is designed to run directly in modern web browsers without heavy runtime dependencies, complex build steps, or backend servers (`node_modules`-free).

Whether you are debugging REST APIs, sanitizing escaped JSON payloads, inspecting data trees, or generating test requests, these tools provide an instant, reliable, and privacy-respecting environment right on your local machine.

---

## 🤖 Why This Repo is Built for AI & LLM Workflows

Modern software engineering frequently involves AI coding assistants (such as **Google Antigravity, Gemini, Claude, ChatGPT, Cursor, and Copilot**). This repository is deliberately architected with AI-assisted development in mind:

### 1. 🧠 Instant Sanitization of LLM Outputs
* LLM responses frequently include **stringified JSON blobs**, escaped quotes (`{\"key\": \"value\"}`), or **Python literals** (`True`, `False`, `None`) instead of valid JSON.
* Tools like **JsonXplorer** feature recursive deep-parsing, intelligent error analyzers, and 1-click syntax auto-repair to clean, unescape, and format AI-generated payloads in milliseconds.

### 2. ⚡ Zero-Friction Execution for Autonomous Agents
* Every tool is a standalone, client-side application.
* AI agents can inspect, launch, or recommend tools directly to users without having to configure servers, install packages, or resolve dependency conflicts.

### 3. 🧩 Predictable, Modular Architecture for AI Generation
* Each tool follows a self-contained, modular blueprint: `<Tool-Category>/<ToolName>.html` with dedicated `<Tool-Category>/img/` assets.
* AI agents can easily understand existing implementations and generate brand-new, production-ready utilities following the exact same conventions.

### 4. 📋 Prompt / Context Template for AI Assistants
When collaborating with an AI coding assistant, you can share this context snippet to immediately orient the AI:

```markdown
I am working on the "Tools-For-Use" repository. It is a collection of standalone,
zero-dependency developer web tools (single-file HTML/CSS/JS with modern UI).
When suggesting new tools or refactoring existing ones:
1. Keep each tool self-contained and runnable by simply opening the HTML file in a browser.
2. Use modern dark aesthetics (JetBrains Mono, Monaco Editor, Lucide icons, glassmorphism).
3. Place screenshots in the respective `<category>/img/` directory.
4. Support AI/developer edge cases (e.g., auto-repairing syntax, unescaping nested strings, copying JSON paths).
```

---

## 📂 Repository Structure

The repository is organized by category, ensuring that newly uploaded utilities have a clear, isolated home:

```text
Tools-For-Use/
├── Req handler/                       # API Request & Payload Handling Tools
│   ├── JsonXplorer.html               # JsonXplorer API Studio (REST client + Tree Inspector)
│   └── img/                           # Screenshots and visual media for Req handler tools
│       └── Screenshot 2026-10-29 122908.png
├── <Future-Category>/                 # Expandable for upcoming developer tools
│   ├── <ToolName>.html                # Standalone tool entrypoint
│   └── img/                           # Screenshots for the respective tool
├── .gitattributes
└── README.md                          # Repository documentation & directory
```

---

## 🧰 Available Tools Catalog

| Category | Tool Name | File Entry | Description | Status |
| :--- | :--- | :--- | :--- | :---: |
| **API & Data** | **JsonXplorer API Studio** | [`Req handler/JsonXplorer.html`](Req%20handler/JsonXplorer.html) | High-performance REST API client, Monaco code editor, interactive tree view with recursive unescaping & JSON auto-repair. | ✅ Ready |
| *Upcoming* | **JWT Inspector & Decoder** | `Security/JwtInspector.html` | Client-side token header/payload parser, expiration calculator, and claim analyzer. | 🚧 Planned |
| *Upcoming* | **Regex Live Lab** | `Text/RegexLab.html` | Real-time regular expression tester with syntax explanations and group extractors. | 🚧 Planned |
| *Upcoming* | **Base64 / Hash Studio** | `Crypto/HashStudio.html` | Multi-format text/file encoder, decoder, HMAC, and cryptographic hash generator. | 🚧 Planned |

---

## 🌟 Featured Tool: JsonXplorer API Studio

Located at [`Req handler/JsonXplorer.html`](Req%20handler/JsonXplorer.html), **JsonXplorer** is an all-in-one API testing and JSON exploration workbench:

### Key Highlights
- 🌐 **Full REST API Client**: Supports `GET`, `POST`, `PUT`, `DELETE` with custom query parameters, custom headers, and authentication (Bearer Token, Basic Auth).
- 🔗 **Smart URL Param Extraction**: Paste any full URL with query parameters (e.g. `https://api.example.com/v1?page=2&limit=50`), and JsonXplorer automatically splits and populates the config grid.
- 💻 **Monaco Code Editor**: Powered by the same editor engine as VS Code, complete with dark theme, line numbers, and custom line highlights for JSON syntax errors.
- 🌲 **Interactive Tree Hierarchy**: Explore complex payloads with collapsible nodes, item counters, clean indentation guides, and leaf/object badges.
- 🪄 **Deep Unescape & Auto-Repair**:
  - Automatically parses stringified JSON embedded within fields.
  - Automatically detects and repairs common syntax errors: trailing commas, single quotes, unquoted keys, and Python literals (`True`/`False`/`None`).
- 🎯 **JSONPath & Subtree Copy**: One-click copying of exact JSONPaths (e.g., `$.data.users[0].id`) or isolated subtree branches.
- 🔍 **Live Search & Filter**: Real-time keyword filtering across keys and values with instant match highlights and automatic node expansion.
- 💾 **Export & Clipboard**: Copy full formatted JSON or export directly to an `exported_data.json` file.

### How to Run
Simply double-click [`Req handler/JsonXplorer.html`](Req%20handler/JsonXplorer.html) or open it in any modern browser (Chrome, Edge, Firefox, Brave, Safari). **No server or installation needed.**

---

## 🚀 How to Add New Tools to this Repo

Contributions of new utilities are welcome! To maintain consistency:

1. **Pick or create a category directory** (e.g., `Text tools/`, `Req handler/`, `Formatters/`).
2. **Keep the tool standalone**: Build as a single `.html` file containing internal or CDN-backed scripts (e.g., Lucide, Monaco, Tailwind/Vanilla CSS).
3. **Include an `img/` folder**: Add a high-resolution screenshot inside `<Tool-Directory>/img/`.
4. **Update the Catalog**: Register the new tool in the [Available Tools Catalog](#-available-tools-catalog) table above.
5. **Ensure AI compatibility**: Provide intuitive inputs, keyboard accessibility, and exportable outputs so humans and AI agents can both utilize it seamlessly.

---

## 📸 Tool Previews & Screenshots

### JsonXplorer API Studio
*REST Client & Interactive JSON Tree Workspace with Deep Unescaping*

![JsonXplorer API Studio Screenshot](Req%20handler/img/Screenshot%202026-10-29%20122908.png)

*(Screenshots for each new tool are placed in their respective tool's `img/` folder and showcased above.)*

---

## 📄 License

This repository and its tools are open-source and released under the **MIT License**. Feel free to use, modify, and extend them in your own projects!
