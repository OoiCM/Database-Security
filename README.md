# 🛡️ Medical Information System (Database Security)

A secure medical database system implementing encryption, data masking, access control, and auditing to protect sensitive patient, staff, and diagnosis information.

---

## 📂 Project Description

This project designs and implements a **secure healthcare database system** that manages:

* 👨‍⚕️ Staff information
* 🧑‍🤝‍🧑 Patient records
* 📝 Appointment & diagnosis data

The system ensures **confidentiality, integrity, and availability (CIA)** by applying multiple layers of database security techniques.

---

## 🏗️ System Structure

The database consists of three main entities:

* **Staff** → Stores employee details
* **Patient** → Stores patient information
* **AppointmentAndDiagnosis** → Links patients and doctors with medical records

Primary keys and foreign keys are used to maintain **data integrity and relationships**.

---

## 🔐 Security Features

### 🔒 Data Protection

* Symmetric encryption (AES) for:

  * Phone numbers
  * Home addresses
* Asymmetric encryption for:

  * Diagnosis details (highest sensitivity)
* All sensitive data stored as **ciphertext**

---

### 🎭 Data Masking

* Sensitive fields are masked (`**********`) for unauthorized users
* Only record owners can view full details
* Nurses cannot view diagnosis content (masked only)

---

### 👥 Access Control

* Role-based access system:

  * **SuperAdmin**
  * **Doctor**
  * **Nurse**
  * **Patient**
* Implements:

  * Least privilege principle
  * Row-Level Security (RLS)
  * Controlled stored procedures

---

### 🔄 Secure Data Updates

* All updates to sensitive fields are:

  * Re-encrypted before storage
* Prevents plaintext exposure during updates

---

### 💾 Backup & Recovery

* Full recovery model enabled
* Supports:

  * Full backup
  * Differential backup
  * Transaction log backup
* Ensures **data recoverability**

---

### 📊 Auditing & Monitoring

* Tracks:

  * Login attempts
  * Data changes (DML)
  * Schema changes (DDL)
* Maintains tamper-resistant audit logs
* Supports point-in-time recovery

---

## ⚙️ Technologies Used

* Microsoft SQL Server
* T-SQL (Stored Procedures, Triggers, Views)
* Encryption (Symmetric & Asymmetric)
* Row-Level Security (RLS)

---

## 🚀 How to Run

1. Open SQL Server Management Studio (SSMS)

2. Execute scripts in order:

   * Database creation
   * Table creation
   * Security setup (keys, certificates)
   * Stored procedures & views
   * Auditing & backup configuration

3. Test using different roles:

   * SuperAdmin
   * Doctor
   * Nurse
   * Patient

---

## 📝 Key Functionalities

* Staff & patient can view their own data (decrypted)
* Doctors can add and update diagnosis securely
* Nurses can manage appointments but cannot see diagnosis
* Sensitive data always remains encrypted at rest

---

## 📚 Learning Outcomes

This project demonstrates:

* Database security implementation
* Encryption & key management
* Role-based access control
* Data masking techniques
* Auditing and compliance practices

---

## 💡 Highlights

* Real-world healthcare security simulation
* Multi-layered protection approach
* Strong separation of duties
* Fully auditable and recoverable system
