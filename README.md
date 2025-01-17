# Simple Digital Wallet

![Simple Digital Wallet](bg.jpg)

## Table of Contents

- [Introduction](#introduction)
- [Features](#features)
- [Data Structures Used](#data-structures-used)
- [Project's Schema](#projects-schema)
- [File Handling](#file-handling)
- [Usage](#usage)
- [Installation](#installation)
- [Contributing](#contributing)

## Introduction

Welcome to the Simple Digital Wallet! This project provides a comprehensive digital wallet solution for managing transactions, user accounts, authentication, and more. It was initially developed as a C++ console application and later evolved into a more sophisticated version with a graphical user interface using Qt.

## Features

- User authentication and management (including admins and regular users)
- Secure password handling with masking and hashing
- Transaction management (sending money, requesting money, viewing transaction history)
- Notification system for handling money requests
- Deposit and withdrawal functionalities
- Profile management (editing user details)
- Error handling for various scenarios

## Data Structures Used

1. **unordered_map<string, User> mapOfUsers**: Stores user information, where the key is the user's address and the value is an instance of the User class.
2. **vector<Transaction> transactions**: Stores transaction history, including sender address, receiver address, transaction amount, and type.
3. **vector<Transaction> RequestHistory**: Stores transaction history specifically for money requests.
4. **queue<char> passwordQueue**: Used for collecting characters for password input with masking.

## Project's Schema

![schema](schema.png)

In this schema, users are stored in the **Users** table with attributes like address, name, balance, etc. The **Transactions** table logs all transactions, including sender and receiver addresses, amounts, and types. Similarly, the **RequestHistory** table tracks money requests between users, with sender and receiver addresses, amounts, and timestamps. Both transactions and requests are associated with users via their addresses.

## File Handling

The `Files` class is responsible for reading data from and writing data to files. It reads user information, transaction history, and request history from files and populates the respective data structures. Saving data to files is assumed to be implemented similarly.

## Usage

To use the Simple Digital Wallet, follow these steps:

1. Clone the repository.
2. Compile and run the project using your preferred IDE or command line.
3. Interact with the system using the provided interfaces for signing up, logging in, performing transactions, managing profile, etc.

## Installation

1. Clone the repository:
    ```bash
    git clone https://github.com/Abraam318/simple-digital-wallet.git
    ```
2. Navigate to the project directory:
    ```bash
    cd simple-digital-wallet
    ```
3. Compile and run the project.

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.
