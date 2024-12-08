# Chat-with-SQL

**ChatWithSql** is a Python-based utility that enables users to interact with SQL databases using natural language queries. It leverages LangChain's NLP capabilities and OpenAI's GPT-3.5-turbo model to provide seamless interaction with databases.

---

## Prerequisites

To use **ChatWithSql**, ensure you have the following installed:

- **Python**: Version 3.7 or later
- **Required Python Libraries**:
  - `langchain`
  - `openai`
  - `pymysql`
  - `python-dotenv`
- **OpenAI API Access**: A valid OpenAI API key
- **SQL Database**: MySQL database or any compatible SQL database

---

## Installation

1. **Install the required libraries**:

   ```bash
   pip install langchain openai pymysql python-dotenv
2. **Set up the environment variables**:

   - Create a `.env` file in your project directory if it doesn't already exist.
   - Add your OpenAI API key to the `.env` file:

     ```plaintext
     OPENAI_API_KEY=sk-xxxxxx
     ```

   Replace `sk-xxxxxx` with your actual OpenAI API key.

3. **Ensure your database is set up**:

   - Prepare your MySQL database and note down the following details:
     - Username
     - Password
     - Host address (e.g., `localhost`)
     - Database name
   - Ensure the database is accessible and contains the required tables for querying.

4. **Download the project** (if applicable):

   - Clone or download this repository to your local machine:

     ```bash
     git clone https://github.com/your-username/chat-with-sql.git
     cd chat-with-sql
     ```

5. **Run the script**:

   - Create a Python script to interact with the **ChatWithSql** class or modify the example script provided in this repository.
   - Replace the database credentials and API key with your actual details.

6. **Example Usage**:

   ```python
   from chat_with_sql import ChatWithSql

   # Initialize the ChatWithSql object with your database credentials
   chat_sql = ChatWithSql("root", "12345", "localhost", "your_database")

   # Send a natural language query
   response = chat_sql.message("How many rows are there in the cattle table?")
   print(response)
