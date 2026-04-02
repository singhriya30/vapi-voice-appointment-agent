🏥 Dubai Hospital Voice Appointment Agent
An AI-powered voice assistant system that allows users to schedule, cancel, and view hospital appointments using voice interactions via Vapi.

This project integrates:

🎤 Voice AI (Vapi)
⚡ FastAPI backend
🗄️ Database (SQLAlchemy)
🌐 Public API exposure using ngrok
💻 Streamlit frontend (for testing)
🧠 Features
✅ Schedule appointment
❌ Cancel appointment
📅 View appointments
🎤 Voice interaction (Vapi)
🌍 Public API access via ngrok
📁 Project Structure

VAPI_VOICE_AGENT/
│
├── backend.py              # FastAPI backend
├── database.py             # Database setup (SQLAlchemy)
├── dummy_frontend.py       # Streamlit frontend (testing UI)
├── requirements.txt        # Python dependencies
├── .venv/                  # Virtual environment
⚙️ Requirements
🐍 Software
Python 3.10+
pip
ngrok account
📦 Python Dependencies

Create requirements.txt:

fastapi
uvicorn
sqlalchemy
pydantic
streamlit
requests

🔧 Setup Instructions
1️⃣ Clone / Create Project
mkdir VAPI_VOICE_AGENT
cd VAPI_VOICE_AGENT
2️⃣ Create Virtual Environment
python -m venv .venv

Activate:

.venv\Scripts\activate
3️⃣ Install Dependencies
pip install -r requirements.txt
🖥️ Running the Backend
python backend.py

You should see:

Uvicorn running on http://127.0.0.1:4444
🌐 Running ngrok
Step 1: Go to ngrok folder
cd C:\Users\SINGH\OneDrive\Desktop\ngrok\ngrok-v3-stable-windows-386
Step 2: Add Auth Token
.\ngrok.exe config add-authtoken YOUR_TOKEN
Step 3: Start Tunnel
.\ngrok.exe http 4444
Step 4: Copy Public URL

Example:

https://abc123.ngrok-free.app
🔗 API Endpoints
1️⃣ Schedule Appointment

POST /schedule_appointment/

{
  "patient_name": "Ria Singh",
  "reason": "headache",
  "start_time": "2026-04-02T22:00:00"
}
2️⃣ Cancel Appointment

POST /cancel_appointment/

{
  "patient_name": "Ria Singh",
  "date": "2026-04-02"
}
3️⃣ List Appointments

POST /list_appointments/

{
  "date": "2026-04-02"
}
💻 Running Frontend (Optional)
streamlit run dummy_frontend.py
🤖 Vapi Integration
Base URL

Replace:

http://localhost:4444

With:

https://your-ngrok-url.ngrok-free.app
Tool Request Body Schema
{
  "patient_name": "string",
  "reason": "string",
  "start_time": "string"
}
⚠️ Important Rules
start_time must be in ISO format
Example: 2026-04-02T22:00:00
Always use ngrok URL (NOT localhost)
🧪 Testing Flow
Start backend
Start ngrok
Copy public URL
Use in Vapi
Test scheduling via voice
