

🧩 Monolith Analysis App with OpenTelemetry and SigNoz
📌 Overview
This is a Flask-based monolith web application that simulates a dice roll and demonstrates full observability using OpenTelemetry. It exports traces, metrics, and logs to SigNoz using the OTLP HTTP protocol for real-time monitoring, error tracking, and performance analysis.

🚀 Key Features
🎲 Dice Roll Simulation at / or /rolldice endpoints

📊 OpenTelemetry Tracing & Metrics for HTTP requests and dice logic

⚠️ Exception Tracking with Error Logging (simulated)

📡 SigNoz Integration via OTLP over HTTP (Default port: 4318)

📁 Easy deployment via docker-compose and Codespace-ready

🛠️ Prerequisites
Ensure the following tools and setup before running the project:

✅ Python 3.12+

✅ SigNoz running locally (via Docker Compose or Codespaces)

✅ OpenTelemetry and Flask dependencies:

bash
pip install flask opentelemetry-api opentelemetry-sdk opentelemetry-exporter-otlp
📦 Setup Instructions
Clone the Repository
bash
git clone  https://github.com/KeerthanaGarimella/task-3
cd Monitoring-and-Logging-lnclass3
Start SigNoz (if not running)

bash
# Inside repo or SigNoz directory
docker-compose -f docker-compose.yaml up -d

Run the Flask Application

bash
python app.py
🌐 Access & Usage
Visit the app at: http://localhost:3000

Simulate a dice roll with optional player parameter:

ruby
http://localhost:3000/?player=Keerthana
View traces and metrics live in SigNoz dashboard (localhost:3301 or Codespaces forwarded port)

🧪 Simulating Errors (Optional for Testing)
To trigger an error and observe it in SigNoz


