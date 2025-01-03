# LLM Analysis for PDF Querying with RAG Input

This repository contains a Python-based framework for analyzing various Large Language Models (LLMs) and their ability to process and answer questions from PDFs using RAG (Retrieval-Augmented Generation) input. The analysis involves comparing multiple models like Llama, Gemma, Qwen, and Mistral in terms of accuracy, relevance, and processing time, both with and without context.

## Features

- **Comparison of multiple LLMs**: Includes Llama, Gemma, Qwen, and Mistral.
- **Query-based analysis**: Questions are answered with and without contextual PDF input.
- **Time performance tracking**: Logs response times for each model with and without context.
- **Formatted answers**: Outputs answers with appropriate markdown formatting.
- **PDF context processing**: Extracts and processes content from a PDF document to provide context for answering queries.

## Directory Structure

```
root/
├── main.ipynb                 # Jupyter notebook that runs the analysis
├── answers_db/                # Stores model-generated answers
│   ├── context/               # Answers generated with PDF context
│   │   ├── gemma/
│   │   ├── llama/
│   │   ├── mistral/
│   │   └── qwen/
│   └── no_context/            # Answers generated without PDF context
│       ├── gemma/
│       ├── llama/
│       ├── mistral/
│       └── qwen/
└── time_db/                   # Stores timing logs for model responses
    ├── context/               # Time logs with context
    └── no_context/            # Time logs without context
```

## Prerequisites

Before running the notebook, you need to have the following installed:

- **Python 3.x** (preferably 3.8+)
- **CUDA** (for GPU acceleration, if you plan to use a GPU)

## Setup and Installation

1. **Clone the repository:**

   Start by cloning this repository to your local machine:

   ```bash
   git clone https://github.com/josh1221wa/llm-rag-analysis.git
   cd llm-rag-analysis
   ```

2. **Install dependencies:**

   Use the `environment.yml` file to create a conda environment and install all the necessary libraries:

   ```bash
    conda env create -f environment.yml
   ```

3. **Download the required models:**

   The notebook uses Ollama models (`llama3.2`, `gemma2`, `qwen2.5`, and `mistral`). Make sure that these models are available and properly configured in your environment.

4. **Download and place a PDF file:**

   Place your desired PDF document (e.g., `Applications of Blockchain.pdf`) in the project directory. The PDF content will be used as context for the models' responses.

5. **Run the Jupyter Notebook:**

   After the setup is complete, run the Jupyter notebook:

   ```bash
   jupyter notebook llm_analysis.ipynb
   ```

## Usage

- **Querying Models**: The Jupyter notebook allows you to input your questions, and it will generate answers using various models. The notebook will display answers both with and without PDF context.
- **Time Analysis**: The models' response times are logged, allowing you to track performance.
- **Answer Storage**: The generated answers are stored in the `answers_db` directory, while response times are logged in `time_db`.

## Conclusion

Thank you for exploring this repository! Feel free to clone, modify, or extend it for your own experiments with large language models and blockchain applications, and don't hesitate to contribute or reach out with any questions.
