﻿# File-Monitoring
---

# 📂 File Monitoring using FastAPI

This project implements a **file monitoring system** using **FastAPI**, allowing users to track changes (creation, modification, deletion) in a specified directory through an API interface. It leverages Python's `watchdog` library for real-time monitoring and `FastAPI` for serving and interacting with the data.

## 🚀 Features

* 🕵️‍♂️ Real-time directory monitoring
* 📬 RESTful API to get monitored file events
* 🔁 Automatic update of file changes (create/modify/delete)
* 🧩 Modular and easy-to-extend code structure
* 🧪 Run and test directly from a Jupyter Notebook

## 🛠️ Technologies Used

* **Python 3.8+**
* **FastAPI**
* **Uvicorn**
* **watchdog**
* **Jupyter Notebook**

## 📁 Structure

```
.
├── File monitoring using FastAPI.ipynb   # Jupyter notebook with implementation
├── README.md                             # This file
```

## 📦 Installation

1. **Clone the repository:**

   ```bash
   git clone https://github.com/your-username/file-monitoring-fastapi.git
   cd file-monitoring-fastapi
   ```

2. **Create a virtual environment (optional but recommended):**

   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**

   ```bash
   pip install fastapi uvicorn watchdog
   ```

## ▶️ Running the App

Inside the notebook or from a separate `.py` script, run the FastAPI server using Uvicorn:

```bash
uvicorn main:app --reload
```

* The API will be available at: `http://127.0.0.1:8000`
* Swagger Docs: `http://127.0.0.1:8000/docs`

> Note: Replace `main` with the filename (without `.py`) if using a standalone script.

## 📬 Example API Endpoints

* `GET /events` – Get the list of recent file system events
* `POST /start-monitoring` – Start monitoring a directory
* `POST /stop-monitoring` – Stop monitoring

## ✅ Usage

You can test the API using:

* Swagger UI at `/docs`
* `curl` or `Postman`
* Python requests

Example using `curl`:

```bash
curl -X POST "http://127.0.0.1:8000/start-monitoring" -H "Content-Type: application/json" -d '{"path": "/your/folder/path"}'
```

## 🧠 Learning Objectives

* Learn how to use FastAPI for building RESTful services
* Understand how to use `watchdog` to monitor file system changes
* Combine asynchronous Python with real-time file operations

