# StateraSense
# 🧠 StateraSense – Burnout Prevention Platform

**StateraSense** is a modular, extensible, and intelligent burnout prevention system built with .NET using **Clean Architecture** and **Microservices**. It helps users assess stress, receive personalized wellness recommendations, set micro-goals, and track their mental well-being over time.

---

## 🚀 Features

- 📝 **Stress Self-Assessments**  
- 💡 **AI-Driven Personalized Recommendations** (coming soon)  
- 🎯 **Micro Goals & Progress Tracking**  
- 🔔 **Smart Reminders for Wellness Activities**  
- 📊 **Wellness Analytics Dashboard**  
- 🧑‍💼 **User & Subscription Management**  
- 🏢 **Organization Onboarding (Schools/Companies)**  

---

## 📦 Project Structure

```plaintext
StateraSense/
├── src/
│   ├── Services/
│   │   ├── UserService/
│   │   ├── StressCheckService/
│   │   ├── RecommendationService/
│   │   ├── MicroGoalService/
│   │   ├── WellnessReportService/
│   │   ├── ReminderService/
│   │   └── OrganizationService/
│   ├── BuildingBlocks/
│   └── Shared/
├── docs/
└── StateraSense.sln
```

Each service follows Clean Architecture:
- `Domain` (Entities, ValueObjects, Events)  
- `Application` (Use Cases, Interfaces, DTOs)  
- `Infrastructure` (EF, external services, data access)  
- `API` (Controllers, endpoints, validations)

---

## 📐 Architecture

- ✅ **Clean Architecture** (use-case-driven design)  
- ✅ **Microservices** (scalable, modular)  
- ✅ **Polyglot Persistence**: SQL Server, PostgreSQL, MongoDB  
- ✅ **AI-Ready** for future ML/LLM-based personalization  
- ✅ **DDD** principles with clear bounded contexts  

---

## 🛠️ Tech Stack

- **Backend**: ASP.NET Core (.NET 8/9)  
- **Databases**:
  - SQL Server (Users, Organizations)
  - PostgreSQL (Workload, Wellness Reports)
  - MongoDB (Assessments, Interventions)
- **Authentication**: JWT + Identity (with support for OAuth2 planned)
- **DevOps**: Docker, GitHub Actions (CI/CD)  
- **AI**: OpenAI / ML.NET (planned)  

---

## 🧪 Getting Started

### Prerequisites

- [.NET 8 or 9 SDK](https://dotnet.microsoft.com/)
- Docker (for services and DBs)
- PostgreSQL, SQL Server, MongoDB (via Docker or local installs)

### Run the app

```bash
# Clone the repository
git clone https://github.com/venlomj/StateraSense.git
cd StateraSense

# Launch required services
docker-compose up -d

# Build and run solution
dotnet build
dotnet run --project src/Services/UserService/StateraSense.UserService.API
```

### Development Notes
- Each microservice can be run/debugged independently.
- Services communicate via REST and will eventually use message queues (RabbitMQ/Kafka) for async processing.

---

## 🌍 Roadmap

- [x] User Registration & Auth  
- [x] Stress Check API  
- [ ] Personalized AI Recommendations  
- [ ] Micro Goals & Reminders  
- [ ] Analytics Dashboard  
- [ ] Organization Portals  
- [ ] Mobile App (Xamarin/.NET MAUI)

---

## 🧠 Vision

**StateraSense** aims to become an intelligent companion for managing personal well-being in education, workplaces, and everyday life — helping users **prevent burnout before it begins**.

---

## 📄 License

MIT License © venlomj
