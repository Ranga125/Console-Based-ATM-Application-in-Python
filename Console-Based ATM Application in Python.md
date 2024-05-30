
Project Overview
This project is a console-based ATM application that simulates basic banking operations. Users can log in with a user ID and PIN, check their balance, withdraw and deposit funds, transfer money to other users, view their transaction history, change their PIN, and quit the session.

Features
    1.User Authentication:
        Login with user ID and PIN.
        Validate user credentials.
    2.Banking Operations:
        View transaction history.
        Withdraw funds.
        Deposit funds.
        Transfer funds to another user.
        Check balance.
        Change PIN.
    3.User Management:
        Add new users with an initial balance.
        Store and manage user data.
    4.Session Management:
        End session after user quits.
Project Structure
        User Class: Handles user details, balance, and transaction history.
        ATM Class: Manages users and authentication.
        Transaction Class: Records details of each transaction.
        BankOperations Class: Implements operations like withdraw, deposit, transfer, and change PIN.
        ATMSystem Class: Controls the user interface and main application flow.
Getting Started
     Prerequisites
     Python 3.12.3 installed on your machine.
Installation
     1.Clone the repository:
         git clone https://github.com/yourusername/atm-application.git
     2.Navigate to the project directory:
         cd atm-application
Usage
     Open a terminal and navigate to the project directory.
     Run the application:
         python atm_application.py
Follow the on-screen prompts to use the ATM application.
Example Users
    You can add users in the ATMSystem class initialization before starting the system. Here are some example users:
         atm_system = ATMSystem()
         atm_system.atm.add_user(User("user1", "1234", 1000))
         atm_system.atm.add_user(User("user2", "5678", 500))
Code Overview
      Here is a brief overview of the main classes and their functionality:

User Class
    1.Attributes:
         user_id: User ID.
         pin: User PIN.
         balance: User balance.
         transaction_history: List of user's transactions.
    2.Methods:
         add_transaction(transaction): Adds a transaction to the user's history.
         get_transaction_history(): Returns the user's transaction history.
         change_pin(old_pin, new_pin): Changes the user's PIN.
ATM Class
    1.Attributes:
         users: Dictionary of users.
    2.Methods:
         add_user(user): Adds a user to the ATM.
         authenticate_user(user_id, pin): Authenticates a user by ID and PIN.
Transaction Class
    Attributes:
         transaction_type: Type of transaction (Withdraw, Deposit, Transfer).
         amount: Amount of the transaction.
BankOperations Class
    Attributes:
         user: The user performing the operations.
    Methods:
         withdraw(amount): Withdraws an amount from the user's balance.
         deposit(amount): Deposits an amount to the user's balance.
         transfer(target_user, amount): Transfers an amount to another user.
         change_pin(old_pin, new_pin): Changes the user's PIN.
ATMSystem Class
    Attributes:
        atm: Instance of the ATM class.
    Methods:
        start(): Starts the ATM system.
        user_menu(user): Displays the user menu and handles user inputs.
Potential Enhancements
    Implement a database to store user information persistently.
    Add logging for security and auditing purposes.
    Create a graphical user interface (GUI) for better user experience.
License
    This project is licensed under the MIT License. See the LICENSE file for more details.

Acknowledgements
    This project was inspired by the need to understand object-oriented programming in Python and managing a simple banking system.
