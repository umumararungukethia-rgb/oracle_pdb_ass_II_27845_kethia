Oracle Pluggable Database (PDB) Management Assignment II
Student Information
•	Student Name: Umunmararungu Kethia
•	Student ID: 27845
•	Course: Database Development with PL/SQL (INSY 8311)
•	Database: Oracle Database 21c XE
PDB Information
Permanent PDB
•	PDB Name: ke_pdb_27845
•	PDB User: Kethia_plsqlauca_27845
•	Status: READ WRITE
Temporary PDB
•	PDB Name: ke_to_delete_pdb_27845
•	Purpose: Created for testing PDB creation and deletion
•	Status: Successfully deleted
Tasks Completed
Task 1: Permanent PDB Creation
A permanent pluggable database named ke_pdb_27845 was created successfully from the PDB seed.
The PDB was opened successfully in READ WRITE mode.
A database user named Kethia_plsqlauca_27845 was created inside the PDB and granted the required privileges.
Evidence is available in:
screenshots/pdb_creation/
Task 2: Temporary PDB Creation and Deletion
A temporary PDB named ke_to_delete_pdb_27845 was created successfully and opened in READ WRITE mode.
The temporary PDB was then closed and deleted using:
ALTER PLUGGABLE DATABASE ke_to_delete_pdb_27845 CLOSE IMMEDIATE;

DROP PLUGGABLE DATABASE ke_to_delete_pdb_27845 INCLUDING DATAFILES;
The deletion was verified using a query against V$PDBS, which returned no rows for the deleted PDB.
Evidence is available in:
screenshots/pdb_deletion/
Task 3: Oracle Enterprise Manager
Oracle Enterprise Manager was accessed successfully and the dashboard was captured as evidence.
Evidence is available in:
screenshots/oem_dashboard/
Repository Structure
oracle_pdb_ass_II_27845_kethia/
│
├── README.md
│
└── screenshots/
    ├── pdb_creation/
    │   ├── 01_pdb_creation.png
    │   ├── 02_pdb_open_state.png
    │   └── 03_user_creation.png
    │
    ├── pdb_deletion/
    │   ├── 01_temp_pdb_creation.png
    │   └── 02_temp_pdb_deletion.png
    │
    └── oem_dashboard/
        └── 01_oem_dashboard.png
Issues Encountered
During the implementation, an initial PDB creation attempt produced an error because the required FILE_NAME_CONVERT clause was not specified. The issue was resolved by specifying the correct PDB seed and target datafile directories.
Another issue occurred when attempting to assign a quota on the USERS tablespace because the PDB did not contain a USERS tablespace. This command was therefore not required for the successful completion of the task.
Repository Link
GitHub Repository: [Insert your public GitHub repository URL here]
Conclusion
The required Oracle PDB management activities were completed successfully, including permanent PDB creation, user creation, temporary PDB creation and deletion, verification of PDB status, and Oracle Enterprise Manager dashboard access.

