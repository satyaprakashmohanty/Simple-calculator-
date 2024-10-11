# Simple-calculator-
import math

def add(a, b):
    return a + b

def subtract(a, b):
    return a - b

def multiply(a, b):
    return a * b

def divide(a, b):
    if b == 0:
        return "Error! Division by zero."
    else:
        return a / b

def square(a):
    return a ** 2

def sqrt(a):
    if a < 0:
        return "Error! Cannot compute square root of a negative number."
    else:
        return math.sqrt(a)

def logarithm(a):
    if a <= 0:
        return "Error! Logarithm not defined for zero or negative numbers."
    else:
        return math.log(a)

def calculator():
    print("Simple Calculator")
    print("Select operation:")
    print("1. Add")
    print("2. Subtract")
    print("3. Multiply")
    print("4. Divide")
    print("5. Square")
    print("6. Square Root")
    print("7. Logarithm")

    choice = input("Enter choice(1-7): ")

    if choice in ['1', '2', '3', '4']:
        num1 = float(input("Enter first number: "))
        num2 = float(input("Enter second number: "))

    if choice == '1':
        print(f"Result: {add(num1, num2)}")
    elif choice == '2':
        print(f"Result: {subtract(num1, num2)}")
    elif choice == '3':
        print(f"Result: {multiply(num1, num2)}")
    elif choice == '4':
        print(f"Result: {divide(num1, num2)}")

    elif choice == '5':
        num = float(input("Enter a number: "))
        print(f"Result: {square(num)}")

    elif choice == '6':
        num = float(input("Enter a number: "))
        print(f"Result: {sqrt(num)}")

    elif choice == '7':
        num = float(input("Enter a number: "))
        print(f"Result: {logarithm(num)}")

    else:
        print("Invalid input")

if __name__ == "__main__":
    calculator()
    
