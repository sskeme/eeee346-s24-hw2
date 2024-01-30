# Introduction

In this homework, you will implement Newton's method, also known as the Newton-Raphson method, to find roots of equations. Note that this homework only uses quadratic equations.

# Background: Newton's Method

The algorithm is an iterative process that produces better approximations of an equation's root.

The initial approximation of the root (x1) is calculated based on an initial guess (x0), evaulation of the equation f(x0) and its derivative f'(x0).

x1 = x0 - f(x0) / f'(x0)

This equation is repeated 1) MAX_ITERS times or 2) until the difference between xn+1 and xn is very small.

xn+1 = xn - f(xn) / f'(xn)

You can find more information about this method here: https://en.wikipedia.org/wiki/Newton%27s_method.

# Tasks

* Implement the quad() and quadPrime() functions in quadratic.cpp. These functions are already declared in quadratic.h, and you can find information about their parameters in this header file.
  
* Implement the newtonRaphsonQuad() function in netwon.cpp. This function is already declared in newton.h, and you can find information about its parameters in this header file.
  * In newtonRaphsonQuad(), call the quad() and quadPrime() functions to calculate approximate roots.
  * In newtonRaphsonQuad(), use THRESHOLD and MAX_ITERS, which are declared in newton.h, to terminate the algorithm. Do not change their values.

# Compile and Test

1. Type the following commands on Terminal.

```
g++ -o main *.cpp *.h
```
```
./main
```

2. Enter 4 numbers (a, b, c, and guess of main() in order) and check if your result is correct. Here is an example.
 * Input
 ```
 3 -11 1 0.1
 
 // Quadratic: 3x^2 - 11x + 1

 // Initial Root Guess: 0.1
 ```

 * Expected Output
 ```
 Root Found: 0.0932822, Iterations: 2
 ```

# Submit

1. Type the following commands on Terminal.

```
git add .
```
```
git commit -m "your_message_or_note_for_this_submission"
```
```
git push
```

2. You can verify that your program is working properly with predetermined inputs on GitHub Actions.
