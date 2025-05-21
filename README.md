# RAG_pdf_test
upload a pdf and get answer about pdf context
RAG PDF Question Answering App

This is a local Retrieval-Augmented Generation (RAG) application that allows you to upload PDF documents and ask questions about their content.

## Features

- Upload PDF files via the web interface
- Extract and index text chunks 
- Use a local transformer-based language model for answering questions offline
- Simple Streamlit interface for easy interaction

## Installation

Clone the repository and install dependencies:

```bash
git clone https://github.com/yourusername/rag_pdf_test.git


python -m venv env
env\Scripts\activate


cd rag_pdf_test
pip install -r requirements.txt
streamlit run app.py





##################

if above will not run, then
delete the models folder and download_model.py

then create download_model.py file, then add below code in that file


from transformers import AutoTokenizer, AutoModelForCausalLM
model_id = "distilgpt2"
AutoTokenizer.from_pretrained(model_id).save_pretrained("models/distilgpt2")
AutoModelForCausalLM.from_pretrained(model_id).save_pretrained("models/distilgpt2")


# and run in terminal this command
# python download_model.py


# streamlit run app.py


 -->
