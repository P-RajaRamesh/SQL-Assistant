# SQL-Assistant

Healthcare Database Request Assistant (HDBRA) is an AI-powered Streamlit application designed to assist healthcare professionals with database-level service requests that are not manageable via standard user interfaces. Built with LangChain, Gemini Pro (Google Generative AI), and FAISS, the app retrieves relevant SQL queries or stored procedures from a vector store based on the user’s natural language request.

Uploaded database operation documents are pre-processed, embedded using Hugging Face models, and indexed in FAISS for efficient retrieval. When a request is submitted, HDBRA searches the vector store for the most relevant examples, augments them with contextual information, and generates a professional response including the SQL solution, action type, affected tables, and explanation.

The assistant supports tasks like data updates, corrections, assignments, report generation, and integrity checks — all adhering to a predefined healthcare database schema. With a clean, interactive UI, it also offers request history tracking for audits.

Ideal for healthcare IT teams and DB admins, this tool bridges natural language queries with operational database management through retrieval-augmented generation (RAG).

---

🛠️ Installation

1. Clone the Repository:
```
git clone https://github.com/P-RajaRamesh/SQL-Assistant.git
cd SQL-Assistant
```

2. Create a Virtual Environment (Optional but recommended):
```
python -m venv venv
source venv/bin/activate
```

3. Install Dependencies:
```pip install -r requirements.txt```


4. Run the Application:
```streamlit run main.py```

---

📁 Project Structure
```
SQL-Assistant/
├── .devcontainer/           # Development container configurations
├── data/                    # Sample data and documents
├── faiss/
│   └── healthcare_index/    # FAISS index files
├── logo/                    # Project logos and images
├── src/                     # Source code modules
├── main.py                  # Entry point for the Streamlit app
├── requirements.txt         # Python dependencies
└── README.md                # Project documentation
```

---

🤖 Technologies Used

Streamlit: For building the interactive web interface.

LangChain: Framework for developing applications powered by language models.

Gemini Pro: Google's generative AI model for natural language understanding.

FAISS: Library for efficient similarity search and clustering of dense vectors.

Hugging Face Transformers: For embedding textual data into vector representations.
