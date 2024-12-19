# no-more-sql


### Project Purpose

No-More-SQL was built to simplify SQL generation for users with little to no SQL knowledge. The project empowers users to type natural language queries, such as "Show me the sales by region for 2023," and automatically generates accurate SQL code. By leveraging RAG (Retrieval-Augmented Generation) and LLama-based LLMs, the system combines past query examples with a powerful language model to produce reliable and optimized SQL code seamlessly. The UI is built using streamlit.

### Project Overview
No-More-SQL integrates retrieval-augmented generation (RAG) with LLama-based LLM to generate SQL queries dynamically:
1. **User Input:** The user provides a natural language query (e.g., "Find total revenue for last quarter").
2. **Retrieval:** The system searches a database of prior queries to retrieve the most relevant examples as context.
3. **Generation:** Using LLama-based models via Ollama, the system instructs the model to output clean SQL code using a structured prompt:
`You are an expert at writing SQL code. Based on the user query and the following examples, write the SQL code with no extra explanation. Just the code.`
4. **Output:** The generated SQL code is returned to the user without additional explanation, ensuring clarity and usability.


### Key Features:
1. Seamless conversion of natural language to SQL.
2. Retrieval of similar examples enhances accuracy using RAG.
3. Lightweight deployment using Ollama for LLama-based models.

### Instructions:
#### Setup
To set up and install dependencies for the project, follow these steps:
1. Clone the Repository
`git clone <repository-url>`
`cd no-more-sql`
2. Install Poetry
If you don't have Poetry installed, install it via pip:
`pip install poetry`

Verify the installation:
`poetry --version`
3. Install Dependencies
Run the following command to create a virtual environment and install the project dependencies:
`poetry install`
This will install all the dependencies listed in the pyproject.toml file, including both runtime and optional dependencies (if needed).

#### Running the Application
Once the setup is complete, you can run the application using Poetry To start the application, use:
`poetry run streamlit run code/main.py`
The command runs the Streamlit app located in code/main.py.

