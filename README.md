This Prison Management System (PMS) is a Java-based desktop application designed to handle inmate records, staff attendance, and visitor logs. It utilizes a tiered access system to ensure that different roles have appropriate permissions within the facility.

🔑 Authentication and Roles
The system validates users through the DataStore class. Depending on the login, the Dashboard adapts its available features:

Admin (admin / 123): Has full access, including registering new inmates.

Staff (staff / 456): Can access attendance and visitor logs.

HR (hr / 789): Focused on records and high-level reports.

📋 Core Modules
1. Inmate Registration
Managed via the RegisterFrame, this module allows administrators to input critical data:

Personal Details: Name, Age, and distinguishing Marks.

Legal Info: Crime committed and sentence duration in years.

Location: Assignment to specific areas like "Block A" or "Block B".

Automated Logic: The system automatically calculates the Release Date by adding the sentence years to the current date.

2. Monitoring and Viewing
View All Inmates: The ViewFrame displays a list of all active inmates. Users can select a specific inmate to view their "Full Profile".

Search: Allows users to find a specific prisoner by their unique ID.

3. Facility Operations
The Dashboard provides buttons for daily operational tasks:

Staff Attendance: Log which staff members are currently on duty.

Visitor Log: Tracks visitors and generates a "Pass" associated with a specific inmate.

Daily Report: Provides a quick summary of the total number of inmates, staff present, and historical entries.

🛠️ Technical Structure
Main.class: The entry point that launches the login screen.

LoginFrame.class: Collects credentials and initiates the session.

Prisoner.class: The data model that stores individual inmate attributes and handles the date logic.

DataStore.class: A centralized repository that mimics a database, holding ArrayList collections for prisoners, attendance, and history.
