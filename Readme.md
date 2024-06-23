# Context Length Experiment: Evaluating Gemini 1.5 Flash

This repository contains an experiment to test Gemini 1.5 Flash's ability to answer questions about up to 1 million tokens of context. The experiment uses a Kaggle dataset containing App Store data to systematically evaluate the model's performance across varying context lengths to see if it degrades with increasing context length.

Unlike traditional [Needle-in-a-Haystack (NIAH) tests](https://arize.com/blog-course/the-needle-in-a-haystack-test-evaluating-the-performance-of-llm-rag-systems/), this experiment uses a real-world dataset where all information is potentially relevant. It tests the model's ability to synthesize and reason across a large, cohesive body of information, rather than simply retrieving irrelevant pieces of data. When the needles are irrelevant to the haystack, the challenge becomes more of an anomaly detection problem. This experiment is meant to give us a sense of how confidently we can trust answers from an LLM in long context use cases, like asking questions about your company data.

## Overview

The main notebook, [Context_Length_AppStoreV2.ipynb](Context_Length_AppStoreV2.ipynb), includes:

- Data collection and preparation using the App Store Apple Data Set
- Implementation of evaluation and prediction functions
- Experiment setup to test Gemini 1.5 Flash across increasing context lengths
- Visualization of test results



## Requirements

To run this experiment, you'll need:

1. A Langsmith account and API Key
2. A Google AI Studio API key
3. An OpenAI API key

## Setup

1. Clone this repository
2. Create a copy of the `.env.sample` file and save it as `.env`
3. Add your API keys to the `.env` file
4. Install the required libraries:

```bash
pip install -qU pandas tiktoken langchain langchain-openai langchain-google-genai matplotlib langsmith python-dotenv seaborn
```

## Running the Experiment

Open the [Context_Length_AppStoreV2.ipynb](Context_Length_AppStoreV2.ipynb) notebook and run the cells sequentially. The notebook will guide you through:

1. Data preparation
2. Setting up the evaluation dataset
3. Implementing the evaluation and prediction functions
4. Running the experiment across different context lengths
5. Visualizing the results

## Results

Gemini 1.5 performed at 100% accuracy across all context lengths tested! 

**[View Test Results on LangSmith](https://smith.langchain.com/public/0f86f6ab-aaf0-4262-b38d-bed96e243a15/d)**

