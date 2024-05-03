[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/e-RY2uhP)
## Python Classes and Files

### Banking
Your task is to manage a bank account and transactions. You should save the transactions in files and read them from files. You should also be able to print the transactions in a nice way.
You should have 2 'data' files. One to save accounts and one for tranactions.

1. Create a class `BankAccount` with the following:
    - fields:
        - `id: int` - a unique identifier for the account (automatically generated and incremented for each new account)
        - `name: str` - the name of the account owner
        - `balance: float` - the current balance of the account
    - `__init__(self, name: str, balance: float = 0.0)` - constructor that takes the name of the account owner and the initial balance. The initial balance should be 0.0 if not provided.
    - `deposit(self, amount: float)` - method that takes an amount and adds it to the balance.
    - `withdraw(self, amount: float)` - method that takes an amount and subtracts it from the balance.
    - `get_balance(self) -> float` - method that returns the current balance.
    - `transfer(self, amount: float, other_account: BankAccount)` - method that takes an amount and another account. It should transfer the amount from this account to the other account. (you should use the `withdraw` and `deposit` methods to do this and you should use the `Transaction` class to save the transaction in a file.)
    - `__str__(self) -> str` - method that returns a string representation of the account. The string should contain the name of the account owner and the current balance.

2. Create a class `Transaction` with the following methods:
    - `__init__(self, amount: float, date: str)` - constructor that takes the amount of the transaction and the date of the transaction. 
    - `save(self, file_name: str)` - method that saves the transaction in a file. The file should contain the amount and the date of the transaction.
    - `__str__(self) -> str` - method that returns a string representation of the transaction. The string should contain the amount and the date of the transaction.



### How program should work
Your programs should be in an infinite loop that takes commands from the user. The user should be able to do the following:
1. user should be able to create new account or select already created account by providing the id of the account.
2. user should be able to deposit money to the account by providing the amount.
3. user should be able to withdraw money from the account by providing the amount.
4. user should be able to get the current balance of the account.
5. user should be able to transfer money from the account to another account by providing the amount and the id of the other account.
6. user should be able to print the transactions of the account.
7. user should be able to exit the program.


### Testing (create new python file for testing)
You should write tests for the `BankAccount` class. You should
- test the constructor
- test the `deposit` method
- test the `withdraw` method
- test the `get_balance` method
- test the `transfer` method
- test the `__str__` method


### Hints
- Use the `datetime` module to get the current date and time.
- Use `Path` from `pathlib` to work with files.
- Your project structure should look like this:
```bash
.
├── banking/
│   ├── __init__.py
│   ├── account.py          # (Account class should be here)
│   └── transaction.py      # (Transaction classes should be here)
├── tests/
│   ├── __init__.py
│   └── test_account.py     # (your tests should be here)
|__ data/
|   ├── accounts.txt
|   └── transactions.txt
└── main.py                 # (your main program should be here)
```



