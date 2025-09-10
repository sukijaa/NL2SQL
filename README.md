<div align="center">
  <br />
  <img src="https://github.com/user-attachments/assets/e0b6d2e6-f5a3-4a1e-8f25-3037e20b3a4a" alt="Project Banner" width="800">
  <br />

  <div>
    <img src="https://img.shields.io/badge/Python-black?style=for-the-badge&logoColor=white&logo=python&color=3776AB" alt="Python Badge" />
    <img src="https://img.shields.io/badge/Azure_OpenAI-black?style=for-the-badge&logoColor=white&logo=openai&color=0078D4" alt="Azure OpenAI Badge" />
    <img src="https://img.shields.io/badge/LangChain-black?style=for-the-badge&logoColor=white&logo=chainlink&color=007a82" alt="LangChain Badge" />
    <img src="https://img.shields.io/badge/SQLite-black?style=for-the-badge&logoColor=white&logo=sqlite&color=003B57" alt="SQLite Badge" />
  </div>

  <h1 align="center">Natural Language to SQL Query Converter</h1>
  <p align="center">A robust system to translate natural language into SQL, powered by Azure OpenAI and LangChain.</p>

</div>

---

## 📋 <a name="table">Table of Contents</a>

1. 🤖 [Introduction](#introduction)
2. ⚙️ [Tech Stack](#tech-stack)
3. 🔋 [Features](#features)
4. 🤸 [Quick Start](#quick-start)
5. 📈 [How It Works](#how-it-works)

---

## <a name="introduction">🤖 Introduction</a>

This project is dedicated to bridging the gap between human language and database interaction. It's a powerful system that seamlessly translates natural language questions into SQL queries and executes them with precision. The primary objective is to empower users to interact with databases effortlessly, without needing to write a single line of SQL. The system is powered by **Azure OpenAI** services and **LangChain Agents** to deliver an intuitive and intelligent data querying experience.

---

## <a name="tech-stack">⚙️ Tech Stack</a>

* **Python**: The core programming language for the project.
* **LangChain**: The framework used for its powerful natural language processing capabilities and agent-based architecture.
* **Azure OpenAI**: Provides the foundational LLMs for language understanding and SQL generation.
* **SQLite**: The local database used for storing data and executing the generated SQL queries.

---

## <a name="features">🔋 Features</a>

👉 **Intuitive Querying**: Transform plain English questions into complex SQL queries, making database interaction accessible to everyone.

👉 **Automated Execution**: Seamlessly execute the generated SQL queries on an SQLite database for efficient data retrieval.

👉 **Accurate Results**: Deliver precise and meaningful answers in response to user queries, enhancing the overall user experience.

👉 **Transparent Process**: View the exact SQL query generated from your natural language input, providing insight into the translation process.

---

## <a name="quick-start">🤸 Quick Start</a>

Follow these steps to set up and run the project locally on your machine.

### Prerequisites

Make sure you have the following installed on your machine:
* [Git](https://git-scm.com/)
* [Python](https://www.python.org/downloads/)
* [pip](https://pip.pypa.io/en/stable/installation/) (Python Package Installer)

### 1. Clone the Repository

First, clone the project from your Git repository. Ensure you have your `employees.db` file in the `data` folder.
```bash
git clone [https://github.com/your-username/Natural-Language-to-SQL-Query-Converter.git](https://github.com/your-username/Natural-Language-to-SQL-Query-Converter.git)
cd Natural-Language-to-SQL-Query-Converter
'''
2. Install Dependencies
Install the required Python packages from the requirements.txt file.

Bash

pip install -r requirements.txt
Note: This will install LangChain v0.0.227 and OpenAI v0.27.8 as required.

3. Set Up Azure OpenAI Environment Variables
Secure an API key from Azure services to enable seamless integration. Create a deployment model named "gpt-35-turbo" in Azure OpenAI Studio. Then, set your environment variables for seamless integration.

You can set these in your terminal or directly within your Python script:

Python

import os

os.environ["OPENAI_API_TYPE"] = "azure"
os.environ["OPENAI_API_VERSION"] = "2023-05-15"
os.environ["OPENAI_API_BASE"] = "YOUR_AZURE_OPENAI_BASE_URL"
os.environ["OPENAI_API_KEY"] = "YOUR_AZURE_OPENAI_KEY"
Replace the placeholder values with your actual Azure OpenAI credentials.

4. Running the Project
You can run the code from your Jupyter Notebook (src/main_notebook.ipynb) or your Python script (src/main.py).

<a name="how-it-works">📈 How It Works</a>
The system delivers two primary outputs: the generated SQL Query and the final Answer, showcasing its ability to accurately and transparently handle user queries.

Example 1: Counting Rows

When you run the LangChain agent with a natural language input like "how many rows are there?", the system generates and executes the corresponding SQL query.

> Entering new SQLDatabaseChain chain...
how many rows are there?

SQLQuery: SELECT COUNT(*) FROM documents;
SQLResult: [(50,)]
Answer: There are 50 rows in the documents table.
Example 2: Summing a Column

The system can also handle more complex queries, like calculating the total salary of all employees.

> Entering new SQLDatabaseChain chain...
how much is the total salary of all the employees?

SQLQuery: SELECT SUM("SALARY") FROM documents
SQLResult: [(309116,)]
Answer: The total salary of all the employees is 309116.