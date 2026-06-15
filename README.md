# 📚 SmartEval AI – AI-Based Student Project Evaluation System

SmartEval AI is an AI-powered platform that automates the evaluation of student project submissions by comparing them against faculty-provided assignment requirements. The system uses **Google Gemini AI** to analyze PDFs, generate detailed feedback, assign scores, and highlight strengths, weaknesses, and missing requirements.

---

# 🚀 Features

### 👨‍🏫 Faculty Module

* Faculty Login
* Create new assignments
* Upload assignment/task PDF
* Store assignment metadata
* Manage available assignments

### 👨‍🎓 Student Module

* Student Login & Registration
* Select assignment
* Upload project/report PDF
* Receive instant AI evaluation

### 🤖 AI Evaluation

* Reads faculty assignment PDF
* Reads student submission PDF
* Compares both documents
* Generates:

  * Requirement-wise checklist
  * Marks/Score
  * Strengths
  * Weaknesses
  * Missing Requirements
  * Suggestions for Improvement
  * Overall Feedback

If no assignment is selected, SmartEval AI performs a general evaluation of the uploaded project.

---

# 🛠️ Tech Stack

## Frontend

* HTML5
* CSS3
* JavaScript

## Backend

* Python
* Flask

## AI

* Google Gemini API

## Document Processing

* PyMuPDF (fitz)
* Pillow

## Database & Storage

* JSON
* Local File Storage

---

# 📂 Project Structure

```
SmartEval/
│
├── Backend/
│   ├── app.py
│   ├── requirements.txt
│   ├── START_BACKEND.bat
│   ├── start_backend.sh
│   ├── uploads/
│   ├── assignments/
│   └── reports/
│
└── Frontend/
    ├── index.html
    ├── login.html
    ├── signup.html
    ├── faculty-dashboard.html
    ├── student-dashboard.html
    ├── create-assignment.html
    ├── upload-test.html
    ├── script.js
    ├── style.css
    └── dashboard.css
```

---

# ⚙️ Prerequisites

Before running the project, install:

* Python 3.10+
* pip
* Google Gemini API Key
* Modern web browser (Chrome, Edge, Firefox)

---

# 🔑 Get Your Gemini API Key

1. Visit:

```
https://aistudio.google.com/app/apikey
```

2. Click **Create API Key**

3. Copy your API key (starts with `AIza...`)

---

# 📦 Installation

## Clone the Repository

```bash
git clone https://github.com/yourusername/SmartEval-AI.git

cd SmartEval-AI
```

---

## Install Dependencies

```bash
cd Backend

pip install -r requirements.txt
```

---

# ▶️ Running the Project

## Windows

Double-click:

```
Backend/START_BACKEND.bat
```

OR

```cmd
cd Backend

set GEMINI_API_KEY=YOUR_API_KEY

python app.py
```

---

## macOS / Linux

```bash
cd Backend

export GEMINI_API_KEY=YOUR_API_KEY

python app.py
```

---

If everything starts correctly, you'll see:

```
==================================================
 SmartEval AI Backend
 http://127.0.0.1:5000
==================================================
```

Keep this terminal running while using the application.

---

# 🌐 Launch the Frontend

Open:

```
Frontend/index.html
```

in your preferred web browser.

---

# 👨‍🏫 Faculty Workflow

1. Login as Faculty
2. Open Faculty Dashboard
3. Click **Create Assignment**
4. Enter assignment details
5. Upload assignment PDF
6. Save assignment

The assignment is now available for students.

---

# 👨‍🎓 Student Workflow

1. Login as Student
2. Open Student Dashboard
3. Select an assignment
4. Upload project/report PDF
5. Click **Evaluate**

The AI generates a complete evaluation report.

---

# 🤖 AI Evaluation Process

```
Faculty Assignment PDF
          │
          ▼
 Extract Assignment Requirements
          │
          │
Student Submission PDF
          │
          ▼
 Extract Student Content
          │
          ▼
 Google Gemini AI
          │
          ▼
 Requirement-wise Comparison
          │
          ▼
 Evaluation Report
```

The generated report includes:

* Overall Score
* Requirement Checklist
* Strengths
* Weaknesses
* Missing Sections
* Suggestions
* Final Feedback

---

# 📄 Evaluation Example

```
Assignment Requirement:
✔ Introduction Included

✔ Objectives Clearly Explained

✘ Missing Architecture Diagram

✔ Implementation Details

✘ Missing Output Screenshots

Overall Score:
85 / 100

Strengths:
• Well-structured report
• Clear explanation
• Good implementation

Weaknesses:
• Missing screenshots
• Incomplete conclusion

Suggestions:
• Add architecture diagram
• Include execution screenshots
• Expand conclusion
```

---

# 📁 Generated Files

The backend automatically creates the following folders:

```
uploads/
```

Stores uploaded student PDFs and extracted page images.

```
assignments/
```

Stores faculty assignment PDFs and metadata.

```
reports/
```

Stores generated evaluation reports in JSON format.

---

# 📌 API Endpoint

## Evaluate Project

```
POST /evaluate
```

Uploads:

* Student PDF
* Assignment PDF (optional)

Returns:

```json
{
    "score": 90,
    "strengths": [],
    "weaknesses": [],
    "feedback": "",
    "suggestions": []
}
```

---

# 🎯 Future Enhancements

* Admin Dashboard
* User Authentication with Database
* Cloud Storage Integration
* Plagiarism Detection
* Rubric-Based Evaluation
* OCR Support for Scanned PDFs
* Report Download (PDF)
* Email Evaluation Reports
* Analytics Dashboard
* Multi-file Project Evaluation

---

# 👩‍💻 Author

**Dakshayani Arza**

Computer Science Student

AI | Cloud Computing | AWS | Full Stack Development

GitHub: https://github.com/Dakshayani2005

---

# 📜 License

This project is developed for educational and academic purposes. You are free to modify and extend it for learning and research.

---
