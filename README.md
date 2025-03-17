# Health Insurance Management System

## Overview
This project demonstrates the design and implementation of a relational database for a health insurance management system. The database structure is created using a **top-down approach**, focusing on key aspects of the system such as:
- Customer management
- Policy administration
- Claims processing
- Healthcare provider information
- Financial transactions  

The project involves creating several interconnected tables, establishing relationships between them, and defining user roles with specific permissions.

## Approach
This project utilizes a **top-down approach** to database design. We started by identifying the major entities and processes in a health insurance system, then broke these down into more specific components and relationships. This approach allowed us to create a comprehensive and cohesive database structure that effectively models the complexities of health insurance management.

## Project Structure
The project is structured around the following main entities:

- **Customers**: Stores customer information, including `CustomerID`, `FirstName`, `LastName`, `DOB`, `PhoneNumber`, and `Email`.
- **Policies**: Contains details about insurance policies such as `PolicyID`, `CustomerID`, `PolicyType`, `StartDate`, `EndDate`, and `PremiumAmount`.
- **Claims**: Tracks claim information, including `ClaimID`, `PolicyID`, `ClaimDate`, `ClaimAmount`, and `ClaimStatus`.
- **Hospitals**: Manages hospital information with fields like `HospitalID`, `HospitalName`, `Address`, and `PhoneNumber`.
- **Doctors**: Stores doctor details including `DoctorID`, `DoctorName`, `Specialty`, `PhoneNumber`, and `HospitalID`.
- **Hospitalizations**: Keeps track of patient hospitalizations, including `HospitalizationID`, `CustomerID`, `HospitalID`, `AdmissionDate`, `DischargeDate`, and `TotalCost`.
- **Treatments**: Records treatment information such as `TreatmentID`, `HospitalizationID`, `DoctorID`, `TreatmentDescription`, and `TreatmentCost`.
- **Payments**: Manages payment records with fields like `PaymentID`, `CustomerID`, `PaymentDate`, `PaymentAmount`, and `PaymentMethod`.

## Database Schema
The database schema includes the following tables:

- `Customers`
- `Policies`
- `Claims`
- `Hospitals`
- `Doctors`
- `Hospitalizations`
- `Treatments`
- `Payments`

Each table is designed with appropriate fields and data types to ensure efficient data storage and retrieval.

## Relationships
The database schema includes the following key relationships:

- **Customers to Policies**: One-to-Many
- **Policies to Claims**: One-to-Many
- **Customers to Hospitalizations**: One-to-Many
- **Hospitals to Hospitalizations**: One-to-Many
- **Hospitals to Doctors**: One-to-Many
- **Hospitalizations to Treatments**: One-to-Many
- **Doctors to Treatments**: One-to-Many
- **Customers to Payments**: One-to-Many

## Roles and Permissions
The system includes various user roles with different levels of access:

| Role | Permissions |
|------|------------|
| **Administrator** | Full access to all tables and data |
| **Insurance Agent** | Manage customer and policy information, create claims |
| **Claims Processor** | Process and update claims |
| **Healthcare Provider** | Manage hospitalizations and treatments |
| **Finance Officer** | Handle payments and financial records |
| **Customer Service Representative** | Access customer information and basic policy details |
| **Auditor** | Read-only access to all tables for audit purposes |
| **Customer** | Access to their own records (if implementing a customer portal) |

Each role has specific permissions designed to ensure **data security** and maintain the **principle of least privilege**.

## Contributors
- *Divyank Harjani - 055010*  
- *Priyadarshani Dash - 055037*  

---
