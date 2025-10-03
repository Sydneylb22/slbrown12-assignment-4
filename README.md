# slbrown12-assignment-5
#Collatz Conjecture
print("=== Challenge 1: Collatz Conjecture ===")
current_number = int(input("Enter starting number: "))
step_count = 0

print("Sequence:", end=" ")
while current_number != 1:
    print(current_number, end=" ")
    if current_number % 2 == 0:
        current_number = current_number // 2
    else:
        current_number = current_number * 3 + 1
    step_count += 1
print(current_number)
print("Steps:", step_count)
git add collatz_sequence.py
git commit -m "Challenge 1: Collatz sequence - while loop for unknown iterations"

print("=== Challenge 2: Prime Number Checker ===")
#Prime Number Checker
n = int(input("Enter a number: "))
print(f"Testing divisors from 2 to {n - 1}...")

is_prime = True
for i in range(2, n):
    if n % i == 0:
        print(f"{n} is not prime (divisible by {i})")
        is_prime = False
        break

if is_prime:
    print(f"{n} is prime!")
 git add prime_checker.py
git commit -m "Challenge 2: Prime checker - for loop for known range"

#Multiplication Table
print("=== Challenge 3: Multiplication Table ===")
print("Multiplication Table")
print("    ", end="")
for col in range(1, 11):
    print(f"{col:4}", end="")
print()

for row in range(1, 11):
    print(f"{row:2} ", end="")
    for col in range(1, 11):
        product = row * col
        print(f"{product:4}", end="")
    print()
git add multiplication_table.py
git commit -m "Challenge 3: Multiplication grid - nested loops for 2D data"

git add README.md
git commit -m "Add loop design documentation"
