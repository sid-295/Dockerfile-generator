 🐳 Dockerfile Generator

A simple **GenAI-powered tool** that generates **optimized Dockerfiles** based on your programming language input.\
This project uses **Ollama with the Llama3 model** to create Dockerfiles following best practices.

---

 📌 Requirements

 🛠 Install Ollama

1. Download and Install Ollama
   For Linux:

   ```sh
   curl -fsSL https://ollama.ai/install.sh | sh
   ```



2. Start the Ollama Service

   ```sh
   ollama serve
   ```

3. Download the Llama3 Model

   ```sh
   ollama pull llama3.2:1b
   ```

---

🚀 Setup & Usage

1️⃣ Create a Virtual Environment (Optional but Recommended)


python3 -m venv venv
source venv/bin/activate  # On Linux


2️⃣ Install Dependencies


pip install -r requirements.txt


3️⃣ Run the Script


python3 generate_dockerfile.py


**Example Input & Output:**

```
Enter the programming language: python

Generated Dockerfile:

FROM python:3.9-slim
WORKDIR /app
COPY requirements.txt .
RUN pip install -r requirements.txt
COPY . .
CMD ["python", "app.py"]
```

---

💡 How It Works

1. Takes a **programming language** as input (e.g., Python, Node.js, Java).
2. Uses **Ollama's Llama3 model** running locally to generate a **Dockerfile** with best practices.
3. Displays the optimized **Dockerfile** with necessary configurations.

---



