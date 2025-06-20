# SwiftAid

**SwiftAid** is a full-stack, real-time emergency response system that leverages AI, live GPS tracking, and cloud-based microservices to drastically reduce ambulance response times and streamline hospital coordination.

---

## 🚀 Key Features

- **1-Tap Emergency SOS**  
  Immediate emergency request initiation with real-time location sharing from the user.

- **AI-Based Ambulance Dispatch**  
  Smart selection of the nearest and fastest ambulance using real-time traffic data.

- **Real-Time Tracking**  
  Live ambulance and patient tracking powered by WebSocket communication.

- **Traffic-Aware Navigation**  
  Integration with Google Maps or Mapbox Directions API for optimized route planning.

- **Hospital Coordination System**  
  Automatically checks hospital ER availability and sends alerts for faster prep.

- **Driver Interface**  
  Paramedics receive turn-by-turn navigation, patient info, and live updates.

- **Admin Dashboard**  
  Centralized control panel to monitor metrics, dispatch activity, and system health.

---

## 🧱 System Architecture

| Layer                | Tech Stack                                      |
|----------------------|--------------------------------------------------|
| **Frontend**         | React.js (modular apps for patients, drivers, admins) |
| **Backend**          | Java Spring Boot (microservice architecture)     |
| **Database**         | PostgreSQL (relational data storage)             |
| **Realtime Updates** | Spring WebSocket + Socket.IO                     |
| **AI Module**        | Python microservice (REST/GRPC API)              |
| **Mapping Services** | Google Maps / Mapbox Directions API              |
| **Cloud Infrastructure** | AWS (EC2, RDS, S3, ALB, CloudWatch)         |
| **DevOps**           | Docker, Kubernetes (EKS), GitHub Actions / Jenkins |

---

## 🔧 Microservices Overview

- **User Service**  
  Authentication, authorization, and role-based access control (JWT-based).

- **Ambulance Service**  
  Tracks ambulance availability, location, and real-time updates.

- **Hospital Service**  
  Monitors ER capacity and sends critical alerts to staff.

- **Dispatch Engine**  
  Central AI-driven logic for ambulance-patient matching and ETA prediction.

- **Notification Service**  
  Sends SMS, email, and push notifications to all stakeholders.

---

## 📂 Repository Structure

```text
.
├── frontend/               # React applications (User, Driver, Admin)
├── backend/
│   ├── user-service/
│   ├── ambulance-service/
│   ├── hospital-service/
│   ├── dispatch-service/
│   └── notification-service/
├── ai-module/             # Python microservice for traffic/ETA prediction
├── docker/                # Docker & Kubernetes configs
├── docs/                  # Architecture diagrams, API contracts, flowcharts
└── README.md
```
---

## 🔄 Data Flow Summary

```text
1. User triggers an SOS request from the app.
2. Frontend sends the request to the backend API.
3. Backend forwards it to the Dispatch Engine.
4. Dispatch Engine:
   - Queries nearby ambulances
   - Uses AI model to evaluate fastest route
   - Selects optimal ambulance
5. Ambulance is dispatched and notified.
6. Hospital is alerted with patient and ETA data.
7. Real-time tracking updates are pushed via WebSocket to all parties.
```
---
