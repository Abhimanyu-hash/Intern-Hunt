# InternHunt

## Overview

`InternHunt` is a Streamlit-based internship discovery app for students and early-career professionals. It parses a PDF resume, extracts technical skills and experience, and then searches for internship opportunities using online search APIs. The app also evaluates match fit percentages for each internship and provides improvement recommendations.

## Features

- PDF resume upload and validation
- Resume parsing for skills, education, experience, and projects
- Query generation using spaCy and optional Ollama model support
- Internship search through SerpAPI
- Job fit analysis using cosine similarity and optional LLM skill extraction
- Matching skills, missing skills, and course recommendations
- Visual fit results with pie charts

## Project Structure

- `README.md` - Project documentation
- `dti/internhunt.py` - Main Streamlit application code

## Prerequisites

- Python 3.9+
- `pip` or another Python package manager
- A SerpAPI API key if you want internship search functionality
- Optional: Ollama server running locally for LLM-based enhancements

## Installation

1. Clone the repository or download the source:

```bash
git clone https://github.com/Abhimanyu-hash/Intern-Hunt.git
cd Intern-Hunt
```

2. Create and activate a Python environment:

```bash
python -m venv venv
source venv/bin/activate
```

3. Install dependencies:

```bash
pip install streamlit pdfplumber nltk spacy ollama matplotlib serpapi scikit-learn
```

4. Install the spaCy English model:

```bash
python -m spacy download en_core_web_sm
```

## Running the App

Run the Streamlit application:

```bash
streamlit run dti/internhunt.py
```

Then open the provided local URL in your browser.

## Configuration

- Set your SerpAPI API key in the app or environment variables if you want real job search results.
- If you have Ollama installed and running on `http://localhost:11434`, the app will use it for better query generation and job analysis.

## Notes

- The app currently expects a PDF resume upload.
- The search and analysis flow depends on external services, so ensure network access and API credentials are configured.
- `internhunt.py` includes debugging output to help trace parsing and analysis steps.

## License

This repository is provided as-is for educational and internship search automation purposes.
