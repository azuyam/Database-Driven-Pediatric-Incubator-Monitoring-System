# 🍼 Database-Driven Pediatric Incubator Monitoring System

## 📖 Introduction
Neonatal Intensive Care Units (NICUs) depend on incubators to create a stable and secure environment for critically ill newborns. This project proposes integrating a MySQL database with an HTML-based web interface to facilitate real-time monitoring, data analysis, and automated alerts for pediatric incubators.

### Key Objectives
- **Enable real-time monitoring** of incubator conditions and infant vitals.
- **Enhance decision-making** through data storage and analysis.
- **Improve patient safety** by generating immediate alerts for critical health changes.

---

## 🎯 Project Goals
- Develop a database-driven system to collect and store incubator and patient health data.
- Design an intuitive web-based dashboard for monitoring incubators remotely.
- Implement automatic notifications when vital signs or environmental factors reach unsafe levels.
- Ensure secure data access with role-based permissions to protect sensitive patient information.

---

## 💻 Technology Stack
- **Database:** MySQL
- **Development Environment:** XAMPP
- **Frontend:** HTML5, CSS3
- **Backend:** PHP (for data retrieval, processing, and CRUD operations)

---

## ⚙️ System Features
- **Database Integration:** Reliable MySQL architecture for data storage and management.
- **Interactive Dashboard:** Built with HTML, CSS, and PHP for seamless monitoring.
- **Automated Alerts:** Instant notifications for abnormal vital signs or incubator conditions.
- **Data Security:** User authentication and encryption protocols to safeguard patient data.
- **Remote Access:** Secure web-based access.

> **Note for Developers - Default Credentials:**
> - **Username:** `admin`
> - **Password:** `password123`

---

## 🗄️ Database Architecture

### Database Name: `NICU_DB`

### Entity-Relationship (ER) Design
#### 1. Patient Details
- `Patient ID` **(Primary Key)**: Unique two-digit identifier
- `First Name` & `Last Name`
- `Assigned Room`

#### 2. Incubator Data
- `Incubator ID` **(Primary Key)**: Unique two-digit identifier
- `Model Type`
- `Assigned Room`
- `Carbon Dioxide Level (%)`
- `Temperature (°C)`
- `Humidity (%)`

#### 3. Patient Vitals
- `Vitals ID` **(Primary Key)**: Unique two-digit identifier
- `Oxygen Saturation (%)`
- `Weight (kg)`
- `Heart Rate`
- `Blood pH Level`

#### 4. Authorized Users
- `User ID` **(Primary Key)**: Unique two-digit identifier
- `First Name` & `Last Name`
- `Username` & `Password` *(For login authentication)*

### Database Relationships & Rules
- **Patient-Incubator (1:1 Relationship):** Each patient is assigned exactly *one* incubator. A patient cannot have multiple incubators.
- **Patient-Vitals (1:N Relationship):** Multiple vital sign records are stored for each patient over time.
- **Room Assignment Rule:** Patient room assignments **must** match their assigned incubator's room.

---

## 🚀 Project Implementation Plan

### 1. User Authentication & Access Control
- **Login Requirement:** Mandatory login for all users.
- **Role-Based Permissions:**
  - **Admin:** Full CRUD (Create, Read, Update, Delete) access.
  - **Guest:** Read-only viewing privileges.

### 2. Dashboard Components & Layout
The interface is structured for intuitive navigation and quick access to critical data.

#### 🔐 Login Page
- Restricts access based on user roles (Admin vs. Guest).

#### 🎛️ Main Dashboard
- **Vitals Overview:** Table displaying patient vitals linked to real-time incubator conditions.
- **Data Tables:** Two primary views—one for patients/vitals, the other for incubators/parameters.
- **Navigation:** Buttons for Patient Management, Incubator Management, and a Logout button.

#### 🚼 Patient Management Page
- Table of all patient details.
- Add new patients (with strict input validation formats).
- Edit patient attributes.
- Assign incubators to patients.
- Back button to return to the main dashboard.

#### 🏥 Incubator Management Page
- Table displaying current incubator data and status.
- Add new incubators (with required input formats).
- Edit incubator environmental parameters.
- Back button to return to the main dashboard.

---

## 📈 Expected Outcomes
1. A fully functional, database-integrated system for monitoring incubators in NICUs.
2. More precise and efficient tracking of neonatal health conditions.
3. A secure, web-based dashboard for remote access to real-time data.
4. Enhanced patient safety through automated alerts and actionable data insights.

---

## 🏁 Conclusion
This project will modernize neonatal care by integrating a database-driven solution for monitoring incubator conditions and infant vitals. The proposed system will aid healthcare professionals in making informed decisions, improving patient safety, and increasing efficiency in NICU operations.
