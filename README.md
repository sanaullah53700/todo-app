# 🚀 Task Nest — Enterprise Task & Employee Management Platform

> **Organize · Assign · Achieve**

Task Nest is a modern, enterprise-style **task and employee management platform** developed during my internship at **Code Bean Software House**.

The project is designed around a multi-role company environment where a **Super Admin** can manage employees, assign and monitor tasks, review employee performance, and track activity, while employees have their own workspace for managing assigned and personal tasks.

---

## 📌 Project Overview

Task Nest was developed to solve a common workplace challenge: keeping employee tasks, deadlines, priorities, progress, and activity organized in one centralized platform.

The system provides separate experiences for:

* 👑 **Super Admin**
* 👤 **Employees**

Each role has access to functionality appropriate to their responsibilities.

The application also includes an interactive dashboard, task priority indicators, deadlines, audit activity, authentication flows, reporting, and persistent browser-based data storage.

---

## ✨ Key Features

### 👑 Super Admin Portal

The Super Admin has centralized control over the company workspace.

* Add and manage employees
* Assign tasks to employees
* Set task descriptions and instructions
* Set task priority
* Set task deadlines
* Monitor employee task progress
* View employee performance information
* Review activity/audit logs
* Export employee task history
* Generate printable performance reports
* Manage company registration information

Tasks assigned by the Super Admin are recorded with the employee, priority, deadline, status, and assignment information.

---

### 👤 Employee Portal

Employees have their own workspace for managing their daily work.

Employees can:

* View assigned tasks
* Create personal tasks
* Set task priority
* Set deadlines
* Mark tasks as completed
* Remove tasks
* Track task status
* View their work-related information

Task completion and deletion actions are also reflected in the application's activity tracking system.

---

## 🔐 Authentication System

Task Nest includes a multi-step authentication interface supporting different user roles.

### Supported Authentication Flows

* Super Admin login
* Employee login
* Company registration
* Sign out
* Forgot password workflow
* OTP verification
* Password reset

The application separates the Super Admin and Employee login experiences and provides role-specific access after authentication.

> **Note:** The current project is a frontend/demo implementation. Authentication credentials and OTP functionality are implemented for demonstration purposes and should not be considered production-grade security.

---

## 📊 Task Management

Tasks contain information such as:

* Task title
* Description
* Assigned employee
* Priority
* Deadline
* Status
* Assignment source
* Creation date

### Task Priorities

| Priority              | Indicator         |
| --------------------- | ----------------- |
| 🔴 Very Important     | Urgent / Critical |
| 🟠 Important          | High Priority     |
| 🔵 Not Much Important | Normal Priority   |

The application also supports different task states including **Assigned, Completed, Overdue, and Deleted**.

---

## 📋 Activity & Audit Tracking

Task Nest maintains an activity log for important employee actions.

Examples include:

* Task creation
* Task completion
* Task assignment
* Employee activity

This gives administrators better visibility into what is happening inside the workspace.

---

## 📈 Reporting

The application provides employee task reporting functionality.

Reports can include:

* Employee name
* Role / department
* Performance score
* Task ID
* Task title
* Priority
* Assigned by
* Status
* Deadline
* Creation date

The project supports exporting task history as a **CSV report** and generating a **printable performance report**.

---

## 💾 Data Persistence

Task Nest uses browser storage to preserve application data between sessions.

The implementation includes:

* `localStorage`
* `sessionStorage`
* Safe storage fallback
* Data versioning
* Persistent company data
* Persistent tasks
* Persistent audit logs
* Session persistence

A fallback in-memory storage mechanism is also included for environments where browser storage is unavailable.

---

## 🎨 UI / UX

The interface was designed with a modern SaaS/enterprise dashboard aesthetic.

### Design Highlights

* 🌙 Dark theme
* ✨ Glassmorphism UI
* 🎨 Gradient-based visual system
* 📱 Responsive layout
* 🔔 Toast notifications
* 🪟 Modal-based forms
* 🎬 Animated splash screen
* 📊 Visual performance indicators
* 🏷️ Color-coded task priorities
* 🎉 Completion animations
* 🔊 Interactive feedback sounds

## The project uses **Outfit** and **Plus Jakarta Sans** typography and a glass-panel visual system with backdrop blur and gradient accents.

## 🛠️ Technologies Used

### Frontend

* HTML5
* CSS3
* JavaScript
* DOM Manipulation
* Browser Storage APIs

### UI / Visuals

* CSS Gradients
* Glassmorphism
* CSS Animations
* Responsive Design
* Google Fonts

### Additional Libraries

* Canvas Confetti

The project loads the Canvas Confetti library for task-completion feedback animations.

---

## 🏗️ Application Architecture

The current implementation is a **client-side web application** contained primarily within an HTML file.

### High-Level Flow

```text
                    ┌─────────────────────┐
                    │      Task Nest      │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │   Authentication    │
                    └──────────┬──────────┘
                               │
                 ┌─────────────┴─────────────┐
                 │                           │
        ┌────────▼────────┐        ┌─────────▼────────┐
        │   Super Admin   │        │     Employee     │
        │     Portal      │        │      Portal      │
        └────────┬────────┘        └─────────┬────────┘
                 │                           │
       ┌─────────▼──────────┐       ┌─────────▼──────────┐
       │ Employee Management│       │ Personal Tasks     │
       │ Task Assignment    │       │ Assigned Tasks     │
       │ Performance        │       │ Completion         │
       │ Audit Logs         │       │ Deadlines          │
       │ Reports            │       │ Priorities         │
       └────────────────────┘       └────────────────────┘
```

---

## 🚀 Getting Started

### 1. Clone the Repository

```bash
git clone https://github.com/YOUR-USERNAME/task-nest.git
```

### 2. Open the Project

Navigate into the project directory:

```bash
cd task-nest
```

### 3. Run the Application

Because the current version is a frontend application, you can open the HTML file directly in a modern browser.

Alternatively, use a local development server such as **VS Code Live Server**.

---

## 🔑 Demo Credentials

The project contains preset demonstration credentials.

### Super Admin

```text
Email: admin@apex.com
Password: admin123
```

### Employee

```text
Email: alex.rivera@apex.com
Password: emp123
```

> ⚠️ These credentials are for demonstration/testing only. Do not use them in a production environment.

---

## 📂 Suggested Project Structure

```text
task-nest/
│
├── index.html
├── README.md
└── assets/
    ├── images/
    └── icons/
```

If you later separate the project into multiple files, a more scalable structure could be:

```text
task-nest/
│
├── index.html
├── css/
│   └── style.css
│
├── js/
│   ├── auth.js
│   ├── admin.js
│   ├── employee.js
│   ├── tasks.js
│   └── storage.js
│
├── assets/
│   ├── images/
│   └── icons/
│
└── README.md
```

---

## 🎯 Project Objectives

The main objectives of this project were to:

* Build a realistic company task-management workflow
* Implement role-based user experiences
* Create separate Admin and Employee portals
* Practice JavaScript-based application state management
* Implement task CRUD-style interactions
* Track employee activity
* Build a modern enterprise dashboard UI
* Implement browser-based data persistence
* Create reporting functionality
* Improve practical frontend development skills

---

## 🔮 Future Improvements

The current version is primarily a frontend/demo implementation. A production-ready version could be extended with:

* 🔐 Backend authentication
* 🗄️ SQL / NoSQL database
* 🔒 Secure password hashing
* 👥 Real user management
* 🛡️ Server-side role-based authorization
* 📧 Real email OTP verification
* 🔔 Real-time notifications
* ☁️ Cloud deployment
* 📊 Advanced analytics
* 📅 Calendar integration
* 💬 Team communication
* 📎 File attachments
* 🔄 Real-time task updates
* 📱 Progressive Web App support

---

## 🧑‍💻 Internship Project

This project was developed as part of my **software development internship at Code Bean Software House**.

It provided practical experience in:

* Frontend development
* JavaScript application logic
* UI/UX implementation
* Authentication flows
* Role-based interfaces
* Task management systems
* Browser storage
* Reporting
* Dashboard design
* Problem solving and debugging

---

## ⚠️ Disclaimer

Task Nest is currently a **demonstration / internship project**.

The current implementation stores application data in the browser and uses demo authentication credentials. It should not be deployed as a production employee-management system without implementing a secure backend, database, proper authentication, authorization, and server-side data validation.

---

## 👨‍💻 Developer

**Developed during internship at Code Bean Software House**

Built with ❤️ using **HTML, CSS & JavaScript**.

---

## ⭐ If You Like This Project

If you find this project useful or interesting, consider giving the repository a ⭐ on GitHub.

**Task Nest — Organize · Assign · Achieve**
