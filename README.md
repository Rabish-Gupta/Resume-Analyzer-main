# AI Resume Analyzer

A small Python project to parse resumes and match them to job descriptions. It provides a simple pipeline for extracting text from resumes, modeling the important fields, and scoring matches against job requirements.

## Features

- Parse resumes and extract candidate information.
- Represent resumes and jobs using lightweight data models.
- Match and score resumes against job descriptions.
- Pluggable prompts/helpers for integrating LLMs or rule-based matching.

## Quickstart

1. Create a Python 3.8+ virtual environment and install dependencies:

```bash
python -m venv .venv
.\.venv\Scripts\activate
pip install -r requirements.txt
```

2. Run the analyzer (simple example):

```bash
python main.py
```

Adjust command-line arguments or call the modules directly from your own scripts.

## Project layout

- `main.py` — entry point / CLI glue.
- `parser.py` — resume parsing and text extraction helpers.
- `models.py` — data classes for resumes, jobs, and match results.
- `matcher.py` — matching and scoring logic.
- `prompts.py` — prompt templates / LLM helpers.

## Usage notes

- The project is intentionally minimal and meant as a starting point. You can replace parsing with a PDF/text extractor of your choice or hook in a cloud OCR service.
- If you integrate an LLM, keep API keys out of source control and use environment variables.

## Development

- Run linters and tests (if present) before committing.
- Open a PR for changes and include small focused commits.
