# AI Resume Analyzer (Semantic ATS)

An AI-powered Resume Analyzer that compares a candidate’s resume with a job description and calculates an **ATS (Applicant Tracking System) score** using **semantic skill matching** instead of simple keyword matching.

The system extracts skills from both the **resume** and **job description** using AI, compares them using **sentence embeddings**, and then generates insights such as **matched skills, missing skills, suggested projects, and an action plan**.

---

## 🚀 Features

* 📄 **Resume Parsing**

  * Upload resume in PDF format
  * Extracts structured text from resumes

* 🧠 **AI Skill Extraction**

  * Uses an LLM pipeline to extract professional skills from both resume and job description

* 🔎 **Semantic Skill Matching**

  * Uses sentence embeddings (`sentence-transformers`) to match skills semantically
  * Detects similar skills even if wording differs

* 📊 **ATS Score Calculation**

  * Calculates ATS compatibility score based on matched vs missing skills

* 💡 **Skill Gap Analysis**

  * Shows:

    * Matched Skills
    * Missing Skills

* 🧑‍💻 **AI Career Guidance**

  * Suggests:

    * Projects to build
    * Resume improvements
    * Action plan to improve ATS score

* 🖥 **Dashboard UI**

  * Clean white & blue interface
  * Displays analysis results clearly

---

## 🧱 Tech Stack

### Frontend

* Next.js
* React
* TypeScript
* TailwindCSS
* Axios

### Backend

* FastAPI
* Python

### AI / NLP

* Langflow
* OpenAI
* Sentence Transformers
* Cosine Similarity

### Other Tools

* PDF Parsing
* Semantic Embedding Matching

---

## ⚙️ System Architecture

Resume PDF
↓
Resume Text Extraction
↓
AI Skill Extraction
↓
JD Skill Extraction
↓
Semantic Skill Matching (Embeddings)
↓
Matched Skills / Missing Skills
↓
ATS Score Calculation
↓
AI Recommendations

---

## 📂 Project Structure

```
resume-analyzer/
│
├── backend/
│   ├── main.py
│   ├── analyse_resume.py
│   ├── ai_skill_extractor.py
│   ├── skill_matcher.py
│   ├── pdf_loader.py
│   └── langflow_client.py
│
├── frontend/
│   ├── app/
│   │   └── page.tsx
│   └── components/
│
├── requirements.txt
└── README.md
```

---

## 🛠 Installation

### 1️⃣ Clone the Repository

```
git clone https://github.com/YOUR_USERNAME/resume-analyzer.git
cd resume-analyzer
```

---

### 2️⃣ Backend Setup

```
cd backend
pip install -r requirements.txt
uvicorn main:app --reload
```

Backend runs on:

```
http://127.0.0.1:8000
```

---

### 3️⃣ Frontend Setup

```
cd frontend
npm install
npm run dev
```

Frontend runs on:

```
http://localhost:3000
```

---

## 📊 Example Output

ATS Score: **42%**

Matched Skills

* Python
* APIs
* Data Structures

Missing Skills

* React
* SQL
* AWS

Suggested Projects

* Build a REST API using Flask
* Deploy a Python application on AWS
