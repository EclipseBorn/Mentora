# Mentora — AI-Based Student Mental Health Safety & Support System

**Mentora** is a student wellbeing platform designed to support early identification of mental health concerns through weekly wellbeing surveys, risk assessment, and role-based dashboards. It aims to help students connect with mentors and enable responsible, data-informed campus support.

## 🎯 Problem Statement

Students may experience academic stress, emotional difficulties, and other wellbeing concerns without receiving timely support. Traditional campus support systems can struggle to identify emerging concerns early, monitor wellbeing trends, and coordinate communication between students and mentors.

## 💡 Proposed Solution

Mentora brings student wellbeing surveys, risk assessment, mentor–student communication, and role-specific dashboards into one platform. Its planned machine-learning integration uses **Python and Scikit-learn** to support predictive risk analysis and help authorized support personnel identify students who may need additional attention.

## ✨ Key Features

- **Weekly Wellbeing Surveys** — Collect structured responses to monitor changes in student wellbeing.
- **Risk Assessment** — Organize survey-related information into risk profiles to support early intervention.
- **Machine Learning Integration** — Designed to support predictive analytics using Python and Scikit-learn.
- **Role-Based Dashboards** — Provide separate interfaces and access permissions for different user roles.
- **Mentor–Student Communication** — Support communication between students and their assigned mentors.
- **Centralized Data Management** — Use MongoDB Atlas to store application data.
- **Authentication and Access Control** — Include JWT-based authentication middleware and role-based authorization.
- **Modular Architecture** — Separate frontend pages, backend controllers, routes, models, and configuration for maintainability.

> **Important:** Risk predictions are intended to support—not replace—qualified human judgment. A model score is not a mental health diagnosis, and urgent concerns require appropriate human support.

## 🛠️ Technology Stack

| Layer | Technologies |
|---|---|
| Frontend | React.js, Vite, Tailwind CSS v4 |
| Backend | Node.js, Express.js |
| Database | MongoDB Atlas, Mongoose |
| Machine Learning | Python, Scikit-learn |
| Authentication | JWT, role-based access control |
| API Communication | Axios, REST API architecture |

## 🏗️ System Architecture

```text
Student
   │
   ▼
React + Tailwind CSS Frontend
   │
   ▼
Express.js REST API
   │
   ├── Authentication & Role-Based Access
   │
   ├── Weekly Survey Management
   │
   ├── Risk Profile Management
   │
   ├── Mentor–Student Communication
   │
   ▼
MongoDB Atlas

Python + Scikit-learn
   │
   └── Planned ML risk-analysis integration
```

The application follows a modular client–server architecture. The backend separates route definitions, controllers, data models, middleware, and services. The frontend uses reusable components, authentication context, API utilities, and role-specific pages.

## 📂 Project Structure

```text
Mentora/
├── client/
│   └── src/
│       ├── api/          # API client and JWT handling
│       ├── components/   # Reusable UI components
│       ├── context/      # Authentication state
│       ├── hooks/        # Custom React hooks
│       ├── layouts/      # Dashboard layouts and role guards
│       ├── pages/        # Role-specific dashboards and pages
│       └── routes/       # Application navigation
│
├── server/
│   ├── config/           # Database configuration
│   ├── controllers/      # Application request handlers
│   ├── models/           # Mongoose data models
│   ├── routes/           # API route definitions
│   ├── middleware/       # Authentication and authorization
│   ├── services/         # Business logic and integrations
│   └── utils/            # Shared utilities
│
└── README.md
```

*The structure above follows the repository's documented architecture; individual files and additional ML directories may vary.*

## 🚀 Getting Started

### Prerequisites

- Node.js v16 or later
- npm
- A MongoDB database, locally or through MongoDB Atlas
- Python and Scikit-learn when setting up the ML component

### 1. Clone the Repository

```bash
git clone https://github.com/theoudar03/Mentora.git
cd Mentora
```

### 2. Configure the Backend

```bash
cd server
npm install
```

Create a `.env` file using the repository's `.env.example`:

```bash
cp .env.example .env
```

Configure `MONGO_URI` and any other environment variables required by the application. Keep credentials and secrets out of version control.

Start the backend:

```bash
npm run dev
```

### 3. Configure the Frontend

Open a second terminal:

```bash
cd Mentora/client
npm install
npm run dev
```

Open the local URL printed by Vite in your terminal.

**Note:** These instructions follow the current README's documented setup. Required environment variables, API URLs, and available scripts may need adjustment if the codebase has changed.

## 🧪 Demo and Testing

The repository documents a demo login layout for exploring role-based dashboards without initially creating database records. Where available, select a demo user from the login dropdown.

Test authentication, role-specific navigation, survey submission, and communication features against the actual implementation before treating them as production-ready.

## 🔐 Privacy, Safety, and Responsible AI

Mental health information requires particular care. A responsible deployment should include:

- Strict role-based access and least-privilege permissions.
- Secure storage and transmission of sensitive information.
- Clear consent and transparent explanations of data usage.
- Limited retention and access to wellbeing records.
- Human review of risk flags and a defined escalation process.
- Testing for model accuracy, bias, and false positives and negatives.

Mentora is intended to assist campus wellbeing support, not replace professional mental health care.

## 🔮 Future Enhancements

- Integrate a Python/Scikit-learn prediction service with the backend.
- Track wellbeing trends across repeated surveys.
- Add explainable risk indicators and authorized intervention workflows.
- Improve mentor follow-up and support-resource management.
- Evaluate model performance, fairness, and reliability before deployment.

## 👨‍💻 Developer

**Theoudar Doss. D**

- GitHub: [@theoudar03](https://github.com/theoudar03)
- Project Repository: [Mentora](https://github.com/theoudar03/Mentora)

---

*Mentora — Supporting student wellbeing through thoughtful technology and timely human support.*
