# 🩺 Physician Notetaker: Clinical NLP Pipeline

Welcome to the Physician Notetaker project! This repository contains an AI-powered system designed to assist healthcare professionals by transcribing and structuring patient-physician dialogues. It leverages state-of-the-art NLP models to extract medical entities, analyze patient sentiment, and generate professional SOAP notes automatically.

## 🚀 Overview
The goal of this project is to reduce the administrative burden on doctors. By taking raw conversation transcripts, the system identifies key clinical data points, providing a structured summary that is ready for Electronic Health Record (EHR) integration.

## ✨ Key Features
- **Medical Named Entity Recognition (NER):** Uses scispaCy (a medical-grade NLP library) to detect symptoms, diagnoses, and treatment plans.
- **Sentiment & Intent Analysis:** Utilizes a DistilBERT transformer to distinguish between a patient's anxiety and their reassurance during a consultation.
- **Automated SOAP Note Generation:** Automatically maps the conversation into the industry-standard Subjective, Objective, Assessment, and Plan format.

## 🛠️ Tech Stack
- **Language:** Python 3.9+
- **Environment:** Google Colab
- **Core AI Libraries:**
  - spaCy & scispaCy (Medical NER)
  - Hugging Face Transformers (Sentiment Analysis)
- **Data Format:** JSON (for easy API integration)

## 📥 Getting Started
### 1. Setup in Google Colab
Since this project requires specific medical models, follow these steps to set up your environment:
1. Open the `.ipynb` file in Google Colab.
2. Run the Setup Cell to install `scispacy` and the `en_core_sci_md` model.
3. Crucial: Go to **Runtime -> Restart session** to avoid NumPy version conflicts.

### 2. Running the Pipeline
Simply paste your transcript into the provided variable and run the cells. The system will automatically output three distinct JSON objects for:
- Summarization
- Sentiment
- SOAP Note

## 📊 Sample Output
The system transforms raw text into a clean, structured JSON format:

```json
{
  "Patient_Name": "Janet Jones",
  "Symptoms": ["Neck pain", "Back pain", "Head impact"],
  "Diagnosis": "Whiplash injury",
  "Treatment": ["10 physiotherapy sessions", "Painkillers"],
  "Current_Status": "Occasional backache",
  "Prognosis": "Full recovery expected within six months"
}
```

## 🧠 Lessons Learned
During the development of this project, I encountered challenges with dependency management (specifically NumPy binary compatibility). Solving this taught me the importance of environment isolation and version pinning in Machine Learning workflows.

## 👤 Author
**Yashovardhan Tiwari** - Initial Work - [codezeewrangler](https://github.com/codezeewrangler)
