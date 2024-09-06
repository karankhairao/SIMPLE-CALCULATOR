# Basic Calculator

## Created by Karan Khairao

Welcome to the Basic Calculator project! This Python program is designed to perform basic arithmetic operations. It prompts the user to input two numbers and select an operation (addition, subtraction, multiplication, or division). The program then performs the selected operation and displays the result.

## Features

- **Addition**: Calculates the sum of two numbers.
- **Subtraction**: Computes the difference between two numbers.
- **Multiplication**: Multiplies two numbers.
- **Division**: Divides the first number by the second, with error handling for division by zero.

## Installation

To use this program, you need to have Python installed on your machine. The program is compatible with Python 3.

1. **Clone the Repository**

   ```bash
   git clone https://github.com/karankhairao/SIMPLE-CALCULATOR.git
Navigate to the Directory

bash
Copy code
cd basic-calculator
Run the Script

bash
Copy code
python calculator.py
Usage
Run the script: Execute the program using Python.
Enter two numbers: Input the two numbers you want to calculate with.
Choose an operation: Select an operation by entering the corresponding number:
1 for Addition
2 for Subtraction
3 for Multiplication
4 for Division
View the result: The program will display the result of the selected operation.
Example
markdown
Copy code
Welcome to the Basic Calculator!

Enter the first number: 15
Enter the second number: 3

Choose an operation:
1. Addition
2. Subtraction
3. Multiplication
4. Division

Enter the number corresponding to your choice (1/2/3/4): 4

The result of division is: 5.0
Code
Below is the Python code for the Basic Calculator:

python
Copy code
# calculator.py

def add(x, y):
    return x + y

def subtract(x, y):
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y == 0:
        return "Error! Division by zero."
    return x / y

def main():
    print("Welcome to the Basic Calculator!")

    try:
        num1 = float(input("Enter the first number: "))
        num2 = float(input("Enter the second number: "))
    except ValueError:
        print("Invalid input! Please enter numeric values.")
        return

    print("\nChoose an operation:")
    print("1. Addition")
    print("2. Subtraction")
    print("3. Multiplication")
    print("4. Division")

    choice = input("Enter the number corresponding to your choice (1/2/3/4): ")

    if choice == '1':
        result = add(num1, num2)
        print(f"The result of addition is: {result}")
    elif choice == '2':
        result = subtract(num1, num2)
        print(f"The result of subtraction is: {result}")
    elif choice == '3':
        result = multiply(num1, num2)
        print(f"The result of multiplication is: {result}")
    elif choice == '4':
        result = divide(num1, num2)
        print(f"The result of division is: {result}")
    else:
        print("Invalid choice! Please enter a number between 1 and 4.")

if __name__ == "__main__":
    main()
