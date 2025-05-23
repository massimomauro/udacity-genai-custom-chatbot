# Custom Character Chatbot with RAG

This repository contains a minimal example of building a **Retrieval‑Augmented Generation (RAG)** chatbot that answers questions about a custom knowledge base – in this case, fictional character descriptions stored in `data/character_descriptions.csv`.

The notebook illustrates how to:

1. Turn raw CSV data into dense **OpenAI embeddings**
2. Perform a lightweight **similarity search** to retrieve the most relevant chunks
3. Build a token‑aware **prompt** that feeds the retrieved context to an LLM
4. Compare answers *with* and *without* retrieval to see the gain in factuality

## Getting Started

This project uses [uv](https://github.com/astral-sh/uv) for fast, reproducible Python environments. Python 3.9+ is required.

1. **Clone the repository**

```bash
$ git clone https://github.com/<your‑user>/udacity-genai-custom-chatbot.git
$ cd udacity-genai-custom-chatbot
```

2. **Create and activate a virtual environment with uv**

```bash
$ uv venv .venv
$ source .venv/bin/activate
$ uv pip install -r requirements.lock.txt  # fully locked install
```

3. **Launch the notebook**

```bash
$ jupyter lab notebooks/custom_chatbot.ipynb
```

## Repository Layout

```
.
├── data/                       # CSV with the knowledge base
├── notebooks/
│   └── custom_chatbot.ipynb    # End‑to‑end walkthrough
├── requirements.txt            # Exact package versions
└── README.md                   # ← you are here
```

## OpenAI API

The notebook expects two environment variables (or you can hard‑code them while experimenting):

* `OPENAI_API_BASE` – base URL (e.g. `https://api.openai.com/v1`)
* `OPENAI_API_KEY`  – your secret key

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.