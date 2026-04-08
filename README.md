# Insurance_agent
Analyse the SecureLife Insurance Brokers dataset for medical costs and details of individuals and build a predictive model.
# 🧠 AI Insurance Claims Processing Agent (Groq + LangChain)

## 📌 Project Overview

This project is an **AI-powered Insurance Claims Processing System** built using:

* **LangChain** (Agent Framework)
* **Groq LLM (LLaMA 3.3 70B)**
* **Python**

👉 The system reads insurance claim documents and automatically:

1. 📄 Reads the claim file
2. 🔍 Extracts important details
3. ⚠️ Checks fraud rules
4. 🧠 Makes a decision (Approve / Escalate / Conditional)
5. 📑 Generates a final report

---

## 🎯 Use Case

This simulates how companies like **Chubb Insurance** process claims automatically using AI.

---

## ⚙️ Tech Stack

* Python 3.10+
* LangChain (Agent Framework)
* Groq API (LLM)
* PyPDF (for PDF reading)
* Regex (for data extraction)

---

## 📁 Project Structure

```
project/
│
├── sample_claims/        # Input claim files
│   ├── claim_001_fire.txt
│   ├── claim_002_theft.txt
│   └── claim_003_water.txt
│
├── reports/              # Generated reports
│
├── Agent_Ai.ipynb        # Main notebook
└── README.md
```

---

## 🚀 Step-by-Step Setup (VERY IMPORTANT)

### ✅ Step 1: Install Required Packages

Run this in your notebook:

```bash
pip install -U langchain==0.2.16 \
langchain-core==0.2.41 \
langchain-community==0.2.16 \
langchain-groq \
pypdf
```

---

### ✅ Step 2: Restart Runtime

👉 In Google Colab:

```
Runtime → Restart Runtime
```

---

### ✅ Step 3: Get Groq API Key

1. Go to: https://console.groq.com
2. Create API key
3. Copy it

---

### ✅ Step 4: Set API Key

```python
import os
os.environ["GROQ_API_KEY"] = "your_api_key_here"
```

---

## 🤖 AI Model Used

```python
model = "llama-3.3-70b-versatile"
```

✔ Best for reasoning
✔ High accuracy
✔ Works with agents

---

## 🛠️ Tools Used in Agent

| Tool                | Purpose                  |
| ------------------- | ------------------------ |
| ReadClaimDocument   | Reads TXT/PDF file       |
| ExtractClaimFields  | Extracts structured data |
| CheckPolicyRules    | Detects fraud & risk     |
| MakeClaimDecision   | Gives final decision     |
| GenerateClaimReport | Saves final report       |

---

## 🔄 Workflow

```
Read Document
     ↓
Extract Fields
     ↓
Check Rules
     ↓
Make Decision
     ↓
Generate Report
```

---

## 🧪 How to Run

```python
process_claim('sample_claims/claim_001_fire.txt')
```

---

## 📊 Sample Outputs

| File                | Expected Result |
| ------------------- | --------------- |
| claim_001_fire.txt  | ✅ APPROVED      |
| claim_002_theft.txt | ⚠️ ESCALATE     |
| claim_003_water.txt | 🔄 CONDITIONAL  |

---

## 🧠 Decision Logic

* **Low Risk (<30)** → ✅ APPROVE
* **Medium Risk (30–60)** → ⚠️ CONDITIONAL
* **High Risk (>60)** → 🚨 ESCALATE

---

## 📑 Output Example

```
FINAL CLAIM DECISION:
Decision: APPROVED FOR PROCESSING
Risk Score: 20/100
Next Steps:
1. Initiate payment
2. Notify customer
```

---

## ⚠️ Common Errors & Fixes

### ❌ Model Error

```
model not found
```

✅ Fix: Use

```python
llama-3.3-70b-versatile
```

---

### ❌ Import Error (AgentExecutor)

```
cannot import AgentExecutor
```

✅ Fix:

```python
from langchain.agents.agent import AgentExecutor
```

---

### ❌ API Key Error

```
authentication failed
```

✅ Fix: Ensure key starts with:

```
gsk_...
```

---

## 🔥 Features

✔ End-to-end automation
✔ Fraud detection logic
✔ Real-world simulation
✔ Report generation
✔ Works with TXT + PDF

---

## 🚀 Future Improvements

* Streamlit UI
* Database integration
* Real-time API deployment
* Advanced ML fraud detection

---

## 👨‍💻 Author

**Rahul Naidu**
AI / Data Science Enthusiast

---

## ⭐ Final Note

This project is **resume-ready** and demonstrates:

* AI Agents
* LLM Integration
* Real-world problem solving

---

👉 If you understand this project, you are already ahead of 90% beginners.

