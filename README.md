<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
</head>
<body>
    <h1>Console-Based ATM Application in Python</h1>
	  <h2>Project Overview</h2>
    <p>This project is a console-based ATM application that simulates basic banking operations. Users can log in with a user ID and PIN, check their balance, withdraw and deposit funds, transfer money to other users, view their transaction history, change their PIN, and quit the session.</p>
<h2>Features</h2>
    <ul>
        <li><strong>User Authentication:</strong>
            <ul>
                <li>Login with user ID and PIN.</li>
                <li>Validate user credentials.</li>
            </ul>
        </li>
        <li><strong>Banking Operations:</strong>
            <ul>
                <li>View transaction history.</li>
                <li>Withdraw funds.</li>
                <li>Deposit funds.</li>
                <li>Transfer funds to another user.</li>
                <li>Check balance.</li>
                <li>Change PIN.</li>
            </ul>
        </li>
        <li><strong>User Management:</strong>
            <ul>
                <li>Add new users with an initial balance.</li>
                <li>Store and manage user data.</li>
            </ul>
        </li>
        <li><strong>Session Management:</strong>
            <ul>
                <li>End session after user quits.</li>
            </ul>
        </li>
    </ul>
<h2>Project Structure</h2>
    <ul>
        <li><strong>User Class:</strong> Handles user details, balance, and transaction history.</li>
        <li><strong>ATM Class:</strong> Manages users and authentication.</li>
        <li><strong>Transaction Class:</strong> Records details of each transaction.</li>
        <li><strong>BankOperations Class:</strong> Implements operations like withdraw, deposit, transfer, and change PIN.</li>
        <li><strong>ATMSystem Class:</strong> Controls the user interface and main application flow.</li>
    </ul>
<h2>Getting Started</h2>
    <h3>Prerequisites</h3>
    <p>Python 3.10.12 installed on your machine.</p>
<h3>Installation</h3>
    <pre><code>git clone https://github.com/Ranga125/Console-Based-ATM-Application-in-Python
cd atm-application</code></pre>
<h3>Usage</h3>
    <pre><code>python atm_application.py</code></pre>
    <p>Follow the on-screen prompts to use the ATM application.</p>
<h2>Example Users</h2>
    <p>You can add users in the <code>ATMSystem</code> class initialization before starting the system. Here are some example users:</p>
    <pre><code>atm_system = ATMSystem()
atm_system.atm.add_user(User("user1", "1234", 1000))
atm_system.atm.add_user(User("user2", "5678", 500))</code></pre>
<h2>Code Overview</h2>
    <p>Here is a brief overview of the main classes and their functionality:</p>
<h3>User Class</h3>
    <ul>
        <li><strong>Attributes:</strong>
            <ul>
                <li><code>user_id</code>: User ID.</li>
                <li><code>pin</code>: User PIN.</li>
                <li><code>balance</code>: User balance.</li>
                <li><code>transaction_history</code>: List of user's transactions.</li>
            </ul>
        </li>
        <li><strong>Methods:</strong>
            <ul>
                <li><code>add_transaction(transaction)</code>: Adds a transaction to the user's history.</li>
                <li><code>get_transaction_history()</code>: Returns the user's transaction history.</li>
                <li><code>change_pin(old_pin, new_pin)</code>: Changes the user's PIN.</li>
            </ul>
        </li>
    </ul>
<h3>ATM Class</h3>
    <ul>
        <li><strong>Attributes:</strong>
            <ul>
                <li><code>users</code>: Dictionary of users.</li>
            </ul>
        </li>
        <li><strong>Methods:</strong>
            <ul>
                <li><code>add_user(user)</code>: Adds a user to the ATM.</li>
                <li><code>authenticate_user(user_id, pin)</code>: Authenticates a user by ID and PIN.</li>
            </ul>
        </li>
    </ul>
<h3>Transaction Class</h3>
    <ul>
        <li><strong>Attributes:</strong>
            <ul>
                <li><code>transaction_type</code>: Type of transaction (Withdraw, Deposit, Transfer).</li>
                <li><code>amount</code>: Amount of the transaction.</li>
            </ul>
        </li>
    </ul>
<h3>BankOperations Class</h3>
    <ul>
        <li><strong>Attributes:</strong>
            <ul>
                <li><code>user</code>: The user performing the operations.</li>
            </ul>
        </li>
        <li><strong>Methods:</strong>
            <ul>
                <li><code>withdraw(amount)</code>: Withdraws an amount from the user's balance.</li>
                <li><code>deposit(amount)</code>: Deposits an amount to the user's balance.</li>
                <li><code>transfer(target_user, amount)</code>: Transfers an amount to another user.</li>
                <li><code>change_pin(old_pin, new_pin)</code>: Changes the user's PIN.</li>
            </ul>
        </li>
    </ul>
<h3>ATMSystem Class</h3>
    <ul>
        <li><strong>Attributes:</strong>
            <ul>
                <li><code>atm</code>: Instance of the ATM class.</li>
            </ul>
        </li>
        <li><strong>Methods:</strong>
            <ul>
                <li><code>start()</code>: Starts the ATM system.</li>
                <li><code>user_menu(user)</code>: Displays the user menu and handles user inputs.</li>
            </ul>
        </li>
    </ul>
<h2>Potential Enhancements</h2>
    <ul>
        <li>Implement a database to store user information persistently.</li>
        <li>Add logging for security and auditing purposes.</li>
        <li>Create a graphical user interface (GUI) for better user experience.</li>
    </ul>
<h2>License</h2>
    <p>This project is licensed under the MIT License. See the LICENSE file for more details.</p>
<h2>Acknowledgements</h2>
    <p>This project was inspired by the need to understand object-oriented programming in Python and managing a simple banking system.</p>
</body>
</html>
