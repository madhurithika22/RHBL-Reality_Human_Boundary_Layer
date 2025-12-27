# RHBL: Reality–Human Boundary Layer 🛡️👤

> **Defending Authenticity in the Age of Synthetic Media.**
> *Where Biological Truth Meets Digital Security.*

![Python](https://img.shields.io/badge/Python-3.9%2B-blue)
![React](https://img.shields.io/badge/React-18-cyan)
![FastAPI](https://img.shields.io/badge/FastAPI-0.109-green)

## 📖 Overview

**RHBL (Reality–Human Boundary Layer)** is a multi-modal security ecosystem designed to verify human authenticity and detect deepfakes in real-time. Unlike traditional FaceID or passive liveness detection, RHBL employs a **neuro-symbolic** approach, combining biological signal extraction (rPPG), cognitive stress testing, and physics-based validation to ensure the subject is not just present, but biologically alive.

This system is architected for **Edge Computing**, ensuring privacy by processing biometric vectors locally without transmitting raw face data to the cloud.

---

## 🏗️ The 4-Layer Architecture

RHBL forces attackers to bypass four distinct technologies simultaneously:

### 🧠 Layer 1: Human Bio-Authenticity (The Biological Check)
* **Technology:** Remote Photoplethysmography (rPPG) & 3D Depth Tesselation.
* **Function:** Extracts invisible color variations in the skin caused by blood flow to verify a live heartbeat. Checks facial depth to prevent screen/mask attacks.

### 🗣️ Layer 2: AI Manipulation Detection (The Intent Check)
* **Technology:** NLP Transformers & Active Verbal Challenge.
* **Function:** Detects psychological manipulation tactics (false urgency) and injects randomized verbal challenges to test the cognitive latency of the subject (breaking generative AI scripts).

### ⚛️ Layer 3: Reality Consistency (The Physics Check)
* **Technology:** Temporal Consistency Models.
* **Function:** Validates that motion obeys the laws of physics (inertia, gravity) and that micro-expressions align with biological plausibility.

### ⚖️ Layer 4: Trust Fusion (The Decision Engine)
* **Technology:** Bayesian Networks & Immutable Ledger.
* **Function:** Fuses signals from all layers to output a **Confidence Interval** (e.g., 98.2%) rather than a binary pass/fail. Validated media is cryptographically signed.

---

## 🛠️ Tech Stack

### Backend (The Sentinel Engine)
* **Framework:** FastAPI (Python)
* **Computer Vision:** OpenCV, MediaPipe (Face Mesh)
* **Signal Processing:** SciPy (rPPG extraction)
* **Database:** SQLite (Local, immutable logging)

### Frontend (The Dashboard)
* **Framework:** React.js (Vite)
* **Styling:** Tailwind CSS
* **Visualization:** Real-time Bio-Signal Graphs & Liveness Feedback

---

## 🚀 Installation & Setup

### Prerequisites
* Python 3.9+
* Node.js & npm
* Git

### 1. Clone the Repository
```bash
git clone https://github.com/madhurithika22/RHBL-Reality_Human_Boundary_Layer.git
cd RHBL-Reality_Human_Boundary_Layer
```

### 🏃‍♂️ Running the Application
To run the full system, you will need two separate terminal windows.
Terminal 1: Start the Backend Server
Navigate to the backend directory and start the FastAPI server on port 7000.

```bash
cd rhbl-
# (Optional) Create and activate a virtual environment
# python -m venv venv
# source venv/bin/activate  (or venv\Scripts\activate on Windows)

# Install Python dependencies
pip install -r backend/requirements.txt

# Run the Sentinel Engine
uvicorn backend.main:app --host 127.0.0.1 --port 7000 –reload
```

Note: The backend will initialize the rhbl_logs.db database automatically upon the first run.
Terminal 2: Start the Frontend Client
Navigate to the frontend directory and launch the React dashboard.

```bash
cd frontend

# Install Node modules
npm install

# Run the development server
npm run dev
```

## 📂 Project Structure

The project is organized into two main directories: `rhbl-` (Backend) and `frontend` (Dashboard).

```text
RHBL-Reality_Human_Boundary_Layer/
│
├── rhbl-/                     # Backend Environment
│   └── backend/               # Python Source Code
│       ├── __init__.py        # Package initialization
│       ├── main.py            # FastAPI Entry Point & API Routes
│       ├── logic.py           # Sentinel Engine (rPPG, Vision, State Machine)
│       ├── database.py        # SQLite Database Handler
│       ├── rhbl_logs.db       # Local Database (Auto-generated on run)
│       └── requirements.txt   # Backend Dependencies
│
└── frontend/                  # Frontend Application
    ├── public/                # Static Assets
    ├── src/                   # React Source Code
    │   ├── App.jsx            # Main Dashboard Component & Logic
    │   ├── main.jsx           # React DOM Entry
    │   └── index.css          # Tailwind Directives & Global Styles
    ├── package.json           # Node Dependencies & Scripts
    ├── tailwind.config.js     # Tailwind CSS Configuration
    └── vite.config.js         # Vite Bundler Configuration
