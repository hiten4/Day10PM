# Day10PM

````markdown
# Student Performance Analytics Assignment

## Overview
This assignment focuses on building a small analytics system for student performance using Python. It demonstrates the use of functions, decorators, memoization, variable scope, and flexible function arguments such as `*args` and `**kwargs`.

---

## Part A — Student Performance Analytics Module

A module **student_analytics.py** was created to process student data and generate performance insights.

### Data Structure

```python
students = [
    {
        "name": str,
        "roll": str,
        "marks": {"math": int, "python": int, "ml": int},
        "attendance": float
    }
]
````

### Functions Implemented

* **create_student()**
  Creates a student record using `**kwargs` for flexible subject marks.

* **calculate_gpa()**
  Calculates GPA from any number of marks using `*args`.

* **get_top_performers()**
  Returns top students based on subject score or overall average.

* **generate_report()**
  Generates a formatted report for a student with optional parameters.

* **classify_students()**
  Classifies students into grade groups using `defaultdict`.

All functions include **type hints**, **docstrings**, and **edge case handling**.

A separate file **test_analytics.py** contains `assert` tests to validate each function.

---

## Part B — Python Decorators

Three decorators were implemented.

### @timer

Measures and prints the execution time of a function.

### @logger

Logs function name, arguments, and return value.

### @retry

Retries a function multiple times if it raises an exception.

Concepts used:

* Closures
* `functools.wraps`
* `*args` and `**kwargs`

---

## Part C — Interview Preparation

### LEGB Rule

Python variable lookup follows this order:

```
Local → Enclosing → Global → Built-in
```

This rule determines how Python resolves variable names in nested scopes.

### Memoization

A `memoize` decorator was implemented to cache expensive function calls.

Example:

```python
@memoize
def fibonacci(n):
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)
```

Memoization drastically improves performance by storing previously computed results.

---

## Part D — AI-Augmented Task

An AI tool was prompted to generate a text analysis function.

The function performs:

* Word counting
* Sentence counting
* Longest word detection
* Simple sentiment analysis

The AI-generated code was evaluated for:

* Proper use of `**kwargs`
* Type hint correctness
* Edge case handling
* Code structure

An improved version was implemented by splitting the logic into smaller helper functions, making the design more modular and maintainable.

---

## Key Concepts Used

* Python functions
* `*args` and `**kwargs`
* Decorators
* Memoization
* Variable scope (LEGB rule)
* defaultdict
* Basic text analysis
* Code testing with assertions

```
```
