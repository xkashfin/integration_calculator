import numpy as np

# Define the function to be integrated
def f(x):
    return np.sin(x)

# Define the integration limits
a = 0
b = np.pi

# Define the number of intervals (must be even for Simpson's rules)
n = 10

# Trapezoid Rule
h = (b-a)/n
x = np.linspace(a, b, n+1)
y = f(x)
T = h*(np.sum(y) - 0.5*(y[0] + y[-1]))

# Simpson's 1/3 Rule
if n % 2 != 0:
    print("Simpson's 1/3 rule requires an even number of intervals.")
else:
    h = (b-a)/n
    x = np.linspace(a, b, n+1)
    y = f(x)
    S1 = h/3 * (y[0] + 4*np.sum(y[1:-1:2]) + 2*np.sum(y[2:-1:2]) + y[-1])

# Simpson's 3/8 Rule
if n % 3 != 0:
    print("Simpson's 3/8 rule requires a multiple of 3 intervals.")
else:
    h = (b-a)/n
    x = np.linspace(a, b, n+1)
    y = f(x)
    S2 = 3*h/8 * (y[0] + 3*y[1] + 3*y[2] + 2*np.sum(y[3:-1:3]) + 3*np.sum(y[4:-1:3]) + y[-1])

# Print the results
print(f"The integral of sin(x) from {a} to {b}:")
print(f"Trapezoid Rule: {T}")
if n % 2 == 0:
    print(f"Simpson's 1/3 Rule: {S1}")
if n % 3 == 0:
    print(f"Simpson's 3/8 Rule: {S2}")
