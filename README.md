Multition Pay Application - README
Overview
The Multition Pay Application is a desktop app developed using the Kivy framework in Python. It serves as a personal time and salary management tool, allowing users to track work hours, calculate total salary based on a minimum wage, and navigate between months to manage historical data. The app features secure access through a PIN login system and persistent data storage using an Excel file.

Features
1. PIN Login System
Users must enter a 4-digit PIN (2256 by default) to access the app.
Incorrect PIN prompts an error popup.
2. Time and Salary Management
Interactive calendar for tracking daily work hours.
Calculates total salary based on entered hours and minimum wage.
3. Minimum Wage Setting
Users can set and update the minimum wage, which is saved persistently in an Excel file.
4. Persistent Data Storage
Work hours and wage details are stored in an Excel file (work_hours.xlsx) to ensure data is retained across sessions.
5. Dynamic Calendar
Displays the current month's calendar.
Highlights the current day.
Allows navigation to future months.
6. Excel Integration
Work hours and wage data are stored and retrieved using the openpyxl library.
Installation and Requirements
Prerequisites
Python 3.x installed on your system.
Required libraries:
kivy
openpyxl
(Optional) A virtual environment to manage dependencies.
Steps to Install
Clone or download the repository.
Install required dependencies:
pip install kivy openpyxl
Run the application:
python multition_pay.py
How to Use
Launching the App
Run the Python script (multition_pay.py).
Enter the PIN (2256) to access the main interface.
Setting Minimum Wage
Click the "Set Minimum Wage" button.
Enter the desired hourly wage and click "Save".
Adding Work Hours
Navigate to the desired date on the calendar.
Enter hours worked in the input box for that date.
The total salary will update automatically.
Navigating Months
Click "Next Month" to move to the following month's calendar.
Project Structure
multition_pay.py: Main application code.
work_hours.xlsx: Excel file storing wage settings and work hours.
Key Components
LoginPage
Provides a secure entry point with a PIN-based authentication system.
MainPage
Core functionality for calendar, wage management, and salary calculation.
Excel Integration
Uses the openpyxl library for persistent data storage and retrieval.
Development Details
Libraries Used
Kivy: For GUI development.
openpyxl: For managing Excel files.
os: For file handling.
datetime: For managing date and time.
calendar: For generating calendar layouts.
Future Enhancements
User Authentication:
Add user-specific profiles with different PINs.
Export Functionality:
Export work hour data to CSV or PDF.
Month Overview:
Display total hours and salary summary for each month.
Theming and Customization:
Allow users to customize app themes and layout.
Author
Developed by Meshack Tirop.

For more information, you can contact me via:

Email: mtirop345@gmail.com
GitHub: Meshack Tirop
License
This project is open-source and free to use under the MIT License.
