# DBMS Fundamentals

## MCA Placement Management System

### Objective

To create an ER model for managing the placement activities of MCA students.

## Main Entities

### Student

* Student_ID (PK)
* Name
* Email
* Phone
* CGPA
* Skills

### Company

* Company_ID (PK)
* Company_Name
* Address
* Contact_Email

### Job

* Job_ID (PK)
* Job_Title
* Salary
* Required_Skills
* Company_ID (FK)

### Application

* Application_ID (PK)
* Applied_Date
* Application_Status
* Student_ID (FK)
* Job_ID (FK)

### Interview

* Interview_ID (PK)
* Interview_Date
* Interview_Type
* Result
* Application_ID (FK)

### Placement

* Placement_ID (PK)
* Joining_Date
* Package
* Student_ID (FK)
* Company_ID (FK)

## Relationships

```text
COMPANY 1 ─── M JOB

STUDENT 1 ─── M APPLICATION M ─── 1 JOB

APPLICATION 1 ─── M INTERVIEW

STUDENT 1 ─── 1 PLACEMENT

COMPANY 1 ─── M PLACEMENT
```

## Simple ER Structure

```text
COMPANY
   |
  offers
   |
  JOB
   |
 receives
   |
APPLICATION
   |
  has
   |
INTERVIEW

STUDENT
   |
 applies
   |
APPLICATION

STUDENT
   |
 selected
   |
PLACEMENT
   |
 provided by
   |
COMPANY
```

## Conclusion

The ER model helps to organize student, company, job, application, interview, and placement information in the MCA Placement Management System.
