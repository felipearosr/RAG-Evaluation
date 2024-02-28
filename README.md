# Llama Index Evaluation Tool

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

2. Navigate to the project directory:
```shell
cd RAG-Evaluation
```

3. Create a conda environment:

```shell
conda create -n rag-eval python==3.11 -y && source activate rag-eval
```
This creates a new Conda environment named rag-eval and activates it. Using a virtual environment is recommended to avoid conflicts with other Python projects or your system's Python.

4. Install the required packages:

```shell
pip install -r requirements.txt
```

## Usage

Running the Evaluation Script:

1. Generate New Questions (Optional):

    If you need to generate new questions for evaluation, use the --generate flag. This step is optional if you have already generated questions stored in questions.json:

```shell
python eval.py --generate
```

This command generates new questions based on the documents provided and saves them to `questions.json`. If you skip this step, the script will use existing questions from the file.

2. Run the Evaluation:

Once you have your questions ready (either newly generated or previously stored), run the script without the `--generate` flag to start the evaluation:

```shell
python eval.py
```
This command evaluates the set questions using the configured LLMs and embeddings, then outputs the results.

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

Configure the tool by setting the following environment variables in your `.env` file, you can follow the example of `.env.example`:

- `OPENAI_API_KEY`: Your OpenAI API key.
- `COHERE_API_KEY`: Your Cohere API key.
- `MODEL`: The LLM model name, default is "gpt-4-0125-preview".
- `EMBEDDING`: The embedding model name, default is "text-embedding-3-large".


## Troubleshooting

If you encounter issues, ensure your API keys are set correctly and that you have the correct permissions for accessing the APIs.
