## Appointment creation system for a clinic
### 1. Introduction
##### 1.1. Purpouse
Design a system that allows the personal to ease the the way appointments are administrated in the clinic. Obtaining data, date of appointment, clinical trial to be done to the client, ect. As in the past they could only handle these situations with old methods by using paper and pens, writting every appointment.

The use of this system is intended to be used by the administrarive personal in the clinic that takes the role of attending the clients and creating the appointments and doing their desired clinical trials* in the specified date.
##### 1.2. Scope
The system allows a receptionist to generate an appointment for a particular client by capturing his information.
The system should be able to generate a appointment for, first the clinic with information of the client cointaining basic and some personal information like, name, age, trial, may be another extra requirements needed depending of the clinical trial to be done; Second the client should obtain only the information about when to come for the trial, as other information about the appointment.
The data should be saved in a database to avoid the loss of data.
The system is intended to aid an speed up work performance.

##### 1.3	Definitions, acronyms, and abbreviations
Some of the main concepts that are worked in the clinic,
* Clinic:
Can be refer to a general medical practice, run by one or more general practitioners, but it could also mean a specialist clinic.
Its a process oriented to a diagnostic like a disease, disorder, etc. 
* General practitioner:
In the medical profession is consiered a medical doctor who treats acute an chronic illnesses and provides preventive care and health education.
* Clinical trial:
In a general sense it can be defined as physical, chemical or microbiologic studies that aids the diagnostic and medical treatment, and these practices are done by doing samples like urine, blood to investigate a posible abnormality.
* Laboratory:
Its a place where a team of specialized members in the area like medics, analists, technical analists, do human biologic samples.
* Hematology:
Is the branch of medicine concerned with the study of cause, prognosis, treatment, and prevention of diseases related to blood.
* Immunology:
A branch of biology that covers the study of immune systems in all organisms.
* Microbiology:
Is the study of microorganisms, those being unicellular(single cell), multicellular(cell colony), or acellular(lacking cells).
Patient: 
Usually will be the customer to take a clinic trial
##### 1.4	References 
Análisis Clínicos. April 5, 2019, from EcuRed:
https://www.ecured.cu/An%C3%A1lisis_Cl%C3%ADnicos

(2017) ANALISIS CLINICOS. April 5, 2019, from Grupo quimico:
http://grupoquimico.com.mx/pdf/art1.pdf
##### 1.5	Overview
The rest of this document will cointain information of the system. 
Section 2 will give an overall description of the system, it will talk about the people involved in it, what will the system will be expected to do, functions and constraints.
Section 3 will focus on the specific requirements the system has to deliver.
### 2. Overall Description
##### 2.1. Product Perspective
This system consists of a application that will save a number of appointments each one with a set of customer information in a database.
Each time the employee has to create, modify or delete, there will be a number of components in the interface so the system can communicate with the database and apply these changes.
##### 2.2	Product Functions
Main actions that the system should perform:
* Create, modify and delete patient information
* Generate a reports that contains the costs of the clinical trial
* Manage information of the doctors in the clinic and patients assigned
* Manage users (employee data and information) into system
* Manage trial information (prices, trial available)
##### 2.3	User characteristics
| User    | Details           |
| ------------- |:-------------:|
| Employee | The employee will play the role of capturing customer data, also modifying any data. They will be also working with the doctor's data(add patients, add doctors, modify doctor information). |
| Administrator   | The administrator of the system will play a greater role by modifying and adding trials, it will also take control of the users on the system that are the employees.  | 
##### 2.4	Constraints
--
##### 2.5	Assumptions and dependencies
* An Administrator should be able to modify all the data that the employee(user) can.
* One employee should be using the system at the time
### 3.	Specific requirements
The specific actions that the system shall do will be described in this section.
##### 3.1 External interfaces
All the visual elements on the system will be described here, and how the system itself will look to the employee.
* Startup
The first screen of the system should be met with a login screen where the employee should input his password given by the administrator
* Main menu
  - At top view there should be met a number of tabs where the employee should be able to access to create modify and delete data
  - Tabs:
    1. Patients
    2. Doctors
    3. Users
    4. Clinic trials
  - Consider that only the administrator should be able to access the "Clinic trials" and "Users" tabs, since only them can modify this data
  - A logout button should be present
* Patient tab
  - This particular screen should have the following sections:
    1. Search bar along with a "Search" button
    2. "New" button
  - A table containing all the current patients with the following information on each:
    1. Name
    2. Gender
    3. Date of birth
    4. Age
    5. Actions
  - In the actions section of the table two buttons should be there these allow to edit and create a new trial for the customer.
  - The buttons are:
    1. Edit
    2. New Trial
* Doctor tab
  - This screen features the doctors in a table available on the clinic
  - It contains the following elements:
    1. "New" button
    2. Inside the table a sub-section called "Actions" features two buttons: "Edit" and "See assigned patients"
* Trials tab
  - Only available for the administrators of the system
  - Features all the costs and available trials at the clinic in a table
  - The table contains the elements "Trial name", "Price" and "Actions"
  - The "Actions" sections features one button:
    1. Edit
  - they can be modified in terms of prices and details
* User Tab
  - This screen features a table with details of all the current users and administrators in the system
  - Only the administrator is allow to modify the information on this screen
  - New users can be created with the "New user" button
  - The table features the sections:
    1. Name
    2. Phone
    3. User rights
    4. Status
    5. Actions
  - The "Actions" sections features a "Edit" button that allow to modify the user data and "Delete user" to delete all user information in the system
##### 3.2 Functions
Here all the descriptions of the actions that can be done in the systems are stated here.
* Functional requirements

* Non-functional requirements
