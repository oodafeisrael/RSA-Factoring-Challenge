#!/usr/bin/python3 
import sys
import math

def is_prime(num):
    if num < 2:
        return False
    for i in range(2, int(math.sqrt(num)) + 1):
        if num % i == 0:
            return False
    return True

def factorize_number(n):
    for i in range(2, n):
        if n % i == 0 and is_prime(i):
            return i, n // i
    return None, None

def main(filename):
    with open(filename, 'r') as file:
        for line in file:
            n = int(line.strip())
            p, q = factorize_number(n)
            if p is not None and q is not None:
                print(f"{n}={p}*{q}")
            else:
                print(f"{n} is not factorizable into two smaller numbers")

if __name__ == "__main__":
    if len(sys.argv) != 2:
        print("Usage: python factors.py <filename>")
        sys.exit(1)
    filename = sys.argv[1]
    main(filename)
