# autopilot_slm
An automation platform built with Python and React, enhanced by AI-powered features. It integrates a Small Language Model (SLM) for intelligent automation, streamlining workflows and boosting productivity. Combines modern web technologies with machine learning for scalable and efficient solutions.

## Frontend
- React application located in the `frontend/` folder.

## Backend
- Python backend located in the `backend/` folder.

## How to Run
1. Start the backend:
   ```bash
   cd backend
   source venv/bin/activate
   python app/main.py

   ---

#### **6. Optional: Add Docker Support**
If you want to containerize your application, create a `docker-compose.yml` file at the root:
```yaml
version: '3.8'
services:
  frontend:
    build:
      context: ./frontend
    ports:
      - "3000:3000"
    volumes:
      - ./frontend:/app
    command: npm start
  backend:
    build:
      context: ./backend
    ports:
      - "5000:5000"
    volumes:
      - ./backend:/app
    command: python app/main.py