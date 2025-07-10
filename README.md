# 🕵️‍♂️ Agent-Based Text-to-SQL Integrated Application (Secured with Vulnerability Detection Tools)

This repository contains an **agent-based NLQ to SQL pipeline** that transforms user queries into SQL statements, while rigorously checking for security vulnerabilities at both the prompt and query level. It is fully integrated into a python notebook and uses modern LLM-based tools and validation agents.

---

## 🚀 Features

- 🔍 **LLM-Powered Text-to-SQL**: Translates natural language into SQL using advanced language models.
- 🧠 **Agent-Based Architecture**: Modular components handle prompt analysis, query generation, and vulnerability checks.
- 🛡️ **Double-Layer Security**: Both natural language inputs and generated SQL queries are screened for threats.
- ☁️ **Notebook Ready**: Quick, browser-based execution with no local setup required.
- 📦 **Requirements File**: All dependencies are managed through `requirements.txt`.


---

## 🧠 How the Agent System Works

The application employs a multi-agent pipeline to ensure both **functionality** and **security**.

### 🔄 Workflow

1. **🔤 Natural Language Input (NLQ)**  
   User submits a plain English question (e.g., _"Show total sales for 2023"_).

2. **🧪 Prompt Safety Agent**  
   - The question is passed to a **Text-to-SQL Prompt Detection Tool**.
   - It checks for **malicious input patterns**, **prompt injections**, or **suspicious keywords**.
   - ✅ If **safe**, proceed to next step.
   - ❌ If **unsafe**, block and notify user.

3. **🧠 Text-to-SQL Agent**  
   - A language model generates a SQL query from the validated input.

4. **🛡️ SQL Vulnerability Detection Agent**  
   - The generated SQL is checked for:
     - SQL Injection attempts
     - Destructive statements (`DROP`, `DELETE`, `UPDATE`)
     - Unauthorized access patterns

5. **✅ Final Execution Decision**  
   - ✅ If all checks pass → query is executed.
   - ❌ If flagged → execution is denied with an alert.

### ⚙️ Summary Flow


[Agents-based-architecture.pdf](https://github.com/user-attachments/files/21167944/Agents-based-architecture.pdf)
