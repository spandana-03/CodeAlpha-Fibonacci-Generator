# CodeAlpha-Fibonacci-Generator
def fibonacci_recursive(n):
    if n <= 1:
        return n
    else:
        return fibonacci_recursive(n - 1) + fibonacci_recursive(n - 2)
# Example: Print the first 10 Fibonacci numbers
n = 10
for i in range(n):
    print(fibonacci_recursive(i), end=" ")
0 1 1 2 3 5 8 13 21 34 
def fibonacci_generator():
    a, b = 0, 1
    while True:
        yield a
        a, b = b, a + b
# Example: Generate the first 10 Fibonacci numbers
fib_gen = fibonacci_generator()
for _ in range(10):
    print(next(fib_gen), end=" ")
0 1 1 2 3 5 8 13 21 34
