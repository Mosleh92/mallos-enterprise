<div align="center">

# 🏬 MallOS

### Mall management system with role-based authentication and operational monitoring

*Multi-role auth • Real-time monitoring • Operational analytics • Node.js + React*

[![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18%!B(MISSING)-339933?style=for-the-badge&logo=node.js&logoColor=white)](https://nodejs.org/)
[![React](https://img.shields.io/badge/React-18-61DAFB?style=for-the-badge&logo=react&logoColor=white)](https://react.dev/)
[![License](https://img.shields.io/badge/License-Proprietary-red?style=for-the-badge)](./LICENSE)

[Features](#-features) • [Architecture](#-architecture) • [Roles](#-role-hierarchy) • [Contact](#-contact)

</div>

---

## 💡 Overview

**MallOS** is a web-based management system for shopping mall operations. It provides role-based dashboards for operations teams, security staff, and management with real-time monitoring capabilities and operational workflow tools.

---

## ✨ Features

### 🔐 Authentication & Access Control
- **Multi-role login** — General Manager, Operations Manager, Security Guard
- **Two-factor authentication (2FA)** for management roles
- **Role-based dashboards** — tailored interface per user role
- Session management with activity logging

### 📊 Operational Modules
- **Tenant management** — lease tracking, contact information, status updates
- **Security incidents** — incident logging with photo/video evidence
- **Maintenance tracking** — ticket workflow, priority management, completion status
- **Visitor analytics** — footfall data, peak hours analysis, trends

### 📡 Real-Time Monitoring
- **Live dashboards** with auto-refresh capabilities
- **Alert notifications** for critical issues
- **Status monitoring** across operational areas
- **Performance metrics** tracking

---

## 🏛️ Architecture

```mermaid
graph TB
    subgraph "Users"
        GM[General Manager]
        OPS[Operations Manager]
        SEC[Security Staff]
    end

    subgraph "Frontend"
        WEB[React Dashboard]
        MOB[Mobile Web View]
    end

    subgraph "Backend"
        API[Express API]
        AUTH[Authentication + RBAC]
        NOTIF[Notification Service]
    end

    subgraph "Data"
        DB[(PostgreSQL)]
        FILES[File Storage]
    end

    GM & OPS & SEC --> WEB & MOB
    WEB & MOB --> API
    API --> AUTH
    API --> NOTIF
    AUTH --> DB
    API --> DB
    API --> FILES
```

---

## 👥 Role Hierarchy

| Role | Access Level | Capabilities |
|---|---|---|
| **General Manager** | Full system access | Financial reports, tenant decisions, system configuration |
| **Operations Manager** | Operations + Analytics | Maintenance oversight, performance reports, staff coordination |
| **Security Staff** | Security + Incidents | Incident logging, patrol tracking, basic reporting |

---

## 🛠️ Tech Stack

| Component | Technology |
|---|---|
| **Frontend** | React, TypeScript, Tailwind CSS |
| **Backend** | Node.js, Express, TypeScript |
| **Database** | PostgreSQL |
| **Authentication** | JWT with TOTP-based 2FA |
| **File Handling** | Multer for uploads |
| **Real-time** | WebSocket for live updates |

---

## 🚀 Key Implementation Features

- **Role-based routing** — React Router with permission guards
- **Real-time updates** — WebSocket connections for live dashboard data
- **File upload handling** — Secure document and image storage
- **Responsive design** — Mobile-friendly interface for field staff
- **Audit logging** — All user actions tracked for compliance

---

## 📄 Status & Licensing

**Status:** Production system deployed and operational  
**Code:** Proprietary - architecture documented here for demonstration

**Available for:**
- 🏢 Mall operator licensing and customization
- 🛠️ Feature enhancement and integration work
- 🤝 Technical consultation on similar systems

---

## 📬 Contact

📧 **moslehmohammad2@gmail.com**  
🐙 **[github.com/Mosleh92](https://github.com/Mosleh92)**

---

<div align="center">

*Production mall management system — built for operational efficiency*

</div>