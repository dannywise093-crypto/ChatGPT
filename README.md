ChatGPT-Workspace
A unified repository containing two distinct sub-projects: chatgpt-clone (a custom web interface modeling the ChatGPT experience) and gpt4free (a reverse-engineered backend provider integration framework).
📁 Repository Structure

`ChatGPT Workspace`
A monolithic repository hosting two independent applications: chatgpt-clone (a responsive, feature-rich web frontend modeled after OpenAI's ChatGPT) and gpt4free (a multi-provider API proxy framework delivering zero-cost access to modern Large Language Models).
`ChatGPT/
├── chatgpt-clone/         # Web Application (Frontend / UI Interface)
│   ├── public/            # Static assets and UI icons
│   ├── src/               # Application source components & state management
│   └── package.json       # Node.js dependencies and run scripts
│
├── gpt4free/              # API Service Framework (Backend Proxy)
│   ├── g4f/               # Core routing, provider modules, and wrappers
│   ├── requirements.txt   # Python runtime dependencies
│   └── main.py            # Local proxy entry point
│
├── .venv/                 # Python Virtual Environment
└── README.md              # Project documentation`

# 🚀 Sub-Projects Breakdown`

1. chatgpt-clone
A modern, lightweight web interface engineered to emulate the official ChatGPT user experience.
Highlights: Real-time token streaming, persistent local session history, custom system prompts, and responsive dark/light UI modes.
Tech Stack: JavaScript / TypeScript, Node.js, HTML5, CSS3.
2. gpt4free
An open-source Python framework (g4f) that aggregates public, reverse-engineered API endpoints to provide access to advanced LLMs without requiring API keys.
Highlights: Multi-model routing (GPT-4o, Claude, Llama, Mistral), OpenAI-compatible endpoint emulation, and asynchronous request handling.
Tech Stack: Python 3.10+, FastAPI / Flask, asyncio, aiohttp.
⚡ Quick Start & Deployment
Prerequisites
Python: 3.10 or higher
Node.js: v18.0.0 or higher
`Installation & Execution`
# Clone the Repository
`git clone https://github.com/dannywise093-crypto/ChatGPT.git
cd ChatGPT`

Initialize & Run gpt4free (Backend API)
# Activate virtual environment
`source .venv/bin/activate`

# Install dependencies and start local server
`cd gpt4free
pip install -r requirements.txt
python -m g4f.cli api --port 1337
`

`cd chatgpt-clone
npm install
npm run dev`

# ⚙️ Environment Configuration
Define local environment variables by creating a .env file within the chatgpt-clone directory:
# Server Configuration
PORT=3000

# Backend Provider Connection
VITE_API_BASE_URL=http://localhost:1337/v1
DEFAULT_MODEL=gpt-4o

# Feature Flags
ENABLE_STREAMING=true
MAX_CONTEXT_TOKENS=4096

# ⚠️ Legal Disclaimer
This repository is maintained strictly for educational, experimental, and research purposes. Users are responsible for ensuring compliance with the Terms of Service of third-party services accessed through the gpt4free provider framework.
