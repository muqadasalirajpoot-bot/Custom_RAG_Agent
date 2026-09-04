# ChatGPT + LangChain Frontend

This project adds a Streamlit frontend to the LangChain backend supplied in `projects.ipynb`.

## Main behavior

1. The app opens on an API-key gate.
2. The user must enter an OpenAI API key.
3. The key is validated before the chatbot interface is shown.
4. An invalid key keeps the user on the API-key screen.
5. A valid key opens the chat interface.
6. The backend flow remains:
   `ChatPromptTemplate → ChatOpenAI → StrOutputParser`
7. The API key is supplied to `ChatOpenAI` at runtime instead of being hard-coded.

## Run locally

```bash
pip install -r requirements.txt
streamlit run app.py
```

Then open the local Streamlit URL shown in the terminal.

## Important security note

Do not put a real API key in `app.py`, `.env`, `.env.example`, GitHub, screenshots, or any public repository.

The key is kept in Streamlit session state for the current app session and is not written to a project file by this code.
