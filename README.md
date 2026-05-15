<div align="center">

# 🏥 MediSense Pro
### AI-Powered Multi-Disease Diagnosis & Health Management Platform

[![Python](https://img.shields.io/badge/Python-3.10+-blue?style=for-the-badge&logo=python)](https://python.org)
[![Streamlit](https://img.shields.io/badge/Streamlit-1.28+-FF4B4B?style=for-the-badge&logo=streamlit)](https://streamlit.io)
[![scikit-learn](https://img.shields.io/badge/scikit--learn-1.4.2-F7931E?style=for-the-badge&logo=scikit-learn)](https://scikit-learn.org)
[![License: MIT](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

**VIT Capstone Project · SWE1904 · R. Divya (21MIS0261)**  
*Guide: Prof. Benjula Anbu Malar M B*

[🚀 Live Demo](#) · [📽️ Demo Video](#) · [📄 Report](#)

</div>

---

## 🧠 What is MediSense Pro?

MediSense Pro is a full-stack AI health platform that helps users **screen for 5 major diseases**, chat with an AI doctor, analyse health trends, and manage their family's medical records — all in one app.

Built with real ML models trained on clinical datasets, integrated with **Groq's LLaMA 3.3 70B** for conversational AI and **Google Gemini Vision** for photo-based symptom analysis.

---

## ✨ Features

| Module | Description | AI/ML Used |
|---|---|---|
| 🩸 **Diabetes Screener** | Home + clinical ML prediction with glucose trends | Random Forest |
| ❤️ **Heart Disease** | Emergency triage + Cleveland dataset ML model | Logistic Regression |
| 🧠 **Parkinson's** | Voice analysis + symptom screener + clinical ML | SVM |
| 🫘 **Kidney Disease** | CKD-EPI eGFR calculator + symptom screener | Rule-based |
| 🦋 **Thyroid** | Hypo vs Hyperthyroid screener + TSH interpreter | Rule-based |
| 🤖 **AI Doctor Chat** | Real-time consultation (Llama 3.3 70B via Groq) | LLM |
| 📸 **Visual Diagnosis** | Photo symptom analysis | Gemini Vision |
| 📊 **Health Analytics** | Trend charts, risk scores, history | — |
| 👨‍👩‍👧 **Family Vault** | Multi-member health profile management | — |
| 💊 **Medicine Reminder** | Drug schedule + interaction checker | — |
| 🏥 **Hospital Locator** | Nearest hospitals by city & speciality | — |
| 📄 **Prescription Card** | Printable PDF referral generator | ReportLab |
| 🔬 **General Diagnosis** | Symptom-based differential diagnosis engine | Rule-based NLP |
| ⚖️ **BMI Calculator** | BMI + body composition analyser | — |

---

## 🛠️ Tech Stack

```
Frontend    →  Streamlit (multi-page app, custom CSS)
ML Models   →  scikit-learn (Random Forest, SVM, Logistic Regression)
Generative  →  Groq API (LLaMA 3.3 70B) · Google Gemini Vision API
Database    →  SQLite (via custom ORM in utils/database.py)
PDF         →  ReportLab
Language    →  Python 3.10+
```

---

## 📁 Project Structure

```
medisense_pro/
├── app.py                    # Main app · auth · navigation
├── config.py                 # Project metadata
├── requirements.txt
├── train_models_complete.py  # Model training script
├── .streamlit/
│   └── config.toml           # Streamlit theme config
├── pages/                    # One file per feature
│   ├── diabetes.py
│   ├── heart.py
│   ├── parkinsons.py
│   ├── kidney.py
│   ├── thyroid.py
│   ├── ai_chat.py
│   ├── photo_diagnosis.py
│   ├── analytics.py
│   ├── dashboard.py
│   ├── family_vault.py
│   ├── medicine_reminder.py
│   ├── hospital_locator.py
│   ├── prescription.py
│   ├── health_report_card.py
│   └── ...
├── utils/
│   ├── database.py           # SQLite CRUD layer
│   └── diagnosis_engine.py   # Rule-based engine
├── models/                   # Trained ML models (.sav)
└── datasets/                 # Clinical training datasets (CSV)
```

---

## ⚙️ Run Locally

### 1. Clone the repo
```bash
git clone https://github.com/YOUR_USERNAME/MediSense-Pro.git
cd MediSense-Pro
```

### 2. Install dependencies
```bash
pip install -r requirements.txt
```

### 3. Add your API keys
Create `.streamlit/secrets.toml`:
```toml
GROQ_KEY   = "your-groq-api-key"
GEMINI_KEY = "your-gemini-api-key"
```
> ⚠️ `secrets.toml` is in `.gitignore` — it will never be committed.

Get free keys here:
- Groq: https://console.groq.com
- Gemini: https://aistudio.google.com/app/apikey

### 4. Run the app
```bash
streamlit run app.py
```

### Demo Login
| Role | Username | Password |
|---|---|---|
| Patient | `demo` | `demo123` |
| Doctor | `doctor` | `doc123` |

---

## 🤖 ML Models

| Disease | Dataset | Algorithm | Accuracy |
|---|---|---|---|
| Diabetes | Pima Indians Dataset | Random Forest | ~78% |
| Heart Disease | Cleveland Heart Dataset | Logistic Regression | ~85% |
| Parkinson's | UCI Parkinson's Dataset | SVM | ~90% |

> Models are pre-trained and stored in `/models`. Re-train with `python train_models_complete.py`.

---

## ☁️ Deploy on Streamlit Cloud (Free)

1. Push this repo to GitHub
2. Go to [share.streamlit.io](https://share.streamlit.io) and connect your GitHub
3. Select `app.py` as the entry point
4. Add `GROQ_KEY` and `GEMINI_KEY` in the **Secrets** tab
5. Click **Deploy** — your app is live! 🎉

---

## 👩‍💻 Author

**R. Divya** · 21MIS0261  
B.Tech Software Engineering · VIT University  
Capstone Project — SWE1904  
Guide: Prof. Benjula Anbu Malar M B

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat&logo=linkedin)](https://linkedin.com/in/YOUR_PROFILE)
[![GitHub](https://img.shields.io/badge/GitHub-Follow-181717?style=flat&logo=github)](https://github.com/YOUR_USERNAME)

---

## 📄 License

This project is licensed under the MIT License — see [LICENSE](LICENSE) for details.
