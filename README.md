# BDC6223 Literature Review Bot

## Team Members
- Hou Xingyu
- Li Jingying
- Lin Xingyu
- Liu Yaoyao

## Problem Statement

The project addresses the challenge of efficiently summarizing, analyzing, and comparing research documents, such as academic papers. Researchers often face information overload and need tools that can quickly extract key insights, find relevant documents, and compare them effectively. This project aims to streamline this process, saving time and enhancing productivity.

## Solution Approach

We developed a system that leverages large language models (LLMs) and vector search to process research documents. Here's how it works:

- **LLM and Tools**: We used LangChain to connect GPT-4 with various document processing tools. The system utilizes OpenAI Embeddings to convert document text into vector representations and FAISS for efficient vector storage and retrieval.
- **Document Processing**: PDFs are loaded using `PyPDFLoader`, and embeddings are created for each document.
- **Retrieval and QA**: Using LangChain's `RetrievalQA` chain, the system can summarize documents, find relevant papers based on user queries, and compare them.
- **Frameworks and Libraries**: The project uses LangChain, LangGraph, OpenAI API, FAISS, and Pandas.
- **Dataset**: The documents processed are offline PDFs containing research abstracts.

## Instructions

### Setup

1. **Clone the repository**
   ```bash
   git clone https://github.com/xinyuhou19980831/dbc6223.git
   cd dbc6223
   ```

2. **Create and activate a virtual environment**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows use `venv\Scripts\activate`
   ```

3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```

4. **Set up API keys**
   - Create a `.env` file in the project root and add your OpenAI API key:
     ```env
     OPENAI_API_KEY=your_openai_api_key
     ```

### Running the Project

1. **Open the Jupyter Notebook**
   ```bash
   jupyter notebook
   ```

2. **Navigate to the project notebook (`project.ipynb`) and open it.**

3. **Run the notebook cells sequentially** to execute the project. Ensure all dependencies are installed and API keys are properly set.


## Results

The system currently supports the following features:

1. **Summarizing Offline PDFs**: Automatically summarizes the methodologies and key insights from research documents.
2. **Finding Relevant Documents**: Locates the document most relevant to a user-specified topic.
3. **Documents Comparison**: Compares multiple documents and ranks them based on similarity scores related to the indicated topic.
4. **Online Document Search**: Searches for papers that are relevant to indicated topics online.
5. **Topic Extraction, Document Clustering and Literature Review**: Groups similar documents together based on topic in a given PDF, enabling easier navigation, analysis and review.

### Example

- **Input**: A set of PDFs with research abstracts.
- **Query**: "Summarize the methodologies and key insights from these papers."
- **Output**: A structured table listing each paper title with its summarized insights.

## Future Work

- **Enhanced Summarization**: Integrate more advanced summarization techniques.
- **Broader Document Types**: Support for Word documents and other formats.
- **Improved UI**: Develop a more interactive web interface with enhanced visualization.
- **Scalability**: Optimize for larger datasets and concurrent users.

## Notes

- Ensure your OpenAI API key has sufficient usage limits.
- The system may need adjustments based on the complexity and structure of input documents.

## Acknowledgments

- Thanks to the developers of LangChain, FAISS, and OpenAI for their robust tools and APIs.
