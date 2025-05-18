Table of Contents

- [Part A](#section-a-functional-and-non-functional-requirements-analysis)


# Section A: Functional and Non-Functional Requirements Analysis

## 1. Introduction
This document outlines the functional and non-functional requirements for a relational database system designed for a college. The system will manage **admins, teachers, students, and courses**, and will support:

- Course offerings by semester
- Student enrollment
- Teacher grade submissions
- Administrative oversight

---

## 2. Functional Requirements (FRs)
Functional requirements define what the system must do.

| ID   | Description                                                              | Role(s) Involved |
|------|---------------------------------------------------------------------------|------------------|
| FR1  | Admins can assign courses to teachers                                    | Admin            |
| FR2  | Admins can set which courses are offered each semester                   | Admin            |
| FR3  | Students can view and enroll only in available courses for the semester  | Student          |
| FR4  | Teachers can assign pass/fail grades to students                         | Teacher          |
| FR5  | The system must store user roles and enforce role-specific permissions   | All roles        |
| FR6  | The system must track course offerings by semester                       | Admin            |
| FR7  | The system must store enrollment records for each student                | System           |

---

## 3. Non-Functional Requirements (NFRs)
Non-functional requirements describe how the system should perform and behave.

| ID    | Description                                                                 | Category         |
|-------|------------------------------------------------------------------------------|------------------|
| NFR1  | System should respond to course and enrollment queries in < 2 seconds       | Performance      |
| NFR2  | System should support up to 1000 users simultaneously                       | Scalability      |
| NFR3  | Role-based access must restrict unauthorized actions (e.g., students grading) | Security         |
| NFR4  | Weekly backups must be possible via MySQL utilities                         | Reliability      |
| NFR5  | Database schema should follow 1NF and 2NF to ensure data consistency        | Maintainability  |
| NFR6  | System should be usable with minimal training                               | Usability        |

---

## 4. How to Distinguish FRs vs. NFRs – A Guide

### Functional Requirements (FRs)
- Define **what the system does** (features, tasks, rules)
- Often relate to **user actions or business logic**
- Can often be written as **user stories**  
  > e.g., *“As a teacher, I want to grade students so that I can complete my teaching responsibilities.”*

#### Checklist for FRs:
- [ ] Is it a core task or action?
- [ ] Is it role-based behavior?
- [ ] Is it directly observable by the user?
- [ ] Does it define a process or function?

---

### Non-Functional Requirements (NFRs)
- Define **how the system behaves**
- Focus on system **quality attributes**
- Impact the **performance, usability, security**, and **reliability**

#### Checklist for NFRs:
- [ ] Is it about system performance or response time?
- [ ] Is it related to availability, security, or maintainability?
- [ ] Does it describe system quality or metrics?
- [ ] Is it invisible to users but affects their experience?

---

### Mnemonic: FURPS+
Helps remember types of NFRs:

- **F**: Functionality  
- **U**: Usability  
- **R**: Reliability  
- **P**: Performance  
- **S**: Supportability  
- **+**: Security, Scalability, Maintainability, etc.

---

## 5. Summary
Understanding the distinction between **functional** and **non-functional** requirements is crucial in system design. Clearly identifying these ensures that the system is both capable and maintainable. This guide serves to be a reusable resource for future MySQL RDBMS design projects.

---