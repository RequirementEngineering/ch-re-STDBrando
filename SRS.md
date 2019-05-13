## Appointment creation system for a clinic
## 1. Introduction
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

| Term        | Definition           |
| ------------- |:-------------:|
| Clinic     | Can be refer to a general medical practice, run by one or more general practitioners, but it could also mean a specialist clinic. Its a process oriented to a diagnostic like a disease, disorder, etc. |
| General practitioner      |   In the medical profession is consiered a medical doctor who treats acute an chronic illnesses and provides preventive care and health education.    |
| Clinical trial |   In a general sense it can be defined as physical, chemical or microbiologic studies that aids the diagnostic and medical treatment, and these practices are done by doing samples like urine, blood to investigate a posible abnormality.    |
| Laboratory | Its a place where a team of specialized members in the area like medics, analists, technical analists, do human biologic samples. |
| Patient | Usually will be the customer to take a clinic trial. |

##### 1.4	References 
Análisis Clínicos. April 5, 2019, from EcuRed:
https://www.ecured.cu/An%C3%A1lisis_Cl%C3%ADnicos

(2017) ANALISIS CLINICOS. April 5, 2019, from Grupo quimico:
http://grupoquimico.com.mx/pdf/art1.pdf
##### 1.5	Overview
The rest of this document will cointain information of the system. 
Section 2 will give an overall description of the system, it will talk about the people involved in it, what will the system will be expected to do, functions and constraints.
Section 3 will focus on the specific requirements the system has to deliver using use case diagrams.
## 2. Overall Description
##### 2.1. Product Perspective
This system consists of a application that will save a number of appointments each one with a set of customer information in a database.
Each time the employee has to create, modify or delete, there will be a number of components in the interface so the system can communicate with the database and apply these changes.
##### 2.2	Product Functions
Main actions that the system should perform:
* Create, modify and delete patient information
* Manage information of the doctors in the clinic and patients assigned
* Manage users (employee data and information) into system
* Manage trial information (prices, trial available)
##### 2.3	User characteristics
| User    | Details           |
| ------------- |:-------------:|
| Employee | The employee will play the role of capturing customer data, also modifying any data. They will be also working with the doctor's data(add patients, add doctors, modify doctor information). The employee can be also considered as a regular user on the system. |
| Administrator   | The administrator of the system will play a greater role by modifying and adding trials, it will also take control of the users on the system that are the employees.  |
| Doctor | The doctor has a less important role in the process but just attend the client or know which clients took his trial. |
##### 2.4	Constraints
- The employees in the clinic might not be experienced enough to use the system, so a little extra time is recommended to understand the use of the system.
- Its important for the employees and administrator to have their passwords at hand since with these they can access the system.
##### 2.5	Assumptions and dependencies
* An Administrator should be able to modify all the data that the employee(user) can.
* The user should be able to work only with creating patient information, adding or modifying doctor information.
* One employee should be using the system at the time.
* 
## 3.	Specific requirements
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
    3. add trial
    4. generate report
  - A table containing all the current patients with the following information on each:
    1. Name
    2. Gender
    3. Date of birth
    4. Age 
    5. assigned trials
* Doctor tab
  - This screen features the doctors in a table available on the clinic
  - It contains the following elements:
    1. "Add" button
    2. "Edit" button
  - A table cointaining all the current doctors available will be shown with the following information
    1. Name
    2. Phone No.
    3. Email
    4. Address
    5. Assigned patients
* Trials tab
  - Only available for the administrators of the system
  - Features all the costs and available trials at the clinic in a table
  - The table contains the elements "Trial name" and "Price"
  - It contains two buttons:
    1. Add
    2. Edit
  - they can be modified in terms of prices and details
* User Tab
  - This screen features a table with details of all the current users and administrators in the system
  - Only the administrator is allowed to modify the information on this screen
  - It contains the following elements:
    1. "Add" button
    2. "Edit" button
  - The table features the sections:
    1. Name
    2. Phone
    3. User rights (Regular or Administrator)
    5. Actions

##### 3.2 Functions
A general description of the system function its described here.
* Functional requirements
* Administrator
  - The administrator shall be able to do everything the employee (user) can
  - The system shall allow the administrator to create a new user
  - The system shall allow the administrator to modify the user information
  - The system shall allow to add new clinic trial information
  - The system shall allow to modify clinic trial information
  - The system shall allow to delete clinic trial information

* Employee
  - The system shall create/add new patient information
  - The system shall search for a particular patient
  - The system shall add a trial to a patient
  - The system shall modify patient information
  - The system shall add new doctor information
  - The system shall seatch for a particular doctor information
  - The system shall modify doctor information
  - The system shall allow to see the patient assigned to a doctor
  
Use cases:
![alt text](https://github.com/RequirementEngineering/ch-re-STDBrando/blob/master/Images/UseCase%20Login.png "Login")

 | Name:    | Login |           
| --- | --- |
 Actors: | Employee, Administrator 
 Pre-conditions: | Have a Password 
Description: | Allows the employee or administrator to login into the system 
- Main scenario:   
1. The actor should press the login button on the main screen, after that input his user name and password.
2. The system will verify if the password and user name exists or are correct and login into the system.
- Alternative scenario:  
1. The system detects that the user name or password are not correct or do not exist in it and shows a error message, telling the actor the information introudced are not correct. 

![alt text](https://github.com/RequirementEngineering/ch-re-STDBrando/blob/master/Images/UseCase%20Patient.png "Patient")

Name:    | Add patient            
| --- | --- |
 Actors: | Employee
 Pre-conditions: | Have logon into the system 
Description: | Allows the employee to add a new patient on the system
- Main scenario:   
1. The employee selects the "add" button in the patient tab.
2. The system will show the spaces to fill with their respective information.
3. The employee fill the empty spaces with the patient information.
4. The system verifies if all the spaces have been filled and saves them.
- Alternative scenario:  
1. The system verifies if all the spaces are filled or if the information is correct, if a space is missing or a certain data is invalid the system will advise the employee of it and will allow the employee to fix it.

Name:    | Search patient            
| --- | --- |
 Actors: | Employee
 Pre-conditions: | Have logon into the system 
Description: | Allows the employee to do a search of a specific patient in the list.
- Main scenario:   
1. The employee selects the empty box where he/she can input the name of a specific patient.
2. System checks if there are any coincidence of names with the one the employee writed and shows it.
- Alternative scenario:  
1. The system checks if there are any coincidences in the list, if none is found the system will show a error message showing that the specified name could not be found.

Name:    | Modify patient data           
| --- | --- |
 Actors: | Employee
 Pre-conditions: | Have logon into the system 
Description: | Allows the employee to change a patient information.
- Main scenario:   
1. The employee selects the patient he/she wants to modify in the patient tab.
2. The employee selects the edit button.
3. The system shows the current data of the patient.
4. The employee does the necessary changes to the patient information.
5. The system checks the changes and saves.
- Alternative scenario:  
1. The system checks if there any wrong data in the patient, it will tell the employee about it and will allow to fix it.

Name:    | Add trial to patient           
| --- | --- |
 Actors: | Employee
 Pre-conditions: | Have logon into the system 
Description: | Allows the employee to add a new trial to the patient history.
- Main scenario:   
1. The employee selects the patient which he/she wants to add a new trial
2. The employee selects the button modify history
3. The employee adds a new trial to the patient history
4. The system checks the selection and saves.
- Alternative scenario:  
1. The system checks the changes to the data, if any of these is not correct, the system will tell the employee about it. 

![alt text](https://github.com/RequirementEngineering/ch-re-STDBrando/blob/master/Images/UseCase%20Doctor.png "Doctor")

|Name:    | Add doctor |           
| --- | --- |
 Actors: | Employee
 Pre-conditions: | Have logon into the system 
Description: | Allows the employee to add a doctor to the system.
- Main scenario:   
1.  The employee selects the add button on the doctor tab.
2. The system shows the spaces to fill.
3. The employee adds the doctor information.
4. The system checks the information and saves.
- Alternative scenario
1. The system checks if the information is correct, if any data is wrong the system tells the employee about it and allows him to fix it.

Name:    | Search Doctor           
| --- | --- |
 Actors: | Employee
 Pre-conditions: | Have logon into the system 
Description: | Allows the employee to do a search of a specific Doctor in the list.
- Main scenario:   
1. The employee selects the empty box where he/she can input the name of a specific Doctor.
2. System checks if there are any coincidence of names with the one the employee writed and shows it.
- Alternative scenario:  
1. The system checks if there are any coincidences in the list, if none is found the system will show a error message showing that the specified name could not be found.

Name:    | Modify doctor data           
| --- | --- |
 Actors: | Employee
 Pre-conditions: | Have logon into the system 
Description: | Allows the employee to change a doctor information.
- Main scenario:   
1. The employee selects the doctor he/she wants to modify in the patient tab.
2. The employee selects the edit button.
3. The system shows the current data of the doctor.
4. The employee does the necessary changes to the doctor information.
5. The system checks the changes and saves.
- Alternative scenario:  
1. The system checks if there any wrong data in the doctor information, it will tell the employee about it and will allow to fix it.

Name:    | See doctor assigned patients          
| --- | --- |
 Actors: | Employee
 Pre-conditions: | Have logon into the system 
Description: | Allows the employee to see the patients that will take a trial with the specified doctor.
- Main scenario:   
1. The employee selects the doctor which he/she wants to see the assigned patients.
2. The employee selects the check patients button.
3. The system shows the list of patients.
- Alternative scenario:  

![alt text](https://github.com/RequirementEngineering/ch-re-STDBrando/blob/master/Images/UseCase%20Trials.png "Trial")

|Name:    | Add trial |           
| --- | --- |
 Actors: | Administrator
 Pre-conditions: | Have logon into the system 
Description: | Allows the administrator to add a trial to the system.
- Main scenario:   
1.  The administrator selects the add button on the trial tab.
2. The system shows the spaces to fill.
3. The administrator adds the new trial information.
4. The system checks the information and saves.
- Alternative scenario
1. The system checks if the information is correct, if any data is wrong the system tells the administrator about it and allows him to fix it.

Name:    | Modify trial          
| --- | --- |
 Actors: | Administrator
 Pre-conditions: | Have logon into the system 
Description: | Allows the administrator to change a trial information.
- Main scenario:   
1. The administrator selects the trial he/she wants to modify in the patient tab.
2. The administrator selects the edit button.
3. The system shows the current data of the trial.
4. The administrator does the necessary changes to the trial information.
5. The system checks the changes and saves.
- Alternative scenario:  
1. The system checks if there any wrong data in the trial information, it will tell the administrator about it and will allow to fix it.

![alt text](https://github.com/RequirementEngineering/ch-re-STDBrando/blob/master/Images/UseCase%20users.png "Users")

|Name:    | Add user |           
| --- | --- |
 Actors: | Administrator
 Pre-conditions: | Have logon into the system 
Description: | Allows the administrator to add a new user to the system.
- Main scenario:   
1.  The administrator selects the add button on the users tab.
2. The system shows the spaces to fill.
3. The administrator adds the new user information.
4. The system checks the information and saves.
- Alternative scenario
1. The system checks if the information is correct, if any data is wrong the system tells the administrator about it and allows him to fix it.

Name:    | Modify user         
| --- | --- |
 Actors: | Administrator
 Pre-conditions: | Have logon into the system 
Description: | Allows the administrator to change a user information.
- Main scenario:   
1. The administrator selects the user he/she wants to modify in the users tab.
2. The administrator selects the edit button.
3. The system shows the current data of the user.
4. The administrator does the necessary changes to the user information.
5. The system checks the changes and saves.
- Alternative scenario:  
1. The system checks if there any wrong data in the user information, it will tell the administrator about it and will allow to fix it.
   
  ## Appendix
  ##### Elicitation process
The process followed to obtain the requirements of the system was to do an interview to the owner of the clinic. He wanted a system  capable of making the administrative apartment to be more efficient, since as time has passed the clinic has gotten more clients and he feels that the old methods that involved the use of pen and paper might not be enough.
After the main questions were done, I’ve decided to reach a more open minded interview of what the client would want and I reached to the following conclusions:

* Conclusions
-	The client decided of a system based on tabs with these respective names: Patients, Doctors, Users, Trials (or also clinic trials)
-	The client requested that in most tabs, the employee should be able to change most information of a client, a doctor, check all clinical trials information (name, price, etc.)
-	The doctors do not have a big involvement in the process but to be aware of what clients he has, and when are the appointment dates that they should attend
-	The client wanted a simple user/administrator system where the administrator would be a specific
-	Since the way the system is looking it will be necessary to create a database where the patient, doctor, trial information will be stored
* Process
1. A patient requests a trial, first off the employee should fill up information on the client and save it, add his trial(s) in the patient history and the employee Will assign the patient to their respective doctor in the requested trial, the patient will be told to come until the next scheduled appointment.
Until the date of the scheduled appointment the patient will come to take his trial with the doctor and do the necessary studies to the patient, finally the employee will erase the patient information on the system unless the patient requested to take more than one trial in his history.
* Other
1. If a patient desires it he can request a change to his requested trial, for that the employee should only select the client information, and check his trial history and do the changes.
2. The employee can add and remove patients that a doctor will attend.
3. The administrator will be taking control of most of the system, adding and removing user data
4. The employee logs into the system, inputs his password and username, succefully logs in. In case not, the employee should reach the administrator to fix the issue.
##### Business Process Diagrams
![alt text](https://github.com/RequirementEngineering/ch-re-STDBrando/blob/master/Images/ClinicBPM.png "Main process")
![alt text](https://github.com/RequirementEngineering/ch-re-STDBrando/blob/master/Images/cliniLoginBPM.png "Login sub process")
![alt text](https://github.com/RequirementEngineering/ch-re-STDBrando/blob/master/Images/clinicTrialBPM.png "Trial data Sub Process")
  
