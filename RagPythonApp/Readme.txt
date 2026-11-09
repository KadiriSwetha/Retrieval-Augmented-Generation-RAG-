## Steps to Run the Project Manually

Step 1: Create a virtual environment

```
python -m venv .venv
```

Step 2: Activate the virtual environment

```
.venv\Scripts\activate
```

Step 3: Install dependencies

```
pip install -e .
```

Step 4: Start Ollama

Open Terminal 1:

```
ollama serve
```

Step 5: Start FastAPI Backend

Open Terminal 2:

```
.venv\Scripts\activate
uvicorn main:app --reload --port 8000
```

Step 6: Start Inngest Dev Server

Open Terminal 3:

```
npx inngest-cli@latest dev --no-discovery --poll-interval 30 -u http://127.0.0.1:8000/api/inngest
```

Step 7: Start Streamlit Frontend

Open Terminal 4:

```
.venv\Scripts\activate
streamlit run streamlit_app.py
```

Step 8: Access the Application

Open your browser:

```
http://localhost:8501
```

Step 9: Use the Application

1. Upload a PDF document.
2. Wait for document processing.
3. Enter a question related to the PDF.
4. Submit your question.
5. View the generated answer.

Note: Keep all four terminals running while using the application.