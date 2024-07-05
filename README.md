Q1ans
An exception in Python is an event that disrupts the normal flow of a program's execution when it encounters an error. Exceptions can occur due to various reasons such as incorrect user input, file not found, network issues, etc.
Differences between Exceptions and Syntax Errors:
1.	Exceptions:
o	Occur during the execution of the program.
o	Examples include ZeroDivisionError, FileNotFoundError, TypeError, etc.
o	Can be handled using try-except blocks to gracefully manage errors.
2.	Syntax Errors:
o	Occur during the parsing of code, before the execution of the program begins.
o	Examples include missing colons, invalid syntax in function calls, etc.
o	Must be corrected in the code before running the program.
In summary, exceptions are runtime errors that occur during program execution, while syntax errors are detected by the Python interpreter during the parsing phase of the code before any execution 
  Q2 ans
When an exception is not handled in Python, it causes the program to terminate abruptly, displaying an error traceback that indicates where the exception occurred and what type of exception it was. This disrupts the normal flow of the program and may lead to unexpected behavior or crashes.
Q3
Ans 
Python uses try, except, finally, and optionally else statements to manage and handle exceptions:
•	try: Attempts to execute code that may raise an exception.
•	except: Catches specific exceptions and defines how to handle them.
•	finally: Executes cleanup code regardless of whether an exception occurred.
Example:
python
Copy code
try:
    num = 10 / 0  # ZeroDivisionError occurs here
except ZeroDivisionError:
    print("Cannot divide by zero!")

Q4:ans
In Python, the try, except, else, and finally blocks are used together for exception handling:
•	try: Attempts to execute risky code.
•	else: Executes if no exceptions are raised in the try block.
•	finally: Executes cleanup code, whether an exception occurred or not.
Example:
python
Copy code
try:
    num = 10 / 2
except ZeroDivisionError:
    print("Cannot divide by zero!")
else:
    print("Division successful!")
finally:
    print("Execution completed.")
In this example:
•	Since 10 / 2 doesn't raise any exceptions, the else block executes, printing "Division successful!".
•	The finally block always executes, printing "Execution completed."
Q5:Ans 
Custom exceptions in Python are user-defined exception classes derived from the base Exception class. They allow developers to create specific error types tailored to their application's needs, improving code readability and maintainability by handling unique error scenarios effectively.
Example:
python
Copy code
class ValueTooHighError(Exception):
    pass

def check_value(value):
    if value > 100:
        raise ValueTooHighError("Value exceeds limit")

# Usage:
try:
    check_value(120)
except ValueTooHighError as e:
    print(e)
In this example, ValueTooHighError is a custom exception raised when a value exceeds a predefined limit.
Q6 Ans:
Here's an example of creating a custom exception class and using it to handle an exception:
python
Copy code
class CustomError(Exception):
    def __init__(self, message):
        self.message = message

def process_data(data):
    if not isinstance(data, int):
        raise CustomError("Invalid data type. Expected integer.")

# Usage:
try:
    process_data("invalid")
except CustomError as e:
    print(e.message)
In this example, CustomError is a custom exception class used to handle cases where the expected data type is not met.

