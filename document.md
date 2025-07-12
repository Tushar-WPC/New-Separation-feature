✅ Use Case Title:
Separate Students from Hostel

🎯 Objective:
To provide hostel administrative staff with a streamlined interface to view, filter, and separate students from hostel accommodation based on the selected academic session, hostel, and financial ledger (balance sheet). This ensures accurate tracking of student movement and updates their status in the hostel records accordingly.

👤 Primary Actor:
Admin (Office/Hostel Department Staff)

📌 Preconditions:
At least one student must be admitted to the selected hostel for the given academic session.

Hostel master data and associated Balance Sheet configurations must be set up and active in the system.

User must have valid permissions to access and perform student separation actions in the hostel module.

📈 Basic Flow (Main Success Scenario):
Admin navigates to:
ERP → Hostel Module → Separation of Students

Admin selects the following filters:

Session (Dropdown) – Active academic session

Hostel Name (Dropdown) – Target hostel

Balance Sheet (Dropdown) – Relevant accounting ledger

Admin clicks the SHOW button.

System fetches and displays a list of hostel-admitted students matching the criteria, with the following columns:

✅ Select (Checkbox) (with "Select All" master checkbox)

Sr. No.

Student PRN

Student Name

Hostel Type (e.g., Boys, Girls, Staff)

Separation Date (Editable per student)

Admin performs one of the following:

Selects individual checkboxes next to student rows

Uses Select All to mark all visible students

Admin clicks the SEPARATE button.

System:

Validates the selection

Updates the status of selected students to "Separated"

Records the Separation Date

Updates hostel occupancy and downstream reports

A confirmation message is displayed:

“✅ Selected students have been successfully separated from the hostel.”

⚠️ Alternate Flows:
No students found:
If no student data is returned for the selected filters, system shows:

“⚠️ No records found.”

No selection made:
If SEPARATE is clicked without selecting any checkbox, system displays:

“⚠️ Please select at least one student to proceed.”

Invalid or missing separation date:
System validates that each selected student has a valid separation date before submission.

💥 Postconditions:
Selected students are officially marked as separated in the ERP database.

Their hostel accommodation record is deactivated or archived based on the separation date.

Related hostel occupancy statistics, billing, and capacity reports are updated accordingly.

📊 Field Overview:
🔽 Input Fields (Filter Section)
Field Name	Type	Description
Session	Dropdown	Select the academic session
Hostel Name	Dropdown	Select the target hostel
Balance Sheet	Dropdown	Select the associated financial ledger

🧾 Student List Table Columns
Column Name	Description
✅ Checkbox	For selecting students; includes “Select All” at the top
Sr. No.	Serial number of each listed student
Student PRN	Permanent Registration Number (unique student identifier)
Student Name	Full name of the student
Hostel Type	Type/category of hostel assigned (e.g., Boys, Girls, Staff)
Separation Date	Date of separation (editable per student row before submission)

🖼️ UI Structure (Text Diagram for Visualization)

----------------------------------------------------------------------------------------------------------------------
|                                            📌 Separate Students from Hostel                                        |
----------------------------------------------------------------------------------------------------------------------

| Session:       [ Select Session ▼ ]   Hostel Name: [ Select Hostel ▼ ]     | Balance Sheet: [ Select Balance ▼ ]   |
|                                                                                                                    |
|                                                   [    SHOW    ]                                                   |
----------------------------------------------------------------------------------------------------------------------

📋 Students List:

[✓] Select All

| [✓]  | Sr. No. | Student PRN      | Student Name       | Hostel Type | Separation Date  |
|------|---------|------------------|--------------------|-------------|------------------|
| [ ]  |   1     | PRN202300001     | Aarya Kulkarni     | Cyber       | [DD/MM/YYYY]     |
| [ ]  |   2     | PRN202300002     | Rohan Deshmukh     | Boys        | [DD/MM/YYYY]     |
| [ ]  |   3     | PRN202300003     | Meena Patil        | Girls       | [DD/MM/YYYY]     |
| ...  |  ...    | ...              | ...                | ...         | ...              |

---------------------------------------------------------------------------------------------------------------------
                                 [   SEPARATE   ]
----------------------------------------------------------------------------------------------------------------------

✅ Note:
- Use checkboxes to select students to be separated.
- You can edit the Separation Date before separating.
- Press SEPARATE to finalize the separation process.

📌 Additional Recommendations (Optional Enhancements for Future):
✅ Add Export to Excel button to download filtered results.

🔍 Enable search/filter within the student list (by PRN or Name).

📆 Allow bulk date selection for separation date.

📋 Add status column (e.g., Already Separated vs Active).

🔐 Audit log for tracking who separated which students and when.
