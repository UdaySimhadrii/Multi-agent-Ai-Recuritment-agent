# AI Recruiter Agency 🤖

An intelligent **Multi-Agent AI Recruitment System** built using **Python, Streamlit, and Google Gemini AI**.
The platform automates resume evaluation by extracting, analyzing, matching, screening, and recommending candidates using AI-powered agents.

---

## 📌 Features

* 📄 Resume PDF Parsing
* 🧠 AI-Powered Candidate Analysis
* 🎯 Intelligent Job Matching
* 🛡 HR Screening & Evaluation
* 💡 Final Hiring Recommendation
* 📊 Interactive Streamlit Dashboard
* ⚡ Multi-Agent Architecture
* 🤖 Powered by Google Gemini 1.5

---

# 📖 Table of Contents

* [Architecture](#-architecture)
* [Project Workflow](#-project-workflow)
* [Key Features](#-key-features)
* [Tech Stack](#-tech-stack)
* [Installation](#-installation)
* [Configuration](#-configuration)
* [Usage](#-usage)
* [Folder Structure](#-folder-structure)
* [Future Improvements](#-future-improvements)
* [License](#-license)

---

# 🏗 Architecture

The project follows a **Sequential Multi-Agent Architecture** managed by a central **Orchestrator Agent**.

Each agent performs a specialized task in the recruitment pipeline.

```text
                ┌────────────────────┐
                │   Streamlit UI     │
                └─────────┬──────────┘
                          │
                          ▼
                ┌────────────────────┐
                │  Orchestrator      │
                └─────────┬──────────┘
                          │
        ┌─────────────────┼─────────────────┐
        ▼                 ▼                 ▼
┌──────────────┐  ┌──────────────┐  ┌──────────────┐
│ Extractor    │  │ Analyzer     │  │ Matcher      │
│ Agent        │  │ Agent        │  │ Agent        │
└──────────────┘  └──────────────┘  └──────────────┘
                          │
                          ▼
                ┌────────────────────┐
                │ Screener Agent     │
                └─────────┬──────────┘
                          ▼
                ┌────────────────────┐
                │ Recommender Agent  │
                └────────────────────┘
```

---

# 🚀 Project Workflow

## 1️⃣ Extractor Agent

* Reads uploaded PDF resumes
* Extracts raw text using `pdfminer.six`

## 2️⃣ Analyzer Agent

Analyzes:

* Technical skills
* Education
* Experience
* Certifications
* Projects
* Domain expertise

## 3️⃣ Matcher Agent

Compares:

* Resume skills
* Job description
* Experience level

Generates:

* Match percentage
* Skill alignment score
* Domain compatibility

## 4️⃣ Screener Agent

Performs:

* HR-level screening
* Communication analysis
* Red-flag detection
* Missing skill detection
* Culture-fit estimation

## 5️⃣ Recommender Agent

Provides:

* ✔ Hire / ❌ No Hire decision
* Improvement suggestions
* Recommended roles

---

# ✨ Key Features

## 📄 PDF Resume Parsing

Uses **pdfminer.six** for accurate PDF text extraction.

## 🔍 Deep Skill Analysis

AI analyzes:

* Programming languages
* Frameworks
* Databases
* Cloud skills
* Experience level

## 🎯 Intelligent Job Matching

Compares resumes with job requirements and generates:

* Skill match %
* Experience score
* Relevance score

## 🛡 Automated HR Screening

Detects:

* Weak communication
* Missing skills
* Inconsistencies
* Red flags

## 💡 Final Recommendation

Provides:

* Final verdict
* Hiring confidence
* Suggested job roles

## 📊 Interactive Dashboard

Built with Streamlit for:

* Resume upload
* AI evaluation
* Visualization
* Candidate insights

---

# 🛠 Tech Stack

| Component    | Technology         |
| ------------ | ------------------ |
| Language     | Python 3.10+       |
| Frontend     | Streamlit          |
| AI Model     | Google Gemini 1.5  |
| PDF Parsing  | pdfminer.six       |
| Architecture | Multi-Agent System |

---

# ⚙ Installation

## 1️⃣ Clone Repository

```bash
git clone https://github.com/UdaySimhadrii/Multi-agent-Ai-Recuritment-agent.git
cd Multi-agent-Ai-Recuritment-agent
```

## 2️⃣ Create Virtual Environment

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

### Linux / Mac

```bash
python3 -m venv venv
source venv/bin/activate
```

## 3️⃣ Install Dependencies

```bash
pip install -r requirements.txt
```

---

# 🔑 Configuration

Open:

```bash
agents/base_agent.py
```

Find:

```python
HARDCODED_API_KEY = "YOUR_KEY_HERE"
```

Replace with your actual Gemini API key:

```python
HARDCODED_API_KEY = "AIzaSyXXXXXXXXXXXX"
```

---

# ▶ Usage

Run the Streamlit app:

```bash
streamlit run app.py
```

Open browser:

```text
http://localhost:8501
```

---

# 📂 Folder Structure

```text
AI-Recruiter-Agency/
│
├── agents/
│   ├── base_agent.py
│   ├── extractor_agent.py
│   ├── analyzer_agent.py
│   ├── matcher_agent.py
│   ├── screener_agent.py
│   └── recommender_agent.py
│
├── orchestrator/
│   └── orchestrator.py
│
├── utils/
│   └── pdf_parser.py
│
├── app.py
├── requirements.txt
└── README.md
```

---

# 📈 Example Output

```text
Candidate Name: John Doe

Skills:
✔ Python
✔ React
✔ Node.js
✔ MongoDB

Match Score: 87%

HR Screening:
✔ Strong communication
✔ Relevant projects
❌ Missing AWS experience

Final Recommendation:
✔ Hire
```

---

# 🔮 Future Improvements

* Multi-resume batch processing
* Resume ranking leaderboard
* Interview question generation
* ATS score generation
* LinkedIn profile analysis
* Voice interview AI agent
* Docker deployment
* Authentication system

---

# 🤝 Contributing

Contributions are welcome!

1. Fork the repository
2. Create a feature branch
3. Commit changes
4. Push to branch
5. Open Pull Request

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Tadaka Uday Simhadri**

* Python Developer
* AI Enthusiast
* MERN Stack Developer
* Cybersecurity Aspirant

---

# ⭐ Support

If you like this project:

⭐ Star the repository
🍴 Fork the project
📢 Share with others
