

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
  
  <h1 align="center">Natural Language to SQL Query Converter</h1>
  <p align="center">A robust system to translate natural language into SQL, powered by Azure OpenAI and Langchain.</p>
  
  <div align="center">
    <a href="#introduction">**Introduction**</a> | <a href="#goals">**Goals**</a> | <a href="#tech-stack">**Tech Stack**</a> | <a href="#quick-start">**Quick Start**</a> | <a href="#results">**Results**</a>
  </div>
</div>

---

## 🤖 Introduction

[cite_start]This project is dedicated to bridging the gap between human language and database query execution[cite: 5]. [cite_start]It's a system that seamlessly translates natural language queries into SQL queries and executes them with precision[cite: 8]. [cite_start]The primary objective is to empower users to interact with a database effortlessly using natural language queries[cite: 14].

<br>

<br>

---

## 🎯 Goals

The specific goals for this project are:
* [cite_start]**Convert Natural Language Queries:** Transform user queries into SQL queries to make database interaction intuitive[cite: 20].
* [cite_start]**Execute SQL Queries:** Execute the generated SQL queries on an SQLite database to ensure efficient data retrieval and manipulation[cite: 21].
* [cite_start]**Provide Accurate Results:** Deliver precise and meaningful results in response to user queries, which enhances the overall user experience[cite: 22].

---

## ⚙️ Tech Stack

* **Python:** The core programming language for the project.
* [cite_start]**Langchain (`v0.0.227+`):** The platform that leverages natural language processing capabilities to parse and translate queries[cite: 25].
* [cite_start]**Azure OpenAI:** Provides the language understanding and model deployment foundation for the project[cite: 12].
* [cite_start]**SQLite:** The database used for executing the generated SQL queries[cite: 21].

---

## 🤸 Quick Start

Follow these steps to set up and run the project locally on your machine.

**1. Clone the Repository & Prepare the Database**
```bash
git clone [https://github.com/your-username/Natural-Language-to-SQL-Query-Converter.git](https://github.com/your-username/Natural-Language-to-SQL-Query-Converter.git)
cd Natural-Language-to-SQL-Query-Converter
# Ensure you have your 'employees.db' file in the `data` folder
2. Install Dependencies

Bash

pip install -r requirements.txt

Note: This will install Langchain v0.0.227 and OpenAI v0.27.8 as required.

3. Set Up Azure OpenAI
Secure an API key from Azure services. Create a deployment model named "gpt-35-turbo" in Azure OpenAI Studio. Then, set your environment variables for seamless integration.



Python

import os
os.environ["OPENAI_API_TYPE"] = "azure"
os.environ["OPENAI_API_VERSION"] = "2023-05-15"
os.environ["OPENAI_API_BASE"] = "YOUR_AZURE_OPENAI_BASE_URL"
os.environ["OPENAI_API_KEY"] = "YOUR_AZURE_OPENAI_KEY"
4. Run the Project
You can run the code from your Jupyter Notebook (src/main_notebook.ipynb) or your Python script (src/main.py).

📈 Results
The system delivers two primary outputs: the generated SQL query and the result of its execution. This showcases the project's capability to accurately and transparently handle user queries.

Example 1: Counting Rows

> Entering new SQLDatabaseChain chain...
how many rows are there?
SQLQuery:SELECT COUNT(*) FROM documents;
SQLResult: [(50,)]
Answer:There are 50 rows in the documents table.
Example 2: Summing a Column

> Entering new SQLDatabaseChain chain...
how much is the total salary of all the employees?
SQLQuery:SELECT SUM("SALARY") FROM documents
SQLResult: [(309116,)]
Answer:The total salary of all the employees is 309116.