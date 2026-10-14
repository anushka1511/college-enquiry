# Multi-Agent College Enquiry Chatbot Using RAG and LCEL

A college enquiry chatbot built using Python, LangChain, LCEL, RAG, and the Gemini API. The system routes student questions to specialist agents for admissions and academic enquiries.

## Overview

Students often need to search through multiple sources to find information about admissions, fees, scholarships, attendance, examinations, and academic procedures.

This project uses a multi-agent approach to route questions to the appropriate specialist. Each specialist retrieves relevant information from a FAQ knowledge base and uses a language model to generate a contextual response.

## Features

- Query classification and routing
- Separate admissions and academic specialist agents
- Retrieval-Augmented Generation (RAG)
- Semantic search using sentence embeddings
- FAISS vector database
- Gemini-powered answer generation
- Source ID references in responses
- Fallback handling for unrelated questions
- Basic routing accuracy evaluation

## Technologies Used

- Python
- Google Colab
- LangChain
- LangChain Expression Language (LCEL)
- Google Gemini API
- Hugging Face Sentence Transformers
- FAISS

## System Workflow

1. The student enters a question.
2. The router classifies the question.
3. The appropriate specialist agent is selected.
4. The agent retrieves relevant FAQ documents from its vector database.
5. The retrieved context is passed to the Gemini language model through an LCEL pipeline.
6. The chatbot returns a response grounded in the retrieved information.

## Project Structure

```text
college-enquiry-chatbot/
├── college_enquiry_chatbot.ipynb
├── README.md
└── .gitignore
```

## How to Run

### 1. Open Google Colab

Open the notebook `college_enquiry_chatbot.ipynb` in Google Colab.

### 2. Install dependencies

Run the first notebook cell to install the required libraries.

### 3. Configure the API key

Obtain a Gemini API key from [Google AI Studio](https://aistudio.google.com/apikey).

Run the API configuration cell and enter your key when prompted. Never hardcode your API key or upload it to GitHub.

### 4. Execute the notebook

Run all cells in order to create the FAQ knowledge base, initialize the embedding model and vector databases, configure the Gemini model, build the specialist agents, and launch the chatbot.

## Sample Questions

- What documents are required for admission?
- How can I apply for a scholarship?
- What is the attendance requirement?
- How can I check my semester grades?
- Where can I find the academic calendar?

## Evaluation

The notebook includes a basic routing evaluation that compares predicted categories with expected categories for a small set of test questions.

This evaluation measures routing performance only. Answer correctness and retrieval quality require separate testing.

## Limitations

- The chatbot depends on the completeness and accuracy of its knowledge base.
- The included FAQ data is illustrative and should be replaced with verified institutional information.
- The language model may generate inaccurate answers.
- A valid Gemini API key and available API quota are required.
- The current implementation supports admissions and academic enquiries.

## Future Improvements

- Integrate official college documents and handbooks.
- Add a Streamlit-based user interface.
- Evaluate retrieval relevance and answer correctness.
- Expand the number of specialist agents and enquiry categories.
- Add conversation history and document upload support.

## Security

Never commit API keys, passwords, or other credentials to version control. Use Colab's secret-management features or environment variables to manage sensitive information.

## License

For educational use. Add an appropriate open-source license if redistribution or reuse is intended.
