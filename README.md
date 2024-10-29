
                                                           Hospital Management System 


Overview
This is a basic Hospital Management System developed in C. It assists in managing some modules of patient records such as new patients, their details, searching specific patients, editing patient’s detail, and finally the patient being checked out with their bills paid.
The project enables you to keep a record of patients in the hospital and those who visit the hospital on a day today basis, making it possible to maintain patient records as applicable in small hospitals.
Features
•	Add Patient Record: A record of the patient’s ID number, name, age, sickness, and visit purpose (Admitted/Daily) should be filled.
•	Display All Records: Examine each patient record and all the records in possession all in a single table.
•	Search Record: A patient’s unique ID can be used to search for them and return their information.
•	Edit Record: Changed information of a certain patient can be saved in the system.
•	Discharge Patient: Admit patients who are not in the hospital or patients who visit the hospital on a daily basis with the summation of the number of days admitted in hospital or the consultation charge on a daily basis.
•	Billing System: The bills of each and every patient is computed depending on the number of days a patient is admitted in hospital or a set amount of money for consultation on an every day basis.
Installation and Usage
Prerequisites
•	C language compilers e.g. GCC
•	Terminal/command prompt to run the software




Menu Options
1.	Add Record: Feed information about the patient: his/her ID, full name, age, illness, visit type and the relevant dates as required. This information is to be saved in the memory of the system and will be accessed when required.
2.	Display Records: List all the details of the patients who exist at the moment, their ID, name, age, disease, visit type and dates of appointments or admissions to the hospital.
3.	Search Record: Type in the ID of a patient you want to target for deletion to verify their details. If the patient is in the data base, their particulars will come up.
4.	Edit Record: Alter some of the patient’s information that has already been recorded by looking for the patient’s ID.
5.	Discharge Patient: Remove a patient from the system using their ID and Creating a receipt according to the patient’s nature of visit (ie ADMITTED or DAILY). When a patient has been discharged, their record is eradicated.
6.	Exit: Officially quit the program.








Code Structure

- `struct Patient`: A structure to hold patient records (ID, name, age, disease, visit type, etc.).
- `MAX_PATIENTS`: The maximum number of patients the system can hold (100 by default).
- `mainMenu()`: Main function that displays the menu and handles user input.
- `addRecord()`: Adds a new patient record.
- `displayRecords()`: Displays all patient records in a table format.
- `searchRecord()`: Searches for a patient by their unique ID.
- `editRecord()`: Allows editing of patient details.
- `dischargePatient()`: Handles patient discharge and bill calculation.
- `findPatientById()`: Helper function to find a patient by their ID.
- `clearScreen()`: Clears the console screen (uses `cls` for Windows, modify to `clear` for Linux).
- `pauseAndClear()`: Pauses the system to allow the user to read the output, then clears the screen for further input.

## Billing System

- Daily Patients: Fixed daily consultation fee of $50.
- Admitted Patients: The cost of admission is $200 per day, multiplied by the number of days the patient was admitted.

 How to Customize

- MAX_PATIENTS: You can change the maximum number of patient records by altering the `#define MAX_PATIENTS 100` line.
- Billing Fees: You can adjust the fees for daily patients or admitted patients by modifying the constants `DAILY_FEE` and `ADMISSION_FEE`.
- Screen Clear Function: The code currently uses `system("cls")` to clear the screen, which is compatible with Windows. For Linux/Mac systems, change it to `system("clear")`.

Known Limitations

- The system does not persist data between runs; all records are stored in memory, so once the program is closed, all records are lost.
- The system can only store up to 100 patients, as defined by `MAX_PATIENTS`.

Future Improvements

- File Storage: Add functionality to save and retrieve patient records from a file.
- Database Integration: Connect the system to a database like MySQL or SQLite for larger and persistent data storage.
- Graphical User Interface (GUI): Implement a GUI version of the system for a better user experience.
- Enhanced Billing: Add more flexible billing options and support for multiple visit types.

License

This project is open-source and free to use under the [MIT License](https://opensource.org/licenses/MIT).

 Contributing

Feel free to fork this project, open issues, or submit pull requests. Any contributions towards improving the project are greatly appreciated.

---
Contact

If you have any questions or suggestions, please feel free to reach out.

