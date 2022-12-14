# Comptester
A simple python package to test the computation speed of different expressions.
 - E.g., does `x*x*x*x*x*x` or `x**6` run faster?

## Installation
To install this package, run `python3 -m pip install tqdm matplotlib && python3 -m pip install -i https://test.pypi.org/simple/ comptester==0.1.0` in the commandline.

## Usage
See the **Example** section below for an in-depth example for how to use this package.
 - The `test` method will perform a test given two expressions, an iteration count, and a sample count.
 - The `tprint` method will print the data from the test.
 - The `plot` method will plot the data so you can see visually how the expressions compare against each other and a control.

## Example
```py
from comptester import tester

# Defining parameters
test1 = 'x*x*x*x*x*x'  # Compute x^6 by multiplication
test2 = 'x**6'  # Compute x^6 by power
iterations = 100000  # Number of times each expression is tested in a sample
samples = 100  # Number of samples to collect

# Run the test and store it in the 'test' variable
test = tester.test(test1, test2, iterations, samples)

# Print the test results to the console
# tester.tprint(test)

# Plot the test results
tester.plot(test)
```

## Example plot
The example code above produces the following plot:

<img src="https://github.com/piano-miles/comptester/blob/main/example/plot.png" width="512">
