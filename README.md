# Llama Index Evaluation Tool

## Introduction

This tool is designed to evaluate large language models (LLMs) and their embeddings, focusing on aspects such as faithfulness, relevancy, and correctness. It uses various components from the llama_index library, integrates OpenAI and Cohere APIs, and supports asynchronous operations for efficient processing.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
- [Features](#features)
- [Dependencies](#dependencies)
- [Configuration](#configuration)
- [Troubleshooting](#troubleshooting)

## Installation

1. Clone the repository:
```shell
git clone https://github.com/felipearosr/RAG-Evaluation
```

2. Install the required packages:

```shell
pip install -r requirements.txt
```

## Usage

To use this tool, set up your environment variables for OpenAI and Cohere API keys, then run the script using:

```shell
python eval.py --generate
```

Use the `--generate` flag to generate new questions before evaluation. This is not needed if you already generated the questions. This questions will go into the file `questions.json`.

## Features

- Evaluation of LLMs based on faithfulness, relevancy, and correctness.
- Integration with OpenAI and Cohere for embeddings and reranking.
- Asynchronous question generation and evaluation.
- Results output to CSV for analysis.

## Dependencies

- Python 3.x
- openai
- cohere-python
- pandas
- dotenv
- asyncio
- argparse
- llama_index library

## Configuration

Configure the tool by setting the following environment variables:

- `OPENAI_API_KEY`: Your OpenAI API key.
- `COHERE_API_KEY`: Your Cohere API key.
- `MODEL`: The LLM model name, default is "gpt-4-0125-preview".
- `EMBEDDING`: The embedding model name, default is "text-embedding-3-large".


## Troubleshooting

If you encounter issues, ensure your API keys are set correctly and that you have the correct permissions for accessing the APIs.
