# Shakespeare QA Bot

## Overview

Shakespeare QA Bot is an intelligent question-answering system that allows users to explore and extract information from Shakespeare's complete works. Leveraging advanced Natural Language Processing (NLP) techniques, this bot can answer questions about characters, plots, themes, and more from Shakespeare's extensive literary corpus.

## Features

- **Intelligent Question Answering**: Uses state-of-the-art DistilBERT model to extract precise answers
- **Named Entity Recognition**: Intelligently matches questions to relevant text segments
- **Web Interface**: Interactive Gradio-powered UI for easy querying
- **Comprehensive Text Processing**: Handles PDF text extraction, cleaning, and segmentation

## Technologies Used

- Python
- Hugging Face Transformers (DistilBERT)
- spaCy
- PyPDF2
- Gradio
- DistilBERT

## Installation

### Prerequisites

- Python 3.8+
- pip package manager

### Required Libraries

```bash
pip install transformers spacy PyPDF2 gradio
python -m spacy download en_core_web_sm
```

## Project Structure

```
shakespeare-qa-bot/
│
├── data/
│   └── Shakespeare-Complete-Works.pdf
│
│
├── notebooks/
│   └── Shakespeare_QA.ipynb
│
└── README.md
```

## How It Works

1. **Text Extraction**: Extracts text from Shakespeare's complete works PDF
2. **Text Cleaning**: Removes unnecessary whitespace, headers, and irrelevant content
3. **Text Segmentation**: Breaks text into manageable 500-character chunks
4. **Named Entity Recognition**: Identifies and caches key entities in each text segment
5. **Question Matching**: Finds the most relevant text segment for a given question
6. **Answer Generation**: Uses DistilBERT to extract precise answers

## Usage

### Running the Gradio Interface

Launch a web interface where you can ask questions about Shakespeare's works.

### Example Queries

- "Who is Bertram?"
- "What happens in Romeo and Juliet?"
- "Describe Macbeth's character"
- "Who wrote these plays?"

## Model Details

- **Model**: DistilBERT (Question Answering variant)
- **Key Features**:
  - 60% smaller than BERT
  - Retains 97% of language understanding
  - Fine-tuned for precise answer extraction

## Limitations

- Accuracy depends on the quality and coverage of the source PDF
- May struggle with highly complex or context-dependent questions
- Limited to the text of the provided Shakespeare works

## Acknowledgments

- Hugging Face Transformers
- spaCy NLP
- Gradio for the web interface