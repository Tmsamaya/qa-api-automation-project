# 🧪 Trello API Test Automation Project

## 📌 Overview

This project is a comprehensive API testing suite built using **Postman** and executed via **Newman (CLI)**. It demonstrates end-to-end testing of Trello’s core functionality, including board and card management, with a strong focus on structured validation and real-world QA practices. 

---

## 🚀 Key Features

* ✅ End-to-end **CRUD workflow testing**
* 🔁 **Dynamic variable chaining** across requests
* 🧪 Layered test validation strategy:

  * Structure validation
  * Schema validation
  * Data integrity checks
  * Business rule validation
* ❌ Robust **negative testing scenarios**
* ⚙️ CLI execution using **Newman**
* 📊 HTML reporting with **htmlextra reporter**

---

## 🔄 Test Workflow (Happy Path)

The primary workflow simulates a real user scenario:

1. Create Board
2. Create Lists (To Do / Done)
3. Create Card
4. Add Comment to Card
5. Update Card (description + move list)
6. Validate Card State
7. Delete Card
8. Confirm Card Deletion
9. Delete Board
10. Confirm Board Deletion

---

## ❌ Negative Testing Coverage

Includes scenarios such as:

* Missing / invalid API key
* Missing / invalid token
* Invalid resource IDs
* Missing required fields

These tests validate API robustness and proper error handling.

---

## 🧠 Test Strategy

Tests are structured in layered validation levels:

* **Structure**:
  Ensures required fields exist in the response.

* **Schema**:
  Validates data types and response shape.

* **Data Integrity**:
  Confirms returned values match expected inputs (e.g., variable chaining).

* **Business Rules**:
  Verifies functional behavior (e.g., card moves to correct list).

---

## 📸 Postman Execution (Visual Proof)

### ✅ Happy Path Workflow

![Happy Path](Screenshots/happy-path-get-request-1.png)

### ❌ Negative Testing Examples

![Negative Tests](Screenshots/negative-testing-invalid-id-1.png)  

![Negative Tests](Screenshots/negative-testing-invalid-id-2.png)  
(Shows an example of generating data to mimic ID's)

---

## ⚙️ Running Tests with Newman

### Prerequisites

* Node.js installed
* Newman installed:

```bash
npm install -g newman
```

### Run Collection

```bash
newman run "Trello API.postman_collection.json" -e "Trello Environment.postman_environment.json"
```

### Run with HTML Report

```bash
newman run "Trello API.postman_collection.json" -e "Trello Environment.postman_environment.json" -r htmlextra --reporter-htmlextra-export report.html
```

---

## 📊 Newman HTML Report

The collection can be executed via CLI using Newman, generating a detailed HTML report:

![Newman Summary](Screenshots/newman-summary.png)
![Request Breakdown](Screenshots/newman-request-breakdown.png)

---

## 🔐 Environment Configuration

This project uses environment variables for sensitive data:

* `trelloKey`
* `trelloToken`

⚠️ **Note:**
API credentials are not included. Replace placeholders in the environment file with your own values.

---

## 🛠️ Tech Stack

* Postman
* Newman
* JavaScript (Postman scripting)
* Trello REST API

---

## 💡 Highlights

* Demonstrates real-world QA workflow design
* Focus on maintainability and clarity
* Emphasis on both positive and negative testing
* CLI integration for automation readiness

---

## 👤 Author

Tomas Amaya
QA Engineer (6+ years experience)

---
