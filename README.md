# AttendanceMarker
Attendance Management System
Overview
This Python-based project allows you to mark and track attendance for students using an Excel file, and also calculate custom attendance points based on specific dates (e.g., Mondays and Tuesdays). The project includes functionality to:

Mark attendance for a specific date.
Save the attendance data back to the Excel file.
Assign points for attendance on different days (with custom values for Mondays and Tuesdays).
Automatically calculate total points for each student based on their attendance records.
Requirements
Python 3.x
Pandas library
Setup Instructions
Ensure you have Python installed on your system.
Install the required Pandas library using the following command:

pip install pandas
Place the Excel sheet with the student names and roll numbers in the same directory as the script. The Excel file should have the following structure:
A column named Roll Number.
A column named Name.
Optional: Columns for existing attendance records.

Usage
1. Marking Attendance
To start marking attendance:

Run the script and the take_attendance() function will prompt you to input the date for marking attendance.
You will be prompted to mark each student as Present or Absent by entering 'y' or 'n' for each roll number.
The attendance will be recorded in the Excel sheet under the specified date.

# Start marking attendance for the specified date(s)
take_attendance()

# After completing, save the updated Excel file
save_attendance()
2. Calculating Attendance Points
The script allows you to assign custom points for attendance on Mondays and Tuesdays:

Mondays: 2 points for attendance.
Tuesdays: 3 points for attendance.
Other Days: 1 point for attendance.

(Award pointa accordingly to number of hours to be completed per semester)
The function calculate_attendance_with_custom_points() calculates the total points based on the attendance records.

# Calculate the attendance points for each student
calculate_attendance_with_custom_points()

# Save the updated Excel file with total points
save_updated_sheet()
3. Saving Attendance Data
After marking attendance or calculating points, the data can be saved to the Excel file using the save_attendance() or save_updated_sheet() functions. These functions update the Excel sheet with the new attendance data and points, respectively.

Key Functions
take_attendance()
This function allows the user to input attendance for a specific date and update the Excel sheet with attendance status (Present/Absent).

mark_attendance_for_date(date_column)
Helper function that marks attendance for a specific date by asking the user to input the attendance for each student.

calculate_attendance_with_custom_points()
This function calculates total points for each student based on attendance on specific days (Mondays and Tuesdays with custom points, and 1 point for other days).

save_attendance() and save_updated_sheet()
These functions save the updated Excel sheet with attendance data and points.
