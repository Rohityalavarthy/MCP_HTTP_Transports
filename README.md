# MCP HTTP Transport Demo

An interactive demo for experimenting with the **Model Context Protocol (MCP)** over **streamable HTTP transport**.

This project combines:
- A **Python MCP server** (`main.py`) exposing simple tools (e.g., an `add` function).
- A **frontend client** (`index.html`) to send MCP requests and visualize responses, including **Server-Sent Events (SSE)**.

---

## 🚀 Features
- **Initialize** an MCP session and exchange capabilities.
- Send **notifications** (`initialized`) to complete setup.
- Perform **tool calls** (e.g., add two numbers).
- Issue **custom MCP requests** (e.g., `tools/list`, `resources/list`).
- Observe **server-initiated events** via GET **SSE connections**.
- Interactive, styled UI for inspecting request/response headers and streaming data.

---

## 📂 Project Structure
├── main.py # MCP server with HTTP transport
├── index.html # Interactive web client for MCP requests
├── pyproject.toml # Project configuration (dependencies, metadata)
└── README.md # Project documentation

---

## 🛠️ Installation & Setup

### Prerequisites
- Python 3.10+
- [MCP Python library](https://pypi.org/project/mcp/)

### Install dependencies
Install dependencies using uv:

```bash
uv sync
```
pip install -e .
Run the MCP HTTP server
python main.py
The server runs by default at:
http://localhost:8000/mcp/
🌐 Using the Web Client
Open index.html in your browser.
Click Initialize Request to start a session.
Send Initialized Notification.
Try a Tool Call (e.g., add 5 + 3).
Experiment with Custom Requests (tools/list, etc.).
Start SSE monitoring to observe server-initiated events.
📖 Learning Goals
This repo is designed as a learning and experimentation playground for:
Understanding the MCP specification.
Exploring HTTP transport mechanisms for MCP.
Working with streaming responses using SSE.
🤝 Contributing
Feel free to open issues or PRs if you’d like to extend this demo with more MCP features or UI enhancements.


## Running the Project

Run the MCP server:

```bash
uv run main.py
```
