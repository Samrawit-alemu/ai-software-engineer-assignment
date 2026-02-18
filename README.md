# AI Experts Assignment 

This repository contains my submission for the AI Software Engineer Assignment (Python).

The project demonstrates:

* Reproducing and fixing a bug via tests
* Writing minimal, reviewable fixes
* Running tests locally and in Docker
* Dependency pinning for reproducibility

---

# Project Structure

```
.
├── app/                # Application source code
├── tests/              # Test suite
├── Dockerfile          # Docker configuration
├── requirements.txt   # Pinned dependencies
├── Explanation.md     # Bug analysis + fix explanation
└── README.md
```

---

# Local Setup & Run Instructions

## 1️ Clone the repository

```bash
git clone <your-repo-url>
cd ai-experts-assignment-3
```

---

## 2️ Create virtual environment

```bash
python -m venv venv
```

Activate it:

Windows (PowerShell)

```powershell
.\venv\Scripts\activate
```

Git Bash / Linux / Mac

```bash
source venv/Scripts/activate
```

---

## 3️ Install dependencies

```bash
pip install -r requirements.txt
```

---

## 4️ Run tests locally

```bash
pytest -v
```

# 🐳 Docker Instructions

## 1️ Build Docker image

```bash
docker build -t ai-assignment .
```

---

## 2️ Run tests in container

```bash
docker run --rm ai-assignment
```

Since the Dockerfile uses:

```
CMD ["pytest", "-v"]
```

tests run automatically.

---

