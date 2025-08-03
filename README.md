# 🧩 Monolith Analysis App with OpenTelemetry and SigNoz

## 📌 Overview

This is a Flask-based monolith web application that simulates a dice roll and demonstrates full observability using **OpenTelemetry**. It exports **traces, metrics, and logs** to **SigNoz** using the **OTLP HTTP protocol** for real-time monitoring, error tracking, and performance analysis.

## 🚀 Key Features

- 🎲 Dice Roll Simulation via `/` or `/rolldice` endpoints
- 📊 OpenTelemetry Tracing & Metrics for HTTP requests and dice logic
- ⚠️ Exception Tracking with Simulated Errors
- 📡 SigNoz Integration via OTLP over HTTP (default port: `4318`)
- 📁 Easy deployment via Docker Compose / Codespaces

---

## 🛠️ Prerequisites

Ensure the following before setup:

- ✅ Python 3.12+
- ✅ SigNoz running (via Docker Compose or GitHub Codespaces)
- ✅ Required Python packages:

```bash
pip install flask opentelemetry-api opentelemetry-sdk opentelemetry-exporter-otlp
📦 Setup Instructions
1. Clone the Repository
bash
git clone https://github.com/KeerthanaGarimella/task-3
cd Monitoring-and-Logging-lnclass3
2. Start SigNoz (if not running)
bash
docker-compose -f docker-compose.yaml up -d
3. Run the Flask App
bash
python app.py
🌐 Access & Usage
Visit the app at: http://localhost:3000

Optional: Add a player parameter to simulate a named roll:
http://localhost:3000/?player=Keerthana
View traces and metrics live in SigNoz dashboard:
http://localhost:3301

or use forwarded port in Codespaces

🧪 Simulating Errors (for Testing)
To simulate an error and see it captured in SigNoz:

Modify roll() function in app.py:
python
def roll():
    raise Exception("Simulated dice roll failure!")
Access /rolldice endpoint to trigger the exception.
