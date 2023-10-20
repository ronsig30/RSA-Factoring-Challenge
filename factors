#!/usr/bin/python3
import sys
import sympy

def factorize_numbers(filename):
    try:
        with open(filename, 'r') as file:
            for line in file:
                number = int(line.strip())
                factors = factorize_number(number)
                print(f"{number}={factors[0]}*{factors[1]}")

    except FileNotFoundError:
        print(f"Error: File '{filename}' not found.")
    except ValueError:
        print("Error: Invalid input in the file.")

def factorize_number(number):
    p, q = sympy.factorint(number)
    return p, q

if __name__ == "__main__":
    if len(sys.argv) != 2:
        print("Usage: ./factors <file>")
    else:
        filename = sys.argv[1]
        factorize_numbers(filename)

