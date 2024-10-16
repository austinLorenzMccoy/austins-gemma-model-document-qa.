# Austin's Gemma Model Document Q&A

![Streamlit](https://img.shields.io/badge/Streamlit-1.24.1-blue)
![Python](https://img.shields.io/badge/Python-3.8%2B-blue)

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Demo](#demo)
- [Installation](#installation)
- [Configuration](#configuration)
- [Usage](#usage)
- [Project Structure](#project-structure)
- [Dependencies](#dependencies)
- [Environment Variables](#environment-variables)
- [Running the Application](#running-the-application)
- [Contributing](#contributing)
- [License](#license)

## Introduction

**Austin's Gemma Model Document Q&A** is a Streamlit-based web application that leverages LangChain, LangChain-Groq, and Google Generative AI Embeddings to provide an interactive Question & Answer system over a collection of PDF documents. Users can upload their documents, embed them into a vector store, and perform semantic searches to get precise answers based on the content.

## Features

- **Interactive UI**: Built with Streamlit for a seamless user experience.
- **Document Ingestion**: Loads and processes PDF documents from a specified directory.
- **Text Splitting**: Breaks down large documents into manageable chunks for efficient processing.
- **Vector Embeddings**: Utilizes Google Generative AI Embeddings for creating vector representations of documents.
- **Semantic Search**: Implements FAISS for efficient similarity searches within the document embeddings.
- **Custom Prompting**: Uses LangChain's `ChatPromptTemplate` to generate accurate and context-based responses.
- **Performance Tracking**: Measures and displays response times for queries.
- **Expandable Insights**: Provides detailed document similarity search results within expandable sections.

## Demo

![Demo Screenshot](path_to_demo_screenshot.png)

*Replace `path_to_demo_screenshot.png` with the actual path to your screenshot.*

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/austins-gemma-model-document-qa.git
   cd austins-gemma-model-document-qa
   ```

2. **Set Up a Virtual Environment**

   It's recommended to use a virtual environment to manage dependencies.

   ```bash
   python3 -m venv venv
   source venv/bin/activate  # On Unix or MacOS
   # or
   venv\Scripts\activate     # On Windows
   ```

3. **Install Dependencies**

   ```bash
   pip install -r requirements.txt
   ```

## Configuration

1. **Environment Variables**

   Create a `.env` file in the root directory of the project with the following content:

   ```env
   GROQ_API_KEY="your_groq_api_key_here"
   GOOGLE_API_KEY="your_google_api_key_here"
   ```

   - Replace `"your_groq_api_key_here"` with your actual GROQ API key.
   - Replace `"your_google_api_key_here"` with your actual Google API key.

2. **.gitignore**

   Ensure that your `.env` file is listed in `.gitignore` to prevent sensitive information from being committed to the repository.

   ```gitignore
   # Environment Variables
   .env
   ```

## Usage

1. **Prepare Your Documents**

   Place your PDF documents in the `./us_census` directory. Ensure that the directory exists and contains the PDFs you want to use for the Q&A system.

2. **Run the Application**

   ```bash
   streamlit run app.py
   ```

   Replace `app.py` with the name of your main Python script if it's different.

3. **Interact with the App**

   - **Title**: "Austin's Gemma Model Document Q&A"
   - **Enter Your Question**: Input your query in the provided text box.
   - **Embed Documents**: Click the "Documents Embedding" button to process and embed your documents.
   - **View Answers**: After embedding, enter a question to receive an answer based on your documents.
   - **Expand for Similar Documents**: Click on the "Document Similarity Search" expander to view relevant document excerpts.

## Project Structure

```
austins-gemma-model-document-qa/
├── .env
├── requirements.txt
├── app.py
├── us_census/
│   ├── document1.pdf
│   ├── document2.pdf
│   └── ...
├── venv/
├── README.md
└── LICENSE
```

- **.env**: Contains environment variables for API keys.
- **requirements.txt**: Lists all Python dependencies.
- **app.py**: Main Streamlit application script.
- **us_census/**: Directory containing PDF documents for Q&A.
- **venv/**: Virtual environment directory.
- **README.md**: Project documentation.
- **LICENSE**: License information.

## Dependencies

All dependencies are listed in the `requirements.txt` file. Key dependencies include:

- **Streamlit**: For building the web application interface.
- **LangChain**: For chaining language model calls and managing prompts.
- **LangChain-Groq**: Integration with GROQ for enhanced language model capabilities.
- **FAISS**: For efficient similarity search and vector storage.
- **Google Generative AI Embeddings**: For creating vector embeddings of documents.
- **PyPDF2 & pypdf**: For loading and processing PDF documents.
- **dotenv**: For managing environment variables securely.

## Environment Variables

Ensure that the following environment variables are set in your `.env` file:

- **GROQ_API_KEY**: Your GROQ API key.
- **GOOGLE_API_KEY**: Your Google API key.

Example `.env` file:

```env
GROQ_API_KEY="gsk_50W2pjGxioT0W7H09CGHWGdyb..."
GOOGLE_API_KEY="AIzaSyCBUl8J-cB4sEdB..."
```

**Security Note**: Never expose your API keys publicly. Always keep the `.env` file secure and exclude it from version control.

## Running the Application

1. **Activate Virtual Environment**

   ```bash
   source venv/bin/activate  # On Unix or MacOS
   # or
   venv\Scripts\activate     # On Windows
   ```

2. **Run Streamlit App**

   ```bash
   streamlit run app.py
   ```

3. **Access the App**

   Open your web browser and navigate to `http://localhost:8501` to interact with the application.

## Contributing

Contributions are welcome! Please follow these steps:

1. **Fork the Repository**

2. **Create a Feature Branch**

   ```bash
   git checkout -b feature/YourFeatureName
   ```

3. **Commit Your Changes**

   ```bash
   git commit -m "Add Your Feature"
   ```

4. **Push to the Branch**

   ```bash
   git push origin feature/YourFeatureName
   ```

5. **Open a Pull Request**


---

## Additional Notes

- **Performance Optimization**: The application uses Streamlit's caching mechanisms to optimize performance, especially during the embedding and vector store creation processes.
  
- **Error Handling**: Basic error handling is implemented to ensure the application runs smoothly even if certain operations fail.

- **Extensibility**: The application is modular, allowing for easy addition of new features or integration with other services.

If you encounter any issues or have suggestions for improvements, feel free to open an issue or submit a pull request!

---

*Happy Coding!*