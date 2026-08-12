# CourseMate-AI
📚 RAG Book Assistant

A Retrieval-Augmented Generation (RAG) application built with Streamlit, LangChain, ChromaDB, OpenAI Embeddings, and Mistral AI. The application allows users to upload a PDF document, create a vector database from its contents, and ask natural language questions that are answered using only the uploaded document.

🚀 Features
Upload any PDF document
Extract and split document content into chunks
Generate embeddings using OpenAI Embeddings
Store embeddings in ChromaDB
Retrieve relevant document chunks using MMR (Maximal Marginal Relevance)
Answer questions using Mistral AI
Streamlit web interface for easy interaction
🛠️ Tech Stack
Python
Streamlit
LangChain
ChromaDB
OpenAI Embeddings
Mistral AI
python-dotenv
📂 Project Structure
RAG-Book-Assistant/
│
├── app.py                  # Streamlit application
├── careate_database.py      # CLI-based RAG question-answer interface
├── main.py                  # Sample Python file
├── chroma_db/               # Generated vector database
├── .env                     # API keys (not committed)
├── requirements.txt
└── README.md
⚙️ Installation
1. Clone the repository
git clone https://github.com/yourusername/rag-book-assistant.git
cd rag-book-assistant
2. Create a virtual environment
python -m venv venv

Activate it:

Windows

venv\\Scripts\\activate

macOS / Linux

source venv/bin/activate
3. Install dependencies
pip install -r requirements.txt
🔑 Environment Variables

Create a .env file in the project root and add:

OPENAI_API_KEY=your_openai_api_key
MISTRAL_API_KEY=your_mistral_api_key
▶️ Run the Application

Start the Streamlit app:

streamlit run app.py

Open the local URL shown in the terminal (usually http://localhost:8501).

📖 How It Works
Upload a PDF document.
Click Create Vector Database.
The document is:
Loaded using PyPDFLoader
Split into chunks
Converted into embeddings
Stored in ChromaDB
Ask a question in natural language.
The system retrieves relevant chunks and sends them to Mistral AI.
The AI generates an answer using only the retrieved document context.
💬 Example

Question

What is the main topic discussed in Chapter 2?

Answer

The application retrieves the relevant section from the uploaded PDF and generates a context-based response. If the answer is not present in the document, it responds:

I could not find the answer in the document.
📌 Retrieval Strategy

The project uses Maximal Marginal Relevance (MMR) retrieval with:

k = 4
fetch_k = 10
lambda_mult = 0.5

This helps return relevant yet diverse document chunks.

📸 Streamlit Interface
Upload PDF
Create Vector Database
Ask Questions
View AI-generated answers
🔮 Future Improvements
Support multiple PDFs
Chat history
Source citations with page numbers
Conversation memory
Local embedding models
Docker deployment
🤝 Contributing

Contributions are welcome. Feel free to fork the repository and submit a pull request.

📄 License

This project is licensed under the MIT License.

👨‍💻 Author

Smit Patel

Aspiring AI/ML Engineer | Data Science Enthusiast
