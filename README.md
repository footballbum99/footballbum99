## Hi there 👋

<!--
**footballbum99/footballbum99** is a ✨ _special_ ✨ repository because its `README.md` (this file) appears on your GitHub profile.

Metro Payroll Analytics — Automated Data Pipeline & Streamlit Dashboard
An end‑to‑end Python application that automates payroll data collection, cleans and structures financial datasets, and delivers an interactive analytics dashboard for exploring employee compensation across branches, job classes, and fiscal years.
This project combines web automation, data engineering, and interactive visualization into a single, reproducible workflow.

Project Overview
This application:
Automatically downloads payroll CSV files from a dynamic website using Selenium
Cleans and normalizes financial fields (Regular Pay, Overtime, Bonuses, etc.)
Derives new metrics such as Total Pay and Extra Pay
Allows users to explore data by single year or multi‑year comparison
Provides drill‑down navigation from Branch → Job Class → Employee
Displays interactive tables, metrics, and filters through Streamlit
The result is a powerful tool for analyzing compensation trends across a large public workforce.

Tech Stack:
Python 3.x
Selenium — automated CSV download
pandas — data cleaning, type fixing, aggregation
Streamlit — multi‑tab dashboard with drill‑down navigation
Session State — persistent UI navigation
 WebDriver


Key Features
Automated Data Cleaning & Type Fixing
The app standardizes all pay columns using a custom clean_currency() function and ensures numeric consistency across fiscal year
Derived Financial Metrics
Total Pay = sum of all pay categories
Extra Pay = Total Pay − Regular Pay − Overtime Pay
Multi‑Year Analysis
Users can toggle between:
Single Year View
Multi‑Year Comparison View
The UI dynamically adjusts labels and summaries based on selection.
Multi‑Level Drill‑Down Navigation
The dashboard supports hierarchical exploration
Branch → Employee Roster → Employee History
This is powered by Streamlit’s session_state and row‑selection events.
Rich, Multi‑Tab Dashboard
Summary & Breakdown — KPIs and pay category totals
Branch Breakdown — drill‑down into branches and employees
Job Class Breakdown — filter by branch and explore job types
Highest Paid Employees — Total Pay ≥ $120K
Most Overtime — OT ≥ $30K
Most Extra Pay — Extra Pay ≥ $30K
Raw Data Explorer — name search + pay range slider

Architecture
Selenium Scraper
      ↓
Raw CSV Files
      ↓
pandas Cleaning & Transformation
      ↓
Derived Metrics (Total Pay, Extra Pay)
      ↓
Streamlit Dashboard (7 Tabs + Drill‑Down Navigation)

Project Structure
├── scrape.py              # Selenium automation for CSV download
├── app.py                 # Streamlit dashboard (main UI)
├── utils/                 # Helper functions (clean_currency, loaders, etc.)
├── data/                  # Raw downloaded CSVs
├── processed/             # Cleaned datasets
├── requirements.txt
└── README.md
Running the App
python scrape.py
streamlit run app.py
Dashboard Preview
Future Enhancements
Automated scheduling (cron, Task Scheduler)
Database backend (PostgreSQL / SQLite)
Docker containerization
Cloud deployment (Streamlit Cloud, Azure App Service)
API layer for external consumption
