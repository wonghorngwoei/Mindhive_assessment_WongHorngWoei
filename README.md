# McDonald Location Finder with LLM Chatbot

A comprehensive system to locate McDonald's outlets in Kuala Lumpur, Malaysia with AI-powered store information queries.

## ✨ Features

- 🗺️ Interactive map with all McDonald's locations
- 📍 5KM catchment area visualization
- 🔍 Intersection highlighting for overlapping areas
- 💬 Natural language chatbot for store queries
- ⏰ 24-hour store filtering
- 🎉 Birthday party venue finder

## 🛠 Tech Stack

| Component       | Technology Used                  |
|-----------------|----------------------------------|
| **Frontend**    | React, Google Maps API           |
| **Backend**     | FastAPI (Python)                 |
| **Database**    | SQLite                           |
| **Chatbot**     | Llama-2-70b-hf (via Together AI) |
| **Geocoding**   | Google Maps Geocoding API        |

## 🚀 Quick Start

### Prerequisites
- Python 3.9+
- Node.js 16+
- SQLite
- Google Maps API key
- Together AI API key

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/wonghorngwoei/McDonald_Location_with_LLMChatbot.git
   cd {yourfilelocation}

2. **Set up backend**


**Create and activate virtual environment**


python -m venv venv


source venv/bin/activate  # Linux/Mac


venv\Scripts\activate     # Windows

**Install dependencies**


pip install -r requirements.txt

**Edit .env with your API keys**

3. **Set up frontend**


cd mcdonalds-map


npm install

### Running the Application
1. **Start backend server**
uvicorn main:app --reload

2. **Start frontend**
npm start

## 🌐 API Endpoints

| Endpoint      | Method  | Description                       |
|---------------|---------|-----------------------------------|
| /stores       | GET     | Get all McDonald's outlets        |
| /chatbot      | POST    | Process natural language queries  |
| /geocode      | POS     | Geocode addresses to coordinates  |

## 💬 Chatbot Examples
1. Which outlets in KL operate 24 hours?
2. Which outlet allows birthday parties?
3. Show me details of Mcdonald's Bukit Bintang

## ⚠️ Limitations

### Technical Constraints
1. **Response Latency**
   - 2-5 second delay on complex queries
   - Llama-2-70B model processing overhead
   - Peak usage performance degradation

2. **Conversation Limitations**

   - No context retention between queries

   - Cannot handle follow-up questions naturally

   - Each query treated as independent

3. **Security Considerations**

   - LLM-generated SQL requires validation

   - Potential injection vulnerabilities

   - Limited to SELECT queries only

## 🚀 Future Enhancements
1. **Conversation Memory**
   - Context-aware follow-ups

   - Multi-turn dialogue support

   - Session-based query history

2. **Enhanced Security**

   - SQL syntax validator

   - Query whitelisting


3. **AI Capabilities**
   - Retrieval-Augmented Generation (RAG)

   - Automated data refresh pipeline

## 🌐 Live Deployment
***When using website, backend may delay for 50 seconds or more due to free services (will spin down with inactivity)***
**Frontend (Vercel)**

Vercel
URL: https://mindhive-assessment-wong-horng-woei-pbcw6bo4l.vercel.app/


**Backend (Render)**

Render
Base URL: https://mindhive-assessment-wonghorngwoei.onrender.com


API Endpoints:

GET /stores - List all McDonald's stores

GET /chatbot?query=text - Chatbot interface


