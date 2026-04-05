# Product Explorer & Error-Resilient Logger (Python)

## 📌 Overview

This project demonstrates how to build a **robust, real-world Python application** that interacts with external APIs, processes data, handles failures gracefully, and logs errors for debugging and monitoring.

The system integrates:

* File handling (read/write/search)
* API data fetching and processing
* Exception handling
* Error logging with timestamps

---

## 🎯 Key Learning Outcomes

* File I/O operations using Python
* API integration using `requests`
* JSON parsing and data transformation
* Exception handling for fault-tolerant systems
* Logging errors with timestamps for debugging
* Input validation and user interaction loops

---

# 📄 Task 1 — File I/O Operations

### 🔍 Objective

Write, append, read, and search text data from a file.

### ⚙️ Features Implemented

* Created `python_notes.txt` using write mode (`'w'`)
* Appended additional content using append mode (`'a'`)
* Read file and printed numbered lines using `enumerate()`
* Counted total lines
* Implemented case-insensitive keyword search
* Built a continuous search loop with exit option

### 💡 Key Insight

Used `.lower()` for case-insensitive matching and `.strip()` for clean output formatting.

---

# 🌐 Task 2 — API Integration

### 🔍 Objective

Fetch and process product data from a public API.

### ⚙️ Features Implemented

#### ✔ Fetch Products

* Retrieved 20 products using:

```
https://dummyjson.com/products?limit=20
```

* Parsed JSON response into Python dictionaries
* Displayed formatted table with key fields

#### ✔ Filter & Sort

* Filtered products with rating ≥ 4.5
* Sorted results by price (descending)

#### ✔ Category-Based Fetch

* Retrieved laptops using:

```
https://dummyjson.com/products/category/laptops
```

#### ✔ POST Request

* Simulated product creation using POST API
* Printed response including generated product ID

### 💡 Key Insight

Distinction between:

* API data processing (client-side filtering)
* Server-side filtering via endpoints

---

# ⚠️ Task 3 — Exception Handling

### 🔍 Objective

Build fault-tolerant functions that handle errors gracefully.

### ⚙️ Features Implemented

#### ✔ Safe Calculator

* Handled:

  * `ZeroDivisionError`
  * `TypeError`

#### ✔ Safe File Reader

* Handled `FileNotFoundError`
* Used `finally` block to ensure execution completion message

#### ✔ Robust API Calls

* Wrapped API requests in try-except blocks
* Handled:

  * `ConnectionError`
  * `Timeout`
  * Generic exceptions

#### ✔ Input Validation Loop

* Validated user input before making API calls
* Prevented invalid requests
* Handled HTTP responses:

  * `200` → success
  * `404` → product not found

### 💡 Key Insight

Difference between:

* Python exceptions (network failures)
* HTTP status codes (server responses)

---

# 📝 Task 4 — Error Logging System

### 🔍 Objective

Log errors with timestamps for debugging and monitoring.

### ⚙️ Features Implemented

* Created `error_log.txt` in append mode
* Logged errors in format:

```
[YYYY-MM-DD HH:MM:SS] ERROR in function_name: ErrorType — message
```

#### ✔ Logged Scenarios

* Connection failure (invalid host)
* HTTP error (404 response)

#### ✔ Used Modules

```python id="n9g6c0"
from datetime import datetime
```

### 💡 Key Insight

HTTP errors are not exceptions — they must be handled using `response.status_code`.

---

# 🛠️ How to Run

### Install dependencies:

```
pip install requests
```

### Run individual modules:

```
part3_api_files.ipynb
```

# 🧠 Real-World Relevance

This project reflects workflows used in:

* Backend systems
* Data engineering pipelines
* API-driven applications
* Monitoring and logging systems

---

# 👩‍💻 Author

**Ekta Tiwari**

---

## 🌟 Final Note

This project demonstrates how Python can be used to build resilient, production-like applications that handle real-world data, external systems, and failure scenarios effectively.
