# Streamlit_app_ollama_with_Google_colab
This project demonstrates how to deploy and interact with open-source Ollama models directly from Google Colab using a Streamlit web application.
It enables developers and researchers to build, test, and share conversational AI or LLM-based prototypes in minutes — entirely in the cloud, without requiring local installations.

# Table of Contents
Project Overview

Features

Installation

Usage

Example Workflow (Colab)

Project Structure

Contributing

License

Contact

# Project Overview
This project demonstrates how to set up and run a conversational LLM (Large Language Model) pipeline in Google Colab using the Ollama open-source model server and a custom Streamlit app for PDF summarization and interactive responses. Ngrok tunnels are used to make both the Streamlit app and Ollama server accessible for real-time cloud interaction.

1. Upload multiple PDFs in Colab.

2. Summarize with selected LLM models (e.g., Llama 3, Gemma 2).

3. View results in a Streamlit interface.

4. Export summaries to Excel.

# Features
1. End-to-end pipeline: Google Colab (cloud notebook) + Ollama server + Streamlit frontend (via ngrok).

2. Multi-model support: Easily swap between LLMs (examples: Llama 3, Gemma 2).

3. Automated PDF upload, text extraction, and chunking.

4. Concise and extended summaries via Ollama API.

5. Instant Excel download of results.

6. No need for local hardware setup—everything runs in Colab.

# Installation
1. Run in Google Colab:

      Clone or upload notebook: Use Copy-of-Streamlit_app_ollama_with_Google_colab.ipynb in Colab.

2. Install required libraries (auto-installs in notebook):

      !pip install streamlit PyMuPDF4LLM pandas openpyxl pyngrok requests

4. Install Ollama and ngrok:

      !curl -fsSL https://ollama.com/install.sh | sh

      !curl -s https://ngrok-agent.s3.amazonaws.com/ngrok.asc | sudo tee /etc/apt/trusted.gpg.d/ngrok.asc >/dev/null
      echo "deb https://ngrok-agent.s3.amazonaws.com buster main" | sudo tee /etc/apt/sources.list.d/ngrok.list
      sudo apt update && sudo apt install ngrok

# Usage
Notebook Flow:

1. Model selection: Choose from available LLM models (Llama3.2, Gemma2, etc.).

2. PDF upload: Use Streamlit UI in Colab to upload one or more PDF files.

3. Generate summaries: Click “Generate Summaries” to process PDFs.

4. View summaries: For each PDF/model, see 50-word and unlimited summaries.

5. Download results: Export results to Excel directly from the UI.

6. Streamlit App URL: Colab will display your unique ngrok URL for accessing the Streamlit interface (runs in your cloud environment).

# Example Workflow (Colab)
1. Upload PDFs

2. Select Model (sidebar)

3. Summarize and view results

4. Download Excel sheet for summary data

# Project Structure
Streamlit_app_ollama_with_Google_colab/

- Copy-of-Streamlit_app_ollama_with_Google_colab.ipynb  # Main Colab notebook
  
- app.py                 # Streamlit frontend (written by notebook)

- requirements.txt       # Python dependencies (if included)
  
- README.md              # This documentation

# Contributing
Contributions and suggestions are welcome! To propose changes, open an issue or pull request. For bug reports, include clear reproduction steps and screenshots if possible.

# License
See the LICENSE file for details.

# Contact
Maintainer: Tapas Mahanand (GitHub Profile)

For issues/support, use the GitHub “Issues” tab or Colab comments.


