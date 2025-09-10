<div align="center">
<br />

<br />
<div>
<img src="https://img.shields.io/badge/Python-black?style=for-the-badge&logoColor=white&logo=python&color=3776AB" alt="Python Badge" />
<img src="https://img.shields.io/badge/Azure_OpenAI-black?style=for-the-badge&logoColor=white&logo=openai&color=0078D4" alt="Azure OpenAI Badge" />
<img src="https://img.shields.io/badge/LangChain-black?style=for-the-badge&logoColor=white&logo=chainlink&color=007a82" alt="LangChain Badge" />
<img src="https://img.shields.io/badge/SQLite-black?style=for-the-badge&logoColor=white&logo=sqlite&color=003B57" alt="SQLite Badge" />
</div>
<br />

<h3 align="center">Natural Language to SQL Query Converter and Executor</h3>

<div align="center">
A project that seamlessly translates natural language queries into SQL, powered by Azure OpenAI and Langchain.
</div>
</div>

📋 Table of Contents
<a href="#introduction">🤖 Introduction</a>

<a href="#tech-stack">⚙️ Tech Stack</a>

<a href="#features">🔋 Features</a>

<a href="#quick-start">🤸 Quick Start</a>

<a href="#more">🚀 More</a>

🚨 Project Summary
This repository contains the full code for a project that creates a robust system to convert and execute SQL queries from natural language. It's an excellent showcase of integrating advanced AI services like Azure OpenAI with powerful frameworks like Langchain Agents to build a practical, real-world application. This project highlights a key skill: bridging the gap between human-readable language and machine-executable commands.

<br>

<br>

<a name="introduction">🤖 Introduction</a>
This project is a sophisticated system that translates natural language queries into executable SQL queries. The main goal is to allow users to interact with databases effortlessly, without needing to write complex SQL syntax. The system uses Azure OpenAI for its powerful language understanding and Langchain to orchestrate the translation and execution process. The result is a precise and reliable tool for database interaction.

<a name="tech-stack">⚙️ Tech Stack</a>
Python: The core programming language for the project.

Langchain: Used for orchestrating the natural language processing workflow.

Azure OpenAI: Provides the powerful language model for translating queries.

SQLite: The local database used for demonstrating and executing the generated SQL queries.

Jupyter Notebook: The primary environment for running and showcasing the project's code.

<a name="features">🔋 Features</a>
👉 Natural Language to SQL Conversion: Transforms user queries from plain English (e.g., "what is the total salary of employees?") into a valid SQL query.

👉 Efficient Query Execution: The system automatically executes the generated SQL query against a local SQLite database and returns the result.

👉 Accurate Results: Delivers both the generated SQL query and the final result, providing transparency and accuracy.

👉 Robust and Reusable Code: The project's structure is designed for clarity and easy reuse in other similar applications.

<a name="quick-start">🤸 Quick Start</a>
Follow these steps to set up and run the project locally on your machine.

Prerequisites

Make sure you have the following installed:

Python 3.x

Git

An Azure OpenAI subscription and an API key.

Cloning the Repository

First, clone the project from your Git repository:

Bash

git clone https://github.com/your-username/Natural-Language-to-SQL-Query-Converter.git
cd Natural-Language-to-SQL-Query-Converter
Installation

Install the required Python packages from the requirements.txt file.

Bash

pip install -r requirements.txt
Set Up Environment Variables

Create a .env file or set your environment variables directly for your Azure OpenAI credentials. This is crucial as it prevents you from exposing your API key in the code.

Python

import os
os.environ["OPENAI_API_TYPE"] = "azure"
os.environ["OPENAI_API_VERSION"] = "2023-05-15"
os.environ["OPENAI_API_BASE"] = "YOUR_AZURE_OPENAI_BASE_URL"
os.environ["OPENAI_API_KEY"] = "YOUR_AZURE_OPENAI_KEY"
Run the Project

You can run the code from your Jupyter Notebook (main_notebook.ipynb) or your Python script (main.py).

For Jupyter Notebook:

Bash

jupyter notebook src/main_notebook.ipynb
For a Python script:

Bash

python src/main.py
<a name="more">🚀 More</a>
Author

Your Name - Connect with me on LinkedIn!

Your GitHub Profile - Check out my other projects!