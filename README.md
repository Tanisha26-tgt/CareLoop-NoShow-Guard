# CareLoop Clinics - NoShowGuard 🩺

Welcome to the **CareLoop Clinics - NoShowGuard** project repository! This project builds an end-to-end data pipeline, predictive model, and GenAI-powered insight extractor to analyze patient appointments, reduce clinic no-shows, and process follow-up notes.

---

## 📂 Project Structure & File Guide

* **`README.md`** – Project overview, architecture, and execution guide.
* **`data/`** – Contains raw datasets:
  * `appointments.csv` – Raw appointment transaction records.
  * `clinics.csv` – Clinic metadata and regional details.
  * `followup_notes.csv` – Call-centre follow-up transcripts and notes.
* **`load_data.sql`** – SQL script for setting up database tables and loading raw datasets into MySQL.
* **`02_queries.sql`** – Consolidated analytical queries (Tasks 2.1 to 2.5) along with database constraint error documentation.
* **`01_ingest_clean.ipynb`** – Data ingestion, data type casting, and cleaning pipeline.
* **`03_model.ipynb`** – Predictive modeling and risk scoring for patient no-shows.
* **`04_genai.ipynb`** – Gemini API integration, prompt engineering, and structured validation using Pydantic.
* **Processed Outputs:**
  * `appointments_clean.csv` – Cleaned master appointment records.
  * `clinics_enriched.csv` – Enriched clinic performance metrics.
  * `test_risk_scores.csv` – Model risk predictions for test data.
  * `notes_analysed.csv` – Extracted insights from call-centre notes.
  * `rejected_rows.json` – Log of validation errors and rejected records.

---

## ⚙️ Technical Workflow & Implementation

1. **Data Ingestion & Cleaning:** Raw CSV files are ingested, validated, and cleaned to handle missing values and formatting inconsistencies.
2. **Relational Database Management (SQL):** Tables are created via `load_data.sql`, and complex aggregations, window functions (`RANK()`), and conditional analysis are executed in `02_queries.sql`.
3. **Machine Learning & Risk Scoring:** Patient attendance behavior is analyzed to build risk assessment profiles.
4. **Generative AI Integration:** Unstructured follow-up notes are processed using Gemini API prompts, structured via Pydantic schemas, and cross-tabulated against clean appointment data.

---

## 🚀 How to Run the Project

1. **Clone the Repository:**
   ```bash
   git clone [https://github.com/Tanisha26-tgt/CareLoop-NoShow-Guard.git](https://github.com/Tanisha26-tgt/CareLoop-NoShow-Guard.git)
