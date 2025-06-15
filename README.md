Mini Banking System

A simple web-based banking system developed as a semester project for the Database Systems course. This project demonstrates database design, SQL programming, and backend integration using Microsoft SQL Server (or MySQL, if not yet migrated) with a PHP and HTML/CSS frontend. It fulfills the requirements of creating a functional application with interrelated tables, user interactions, and proper documentation.

Project Overview
The Mini Banking System allows users to:
Register and log in securely.
Manage their profile (update personal information).
View checking and savings account balances.
Perform transactions (deposit, withdrawal, transfer).
Manage debit cards (view, block, order new).
Submit and view feedback with ratings.
Access a support page with contact details and FAQs.
The project includes a responsive frontend styled with CSS and a backend integrated with a relational database, meeting the course requirements for database design, normalization, and SQL queries (DDL, DML, TCL).

Features
User Authentication: Secure signup and login with password hashing.
Account Management: View checking and savings accounts with balances.
Transactions: Deposit, withdraw, and transfer money with transaction history.
Card Management: View card details, block cards, and order new cards.
Feedback System: Submit feedback with category and rating; view past feedback.
Search Functionality: Search transactions by date range (on dashboard).
Delete Functionality: Delete submitted feedback.
Responsive UI: Clean, user-friendly interface with sidebar navigation.

Technologies Used
Backend: Microsoft SQL Server (recommended) or MySQL (current implementation), PHP (PDO for database connectivity).
Frontend: HTML, CSS (custom style.css), JavaScript (minimal, for feedback rating).
Server: XAMPP (Apache for PHP, SQL Server/MySQL for database).
Tools: Draw.io (for ER diagram), Microsoft Word/Google Docs (for report).


Database Schema
The database consists of 5 interrelated tables:
users: Stores user details (user_id [PK], full_name, username, email, phone, address, password, created_at).
accounts: Stores account details (account_id [PK], user_id [FK], account_type, account_number, balance, created_at).
transactions: Records transactions (transaction_id [PK], account_id [FK], transaction_type, amount, description, target_account_id [FK], transaction_date)
cards: Manages cards (card_id [PK], user_id [FK], card_type, card_number, card_holder, expiry_date, credit_limit, available_credit, is_blocked).
feedback: Stores feedback (feedback_id [PK], user_id [FK], category, rating, comments, submitted_at).

ER Diagram: Available in er_diagram.drawio (to be created using Draw.io).

Normalization:
Tables are in 3NF, with proper primary/foreign keys, unique constraints, and checks.

Usage
Signup/Login:
On login.php, create an account or sign in:
Accounts are automatically created (checking and savings) upon signup.
Dashboard:
View total balance, recent transactions, and search transactions by date.
Profile:
Update personal details (name, email, phone, address).
Accounts:
View checking and savings account balances.
Transfers:
Transfer money between accounts using account numbers.
Deposit/Withdrawal:
Deposit or withdraw money from selected accounts.
Cards:
View card details, block cards, or order new ones.
Feedback:
Submit feedback with a category and rating; view or delete past feedback.

Acknowledgments
XAMPP and SQL Server for free tools.
Draw.io for ER diagram creation.

Contact
For issues or questions, contact the group via GitHub Issues or email.
