# Bank_Management
The Bank Management System is designed to handle core banking operations such as account creation, transactions (credit/debit), and passbook generation efficiently. The system ensures that customer details are stored securely while allowing seamless banking transactions. It also implements triggers and stored procedures to automate key operations.

How it Works:
Customers open an account, and their details are stored in the ACCOUNT_OPENING table.

When KYC is approved, a trigger automatically creates an account in the BANK and adds customer details to ACCOUNT_HOLDER.

Customers can deposit/withdraw money using stored procedures (sp_credit_into, sp_debit_into), which update the TRANSACTION_DETAILS and BANK tables.

The passbook procedure (sp_give_passbook) retrieves transaction history for a given period.

This system ensures automation, security (rollback for insufficient funds), and efficiency in managing banking operations.
