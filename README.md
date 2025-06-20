# Bank-Management-System

🔧 Project Overview
The Bank Management System is a Java-based application that simulates core functionalities of an online banking system. It allows customers to create accounts, perform transactions like deposits, withdrawals, fast cash, and check mini-statements. Admins can manage user data and review all transactions.

🛠️ Technologies Used
Frontend: Java Swing (GUI for desktop interface)

Backend: MySQL (relational database to store users, accounts, and transactions)

Connector: JDBC (Java Database Connectivity)

Tools: JDK, Eclipse/NetBeans, MySQL Workbench

🗂️ Modules Breakdown
1. User Interface (UI) Modules
These are built using Java Swing. Key UI classes:

Signup, Signup2, Signup3: For account registration, capturing personal, financial, and account type info.

Login: Allows users to log in using their card number and PIN.

Transactions: Main dashboard with options like Deposit, Withdraw, Fast Cash, Mini Statement, and Balance Inquiry.

Deposit, Withdrawl, FastCash: Transaction-specific interfaces.

MiniStatement, BalanceEquiry: Show transaction history or account balance.

2. Database Layer
Conn.java: Manages MySQL connectivity using JDBC. A shared class used across the project to execute SQL queries.

3. Backend Database Structure
Based on database file.txt, the following tables exist:

Table	Purpose
signup	Personal details from Signup Page 1
signuptwo	Financial and demographic data
signupthree	Account type, card number, PIN, and services selected
login	Stores login credentials
bank	Stores all transactions (deposit, withdraw, etc.)

✅ Core Functionalities Explained
🔐 User Registration
Involves 3 steps: personal details → additional info → account preferences.

Generates form number, card number, and PIN automatically.

Stores user data across signup, signuptwo, signupthree, and login tables.

🔑 Login
Validates user credentials (card number and PIN).

Redirects to the transaction dashboard on success.

💸 Deposit
Users enter the amount to deposit.

Stores record in bank table with type Deposit.

💵 Withdraw / Fast Cash
Similar to deposit, except transaction type is Withdraw.

Fast Cash provides preset values like ₹100, ₹500, etc.

📄 Mini Statement
Fetches and displays recent transactions from the bank table.

💼 Balance Enquiry
Calculates balance by summing all deposits and subtracting all withdrawals for a specific PIN.

🔐 Security Features
PIN-based authentication

Password/PIN changes

No plaintext password storage (though security could be enhanced with hashing, not currently implemented)

🧑‍💼 Admin Features (if extended)
Currently, the application focuses on user operations. But based on the project report, an admin module is suggested with:

Account overview

Transaction logs

User management

These would require additional UI and database handling for roles/permissions.

📈 Project Goals and Strengths
Automation: Eliminates need for manual records

User Satisfaction: Easy-to-use GUI

Transaction Management: Tracks deposits, withdrawals efficiently

Scalability: Modular design allows for easy future extension (e.g., mobile app, internet banking portal)

🧪 Testing & Validation
Input fields are validated (e.g., empty amounts, null fields in forms).

Error-handling via try-catch blocks.

GUI responds with dialog messages for success/failure.

🧭 Future Enhancements
Add mobile banking via Android/iOS app

Enable OTP/email notifications

Use encryption for PIN and passwords

Implement an admin dashboard

Introduce fund transfer functionality

