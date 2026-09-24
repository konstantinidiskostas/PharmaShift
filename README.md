# 🏥 PharmaShift

> **Status: 🚧 In Active Development**  
> A professional-grade scheduling solution designed for modern pharmacies, built with C# .NET and React.

## 📖 Project Overview
**PharmaShift** is a Full-Stack web application currently being developed to automate and optimize the weekly employee scheduling process for a local pharmacy.

Unlike generic calendar tools, this project focuses on the **"Nurse Scheduling Problem" (NSP)** applied to the pharmacy sector. It aims to replace manual planning with an intelligent system that ensures legal compliance, operational coverage, and fair shift distribution among staff.

### 🎯 The Real-World Challenge
The project is designed to solve complex scheduling constraints such as:
* Maintaining mandatory pharmacist presence at all times.
* Adhering to Labor Law requirements (e.g., the 11-hour rest rule between consecutive shifts).
* Tracking historical shift data to ensure "Fairness" in weekend and closing rotations.

---

## 🛠️ Tech Stack
* **Backend:** C# (.NET 8/9), ASP.NET Core Web API, Entity Framework Core.
* **Frontend:** React.js (Vite), JavaScript (ES6+), CSS3 / Tailwind.
* **Database:** SQLite (File-based local persistence).
* **Architecture:** Monorepo structure, RESTful API design.
* **Version Control:** Git & GitHub.

---

## 🚀 Development Roadmap
This repository serves as live documentation of the professional software development lifecycle:

- [x] **Requirement Analysis:** Stakeholder interviews and SRS documentation.
- [ ] **System Design:** Database schema design and API contract definition.
- [ ] **Core Backend:** Implementation of Employee & Shift management REST APIs.
- [ ] **Scheduling Engine:** Development of constraint-satisfaction validation rules.
- [ ] **Frontend Development:** Interactive shift dashboard and calendar interface.
- [ ] **UAT (Testing):** User Acceptance Testing with real pharmacy scheduling data.

---

## 📈 Key Features (Planned)
* **Automated Constraint Validation:** Real-time feedback for coverage gaps and labor law violations.
* **Historical Analytics:** Equal allocation monitoring for Saturday and evening shifts.
* **Local-First Architecture:** Reliable, lightweight local database without external server dependencies.
* **Responsive UI:** Streamlined interface for rapid weekly schedule adjustments.

---

## 📝 License & Purpose
This project is a **custom professional solution** developed to automate business operations for a specific pharmacy use case.

While the repository is public for **architectural review and portfolio demonstration**, the system is designed to meet concrete industry requirements and legal standards.

*All rights reserved. The source code and documentation are intended for peer review and professional evaluation.*