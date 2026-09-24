# AI-Enabled Scholarship and Fellowship Management System for ST Students

> Smart India Hackathon 2026 · Problem Statement **SIH26239** · Team **Coding Haven**

An intelligent, end-to-end digital platform that automates, streamlines, and brings transparency to the distribution of scholarships and fellowships for Scheduled Tribe (ST) students — covering schemes administered by the Ministry of Tribal Affairs such as the National Fellowship (NFST), National Scholarship (Top Class), and the National Overseas Scholarship (NOS).

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](./LICENSE)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](#contributing)
![Status](https://img.shields.io/badge/status-in%20development-orange)

---

## Table of Contents

- [About the Project](#about-the-project)
- [Key Features](#key-features)
- [Tech Stack](#tech-stack)
- [System Architecture](#system-architecture)
- [Getting Started](#getting-started)
- [Project Structure](#project-structure)
- [Roadmap](#roadmap)
- [Team](#team)
- [Contributing](#contributing)
- [License](#license)

---

## About the Project

Navigating government welfare schemes can be challenging for students from remote and tribal regions — scattered application portals, manual document verification, and unclear rejection reasons often mean eligible students miss out on aid they qualify for.

This repository houses an AI-powered platform that bridges that gap. By combining Optical Character Recognition (OCR), predictive analytics, and automated verification workflows, the system reduces bureaucratic bottlenecks, helps prevent fraud, and supports swift, transparent Direct Benefit Transfer (DBT) to eligible students.

## Key Features

| Feature | Description |
|---|---|
| 🎯 **Intelligent Eligibility Matching** | Scans student profiles against complex criteria across central and state schemes to proactively surface matching opportunities. |
| 📄 **AI-Powered Document Verification** | Uses computer vision and OCR to validate caste certificates, income proofs, and mark sheets, cutting manual review time. |
| 🗣️ **Multilingual Voice & Chatbot Assistant** | Helps students with low digital literacy navigate the portal, fill forms, and check status in regional languages and tribal dialects. |
| 📉 **Predictive Dropout Analytics** | ML models track academic progress and attendance patterns to flag at-risk students and trigger timely interventions. |
| 🛡️ **Fraud Detection & Prevention** | Anomaly detection flags duplicate entries, forged documents, and suspicious claims in real time. |
| 💸 **Transparent DBT Tracking** | End-to-end fund tracking to Aadhaar-linked bank accounts, with no leakage. |

## Tech Stack

**Frontend**
- React.js / Next.js
- Tailwind CSS (responsive, mobile-friendly)

**Backend**
- Python — FastAPI / Django (REST APIs)

**Database**
- PostgreSQL / MongoDB

**AI / ML**
- Scikit-Learn, PyTorch — predictive models
- OpenCV — OCR and document verification
- Hugging Face Transformers — multilingual NLP

**Cloud & Storage**
- AWS / Google Cloud Platform — secure document storage and scalable hosting

## System Architecture

```
                ┌────────────────────┐
                │   Student Portal    │
                │ (Web / Voice / Bot) │
                └─────────┬───────────┘
                          │
                ┌─────────▼───────────┐
                │   API Gateway /      │
                │   Backend (FastAPI)  │
                └───┬─────────┬───────┘
                    │         │
        ┌───────────▼──┐  ┌───▼─────────────┐
        │ Eligibility & │  │  OCR / Document  │
        │ Matching Engine│  │  Verification    │
        └───────────┬──┘  └───┬─────────────┘
                    │         │
        ┌───────────▼─────────▼───────────┐
        │   Fraud Detection & Dropout      │
        │        Analytics (ML)            │
        └───────────────┬──────────────────┘
                         │
                ┌────────▼────────┐
                │  DBT / Disbursal │
                │     Tracking     │
                └──────────────────┘
```

## Getting Started

### Prerequisites

- Node.js ≥ 18
- Python ≥ 3.10
- PostgreSQL or MongoDB instance
- AWS / GCP credentials (for storage services)

### Installation

```bash
# Clone the repository
git clone https://github.com/<your-org>/<repo-name>.git
cd <repo-name>

# Frontend setup
cd frontend
npm install
npm run dev

# Backend setup
cd ../backend
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
uvicorn main:app --reload
```

### Environment Variables

Create a `.env` file in `/backend` with:

```env
DATABASE_URL=postgresql://user:password@localhost:5432/dbname
JWT_SECRET=your_secret_key
AWS_ACCESS_KEY_ID=your_key
AWS_SECRET_ACCESS_KEY=your_secret
```

## Project Structure

```
.
├── frontend/          # React/Next.js client
├── backend/           # FastAPI/Django server
│   ├── app/
│   │   ├── api/       # Route handlers
│   │   ├── models/    # DB models
│   │   ├── services/  # OCR, matching, fraud detection logic
│   │   └── ml/         # ML model training/inference
├── docs/              # Documentation, diagrams
└── README.md
```

## Roadmap

- [ ] MVP: eligibility matching + document upload for NFST, National Scholarship, NOS
- [ ] OCR verification pipeline (caste certificate, income proof, mark sheets)
- [ ] Multilingual chatbot (Hindi + 2–3 regional/tribal languages)
- [ ] Predictive dropout model (pilot)
- [ ] Fraud/anomaly detection rules
- [ ] DBT tracking dashboard for administrators

## Team

**Coding Haven** — Smart India Hackathon 2026, Problem Statement SIH26239

<!-- Add team member names/roles/GitHub handles here -->

## Contributing

Contributions, issues, and feature requests are welcome.

1. Fork the repository
2. Create your feature branch (`git checkout -b feature/amazing-feature`)
3. Commit your changes (`git commit -m 'Add some amazing feature'`)
4. Push to the branch (`git push origin feature/amazing-feature`)
5. Open a Pull Request

## License

Distributed under the MIT License. See `LICENSE` for more information.
