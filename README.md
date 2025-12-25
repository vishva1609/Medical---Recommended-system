# HealthApp – Disease Prediction Chatbot

## Overview
HealthApp (Disease Prediction Chatbot) is a Flask-based web application that helps users identify potential diseases based on symptoms.  
The application provides disease details, precautions, dietary recommendations, medication suggestions, and allows users to book appointments.

The entire application stack is containerized using **Docker** and orchestrated using **Docker Compose** for easy setup and execution.

---

## Features
- **Symptom Input:** Users can input symptoms through the web interface.
- **Disease Prediction:** Predicts possible diseases using a trained ML model.
- **Detailed Information:** Displays:
  - Precautions
  - Prediction explanation
  - Dietary recommendations
  - Medication suggestions
- **Appointment Booking:** Users can book appointments via the application.
- **API Support:** Backend endpoints can be tested using Postman.

---

## Technology Stack

### Backend
- Python (Flask)
- Machine Learning (scikit-learn)

### Frontend
- HTML templates
- CSS (Flask static files)

### Database
- SQLite (`user.db`)  
- Persisted using Docker volumes

### DevOps / Tooling
- Docker
- Docker Compose
- Postman (for API testing)

---

## Project Structure
```
healthapp-main/
├── medical/
│ ├── datasets/
│ ├── models/
│ ├── static/
│ ├── templates/
│ ├── main.py
│ └── user.db
├── postman/
│ └── HealthApp.postman_collection.json
├── Dockerfile
├── docker-compose.yml
├── requirements.txt
└── README.md

```
---

## Running the Application with Docker (Recommended)

### Prerequisites
- Docker
- Docker Compose

### Steps
1. Clone the repository:
```bash
git clone https://github.com/yourusername/healthapp.git
cd healthapp
```
2. Start the application:
```bash
docker compose up
```
3. Open the browser::
```bash
http://localhost:5000

```
## API Testing (Postman)

During development, backend APIs were tested using **Postman**.

A Postman collection is included in the repository:


### Sample API

**POST /predict**

#### Request Body
```json
{
  "symptoms": "itching, skin_rash, fatigue"
}
```
{
  "predicted_disease": "...",
  "precautions": [],
  "medications": []
}
## Database Details

The application uses **SQLite** as a lightweight database.

- The database is persisted using **Docker volumes**
- No external database or cache layer is required



License

This project is licensed under the MIT Licen