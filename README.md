# LLM Engineering Roadmap & Hands-On Labs

A practical repository for learning Large Language Model (LLM) engineering, API integrations, web scraping pipelines, and prompt engineering. This repository features step-by-step Jupyter notebooks and Python modules for building LLM-powered applications.

---

## 📋 Table of Contents

- [Overview](#-overview)
- [Repository Structure](#-repository-structure)
- [Modules & Topics Covered](#-modules--topics-covered)
- [Prerequisites](#-prerequisites)
- [Getting Started](#-getting-started)
- [Environment Setup](#-environment-setup)
- [License](#-license)

---

## 🔍 Overview

This workspace serves as a structured repository for building end-to-end LLM solutions. It covers fundamental and advanced concepts in LLM development:

- **Web Scraping & Preprocessing**: Clean and extract relevant web text while stripping unwanted HTML noise (scripts, styles, tags).
- **Multi-Provider API Integration**: Work with OpenAI Chat Completions and Google Gemini endpoints (via OpenAI compatibility layer and native SDKs).
- **Prompt Engineering & Content Summarization**: Construct system prompts to convert unstructured web text into structured markdown insights.

---

## 📂 Repository Structure

```text
llm-engineering/
├── pyproject.toml         # Project metadata & dependency definitions
├── uv.lock                # Lockfile for reproducible environment builds
├── .python-version        # Specifies Python version runtime (>= 3.11)
├── .gitignore             # Git ignore patterns for Python, secrets, and caches
├── README.md              # Project documentation
└── week-1/                # Week 1: Foundations & Scraping Pipeline
    ├── day_1.ipynb        # Lab 1: Web scraper integration & OpenAI API summaries
    ├── day_2.ipynb        # Lab 2: Direct REST calls & Gemini API endpoints
    └── scraper.py         # Utility module for web content extraction & HTML parsing
```

---

## 🎓 Modules & Topics Covered

### `week-1/` — Core Foundations & API Integrations

- **`scraper.py`**:
  - `fetch_website_contents(url)`: Fetches HTML, cleans noise (`script`, `style`, `img`, `input`), and extracts text stripped of boilerplate.
  - `fetch_website_links(url)`: Extracts all embedded hyperlinks from a web page.
- **`day_1.ipynb`**:
  - Environment validation and OpenAI API initialization.
  - Integration with `scraper.py` to extract website contents dynamically.
  - Structured prompt engineering for automated website summarization.
- **`day_2.ipynb`**:
  - Direct HTTP `POST` requests to OpenAI REST endpoints using `requests`.
  - Python client SDK usage for model interaction.
  - Connecting to Google Gemini models using custom base URLs and Gemini API keys.

---

## 🛠️ Prerequisites

- **Python**: `>= 3.11`
- **Package Manager**: [`uv`](https://github.com/astral-sh/uv) (recommended) or `pip`
- **API Keys**:
  - [OpenAI API Key](https://platform.openai.com/)
  - [Google Gemini API Key](https://aistudio.google.com/) (optional for Day 2)

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/your-username/llm-engineering.git
cd llm-engineering
```

### 2. Set Up Virtual Environment & Dependencies

Using `uv` (recommended):

```bash
# Create virtual environment and install dependencies from pyproject.toml
uv sync
```

Using standard `pip`:

```bash
python3 -m venv .venv
source .venv/bin/activate  # On Windows: .venv\Scripts\activate
pip install -e .
```

---

## 🔑 Environment Setup

Create a `.env` file in the root directory:

```bash
touch .env
```

Add your API keys to `.env`:

```ini
OPENAI_API_KEY=sk-proj-your_openai_api_key_here
GOOGLE_API_KEY=your_google_gemini_api_key_here
```

> ⚠️ **Security Note**: The `.env` file is listed in `.gitignore` and must never be committed to source control.

---

## 📄 License

Distributed under the MIT License. See `LICENSE` for details.
