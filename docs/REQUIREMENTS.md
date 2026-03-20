📋 Software Requirements Specification (SRS): PharmaShift
1. Project Overview
   PharmaShift is a full-stack web application designed to automate and manage the weekly scheduling of pharmacy personnel. The system aims to replace manual, error-prone scheduling with a rule-based engine that balances business operational needs, labor laws, and employee preferences.

2. User Personas
   Pharmacy Manager (Admin): Responsible for employee management, defining shift requirements, and generating/finalizing the weekly schedule.

Pharmacist/Assistant (Staff): Views the published schedule and tracks their assigned hours and historical shifts.

3. Functional Requirements (FR)
   FR1: Employee Management
   The system shall allow the Manager to Create, Read, Update, and Delete (CRUD) employee profiles.

Each profile must include: Full Name, Role (Pharmacist, Assistant, Technician), and Contract Type (Full-time 40h, Part-time 20h, etc.).

FR2: Shift Configuration & Coverage
The Manager shall define "Coverage Rules" (e.g., "Monday Morning requires 2 Pharmacists and 1 Assistant").

The system shall support various shift types: Morning (Opening), Afternoon (Closing), and Split-Shifts.

FR3: Scheduling Engine
The system shall generate a draft schedule based on pre-defined constraints.

The Manager shall be able to manually override or "lock" specific shifts.

FR4: Analytics & Fairness Tracking
The system shall track historical data to ensure "Fairness" (e.g., counting Saturday shifts worked per person over a 3-month period).

The system shall provide a summary of total hours worked per employee to prevent overtime violations.

4. Business Rules & Constraints
   In scheduling logic, we categorize rules into "Hard" (mandatory) and "Soft" (preferred) constraints:

A. Hard Constraints (Non-Negotiable)
Legal Rest Period: Minimum of 11 consecutive hours of rest between shifts (e.g., a "Closing" shift cannot be followed by an "Opening" shift the next day).

Mandatory Presence: A pharmacy cannot operate without at least one licensed Pharmacist on-site.

Maximum Hours: No employee can exceed their contract hours plus a specific legal overtime threshold.

B. Soft Constraints (Optimization Goals)
Employee Preferences: Attempt to honor "Day-Off" requests or preferred shift patterns.

Saturday Rotation: The system should prioritize employees who did not work the previous Saturday.

Split-Shift Minimization: Avoid assigning split-shifts to the same person multiple times a week unless necessary.

5. Non-Functional Requirements (NFR)
   Usability: The UI must be intuitive, allowing a schedule to be generated/edited with minimal clicks (React-based).

Reliability: Data must persist locally using an H2 file-based database, ensuring no data loss upon application restart.

Scalability: The backend architecture (Spring Boot) should allow for future transition to a cloud-based PostgreSQL database.