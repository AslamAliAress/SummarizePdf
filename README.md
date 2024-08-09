#  PDF Summary with LangChain.js

This project is a Node.js application designed to process PDF documents and generate concise summaries based on their content. It utilizes the `langchain` library to load and split the document into manageable chunks, and then summarize the content using retrieval-augmented generation (RAG).

## Prerequisites

Before you begin, ensure you have Node.js installed. You can verify the installation by running:

```bash
node -v
```

If Node.js is not installed, download and install it from here: https://nodejs.org/en

## Setup

1. Initialize the project
Open your terminal and run the following command to create a new Node.js project:

```bash
npm init -y
```
2. Install the necessary dependencies
Run the following commands to install the required libraries:

```bash
npm install langchain 
npm install pdf-parse
npm install @langchain/community
npm install @langchain/openai 
npm install dotenv
```
3. Set up the environment variables
Create a .env file in the root directory of your project and add your OpenAI API key:
```bash
OPENAI_API_KEY=your_openai_api_key_here
```
## Running the Application
1. Load a PDF Document
Make sure to specify the path to the PDF document in the PDFLoader line in the code:

```bash
const loader = new PDFLoader("C:/Users/aslam.ali/Downloads/samplePdf.pdf");
```
2. Run the application
Use the following command to start the application:

```bash
node index.js
```
3. Interact with the application
The application will prompt you to ask a question related to the PDF document. You can continue to ask questions or type "e" to exit.


## Key Features
- PDF Loading: Efficiently load and process PDF documents.
- Document Chunking: Split large documents into smaller chunks for better processing and retrieval.
- Content Summarization: Generate concise summaries of PDF content using retrieval-augmented generation (RAG).
- Contextual Prompting: Guided summarization using system and human prompt templates.

## Important Notes
- Make sure the PDF file path is correct and accessible.
- An OpenAI API key is required for generating embeddings and summarizing the content.
- The langchain library's in-memory vector store is used to store and retrieve document chunks efficiently.
