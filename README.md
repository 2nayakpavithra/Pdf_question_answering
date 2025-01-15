# Pdf_question_answering
PDF Question Answering is an AI-powered application that allows users to extract answers from PDF files by asking questions. It leverages advanced natural language processing techniques and powerful libraries to provide quick and accurate responses.

## Tools & Techs used : 
    AstraDB : This is cloud based NoSql database which is built on the top of the Apache Cassandra
    HuggingFace Hub : It is the hub of LLM models. Models can be based on the required task through the HuggingFace API 
    LangChain     : The LangChain is the framework, where a  developer can build desired AI applications using the LLM models with the help of the HuggingFace API 

# Steps:
1) Installation : Install required libraries and the dependencies

2) Upload PDF files: Initially, the textbook in the PDF file is uploaded to to the google drive and mounted to the google colab to get the access for extraction and processing. 

3) Connecting Details : You need to connect your application with the AstrDB and HuggingFace API
                 -----Connect AstraDB with API_endpoint and AstraDB application token which is unique for each account and the collection name
                 -----HuggingFace Hub can be connected with HuggingFace_api_token : This is unique for each individual and confidential
                 (Note : Do not share this Connection details with anyone)
                 
4) Extract text: The application extracts the text content from the uploaded PDF files using pyPdf library.

5) Text processing and embeddings: The text is processed and split into chunks using langchain's CharacterTextSplitter, and semantic embeddings are generated using HuggingFaceEmbeddings.

6) Building the knowledge base: The text chunks and embeddings are stored in AstraDB, enabling efficient vector similarity search.

7) User interaction and question answering: Users can input their questions, and the application utilizes the question answering chain to provide answers.

8) Session history and clearing: The application keeps track of user queries and their answers, and the session history can be cleared with the "Clear" button.

