# Campus Network Complaint System  
*A Database-Oriented Complaint Management Solution*

---

## 1. Problem Statement
- The **Campus Network Complaint System** is a database-driven application.
- Enables **students and staff** to:
  - Register network-related complaints.
  - Track the status of complaints.
- Enables **network administrators** to:
  - Manage complaints efficiently.
  - Assign complaints to technicians.
  - Resolve issues using CRUD operations.
- Handles:
  - Wi-Fi issues
  - LAN problems
  - Slow internet
  - Network outages
- Ensures transparency, efficiency, and accountability.

---

## 2. Stakeholders

### a) Students / Staff
- Register network complaints.
- Provide issue details and exact location.
- View complaint status.
- Track resolution progress.

### b) Network Administrator
- View all registered complaints.
- Assign complaints to technicians.
- Update complaint status.
- Maintain user and technician records.
- Generate reports.

---

## 3. Data to be Collected

### A. User Information (Students / Staff)
**Attributes:**
- User ID *(Primary Key)*
- Name
- Role *(Student / Faculty / Staff)*
- Roll Number / Employee ID
- Department
- Phone Number
- Email ID
- Hostel / Block / Building

---

### B. Network Location Details
**Attributes:**
- Location ID *(Primary Key)*
- Building Name *(Hostel / Academic Block / Library)*
- Floor Number
- Room / Lab Number

---

### C. Complaint Details
**Attributes:**
- Complaint ID *(Primary Key)*
- User ID *(Foreign Key)*
- Location ID *(Foreign Key)*
- Complaint Type:
  - No Internet
  - Slow Speed
  - Disconnection
- Complaint Description
- Complaint Date
- Priority:
  - Low
  - Medium
  - High
- Status:
  - Pending
  - In Progress
  - Resolved

---

### D. Technician / Admin Details
**Attributes:**
- Technician ID *(Primary Key)*
- Name
- Phone Number
- Email ID
- Assigned Area
- Availability Status

---

### E. Complaint Assignment Details
**Purpose:** Tracks technician assignments

**Attributes:**
- Assignment ID *(Primary Key)*
- Complaint ID *(Foreign Key)*
- Technician ID *(Foreign Key)*
- Assigned Date
- Resolution Date
- Remarks

---

## 4. Functional Requirements
- Allow users to register network complaints.
- Store complaint details in the database.
- Display complaint status to users.
- Assign complaints to technicians.
- Update complaint status after resolution.
- Maintain user and technician records.
- Generate complaint reports.

---

## 5. Non-Functional Requirements
- Ensure data integrity and consistency.
- Only administrators can assign complaints.
- Prevent duplicate complaints.
- Maintain database normalization.
- Support fast data retrieval.

---

## 6. Constraints
- Each complaint must belong to a valid user.
- Each complaint must have exactly one current status.
- A technician can handle multiple complaints.
- A complaint can be assigned to only one technician at a time.
- Status flow must follow:
  - **Pending → In Progress → Resolved**

---
