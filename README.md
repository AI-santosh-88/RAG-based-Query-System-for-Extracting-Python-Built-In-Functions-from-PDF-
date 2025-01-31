## Project Title: "RAG-based Query System for Extracting Python Built-In Functions from PDF"

### Project Description:
This project builds an NLP-based query system utilizing a Retrieval-Augmented Generation (RAG) model to extract and generate answers from a PDF document containing Python’s built-in functions. The system retrieves relevant document sections using a vector-based retrieval mechanism (e.g., using embeddings), then augments this information with a generative model to provide contextually relevant answers to user queries. The entire system is designed to process unstructured PDF data, transforming it into a queryable knowledge base.

### Responsibilities:
#### 1.PDF Fetching & Document Storage:
* Use HTTP requests to download the PDF document from a specified URL.
* Store the document locally for further processing

#### 2.Document Preprocessing & Text Extraction:
* Extract raw text from the PDF using the LangChain UnstructuredFileLoader.

#### 3.Document Chunking & Text Splitting:
* Split the large document into smaller, more manageable chunks using CharacterTextSplitter, allowing the system to handle long documents efficiently.

#### 4.Embedding & Vectorization:
* Convert the document text into dense vector representations using HuggingFaceEmbeddings to create searchable embeddings for later retrieval.

#### 5.Vector Database Setup & Management:
* Use Chroma for storing the document embeddings and enable fast, efficient retrieval of relevant chunks during a query.
  
#### 6.Retrieval-Augmented Generation (RAG) Model Setup:
* Implement the RAG model, which first retrieves relevant document chunks (using a retriever) and then uses a generative model (e.g., ChatGroq) to provide answers to user queries based on those chunks.

#### 7.Querying & Answer Generation:
* Implement the RetrievalQA chain to allow users to ask questions about Python’s built-in functions. The system retrieves relevant information from the vector database and uses the generative model to produce coherent and context-aware answers.

#### 8.Answer Generation & Output:
* Return the generated answers along with the sources used to generate those answers, providing transparency about where the information came from.

### Libraries Used:
#### Requests:
* Library for downloading the PDF from the provided URL.
#### LangChain Document Loaders: 
* Tools for reading and extracting text from unstructured documents like PDFs.
#### LangChain Text Splitters: 
* Used to break down the document into smaller chunks for efficient processing.
#### HuggingFace Embeddings: 
* Embeddings for transforming text into numerical vectors that can be indexed and queried.
#### Chroma: 
* Vector database for managing and querying embeddings.
#### LangChain Groq: 
* Interface for interacting with Groq-powered generative language models (e.g., Llama).
#### LangChain Chains: 
* Framework for creating QA systems, particularly focused on retrieval-augmented generation.




