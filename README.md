SOC CTI Threat Intelligence Dashboard

A Security Operations Center (SOC) Cyber Threat Intelligence Dashboard built using Flask, MongoDB, and JavaScript.
The system allows analysts to collect, enrich, prioritize, and visualize threat indicators (IP addresses) in real time.

This project simulates a mini CTI / SIEM-style platform used by SOC teams to track malicious infrastructure.

Project Overview

The dashboard provides analysts with:

Threat ingestion

Threat enrichment

Risk scoring

MITRE ATT&CK mapping

Threat prioritization

Visual analytics

Investigation tools

The system is designed to mimic real SOC threat intelligence workflows.

Architecture
Frontend (HTML + JS + Chart.js)
        │
        ▼
Flask Backend API
        │
        ▼
Threat Intelligence Engine
        │
        ▼
MongoDB Database
        │
        ▼
External Threat Intelligence APIs
(AbuseIPDB / GeoIP)
Features
Threat Management

Add threat indicators (IP addresses)

Delete threat records

Search threat indicators

Prevent duplicate threats

Threat Intelligence Engine

Automatic severity calculation

Risk score calculation

Threat aging (auto inactive after 30 days)

Duplicate threat update

MITRE ATT&CK technique mapping

Threat Enrichment

Each threat is enriched with external intelligence data:

Country

ISP / ASN

AbuseIPDB reputation score

Threat confidence score

SOC Analytics Dashboard

The dashboard includes visual intelligence components:

Severity counters

Threat distribution pie chart

Confidence score bar chart

Threat timeline analysis

Top critical threats panel

Analyst Tools

SOC analysts can:

Filter threats by severity

Search indicators

Export threat dataset to CSV

View threat enrichment data

Monitor risk scores

Risk Scoring Engine

Risk score is calculated using:

Risk Score = Confidence Score × Severity Weight

Severity weights:

Severity	Weight
High	1.5
Medium	1.2
Low	1.0

Higher risk scores indicate higher priority threats.

MITRE ATT&CK Integration

Threat types are mapped to MITRE ATT&CK techniques.

Example mapping:

Threat Type	Technique	Description
C2 Server	T1071	Application Layer Protocol
Botnet	T1095	Non-Application Layer Protocol
Phishing	T1566	Phishing

This helps analysts understand attacker behavior and tactics.

Technologies Used

Backend

Python

Flask

Flask-CORS

MongoDB

PyMongo

Requests

Frontend

HTML5

CSS3

JavaScript

Chart.js

Threat Intelligence

AbuseIPDB API

GeoIP enrichment

Project Structure
cti-dashboard/
│
├── app.py                # Flask backend API
├── index.html            # Dashboard frontend
├── requirements.txt      # Python dependencies
├── README.md             # Project documentation
│
└── venv/                 # Python virtual environment
Installation
1. Clone Repository
git clone https://github.com/yourusername/cti-dashboard.git
cd cti-dashboard
2. Create Virtual Environment
python -m venv venv

Activate:

Windows

venv\Scripts\activate

Linux / Mac

source venv/bin/activate
3. Install Dependencies
pip install -r requirements.txt
4. Start MongoDB

Make sure MongoDB is running locally.

mongodb://localhost:27017
5. Run Backend
python app.py

Server will start at:

http://127.0.0.1:5000
6. Open Dashboard

Open browser:

http://127.0.0.1:5000
Example Threat Record
{
  "indicator_value": "185.234.217.12",
  "country": "RU",
  "isp": "M247 Ltd",
  "threat_type": "C2 Server",
  "severity": "high",
  "confidence_score": 90,
  "risk_score": 135,
  "abuse_score": 92,
  "mitre_technique": "T1071"
}
Dashboard Components

Severity Overview

High / Medium / Low counters

Threat Intelligence Charts

Severity distribution

Confidence score analytics

Threat detection timeline

Critical Threat Monitoring

Top 5 highest risk threats

Threat Intelligence Table

IP

Country

ISP

Threat type

MITRE technique

Severity

Confidence

Risk score

Abuse score

Status

Future Enhancements

Possible improvements include:

Global threat map visualization

VirusTotal integration

Shodan intelligence enrichment

Real-time threat feed ingestion

MITRE ATT&CK matrix visualization

User authentication for analysts

Alert notification system

Learning Outcomes

Through this project the following cybersecurity concepts were implemented:

Threat intelligence enrichment

Indicator prioritization

Risk scoring models

MITRE ATT&CK mapping

SOC analyst workflows

Data visualization for security analytics

Author

SOC Cyber Threat Intelligence Dashboard

Developed for cybersecurity portfolio and threat intelligence analysis training.
