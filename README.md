# Table of Content <!-- omit in toc -->

- [1. Using the Python Interpreter](#1-using-the-python-interpreter)
  - [1.1. Start Python](#11-start-python)
  - [1.2. Two ways to run Python](#12-two-ways-to-run-python)
    - [1.2.1. Interactive mode (REPL)](#121-interactive-mode-repl)
    - [1.2.2. Run a Python file](#122-run-a-python-file)
  - [1.3. Useful command-line options](#13-useful-command-line-options)
    - [1.3.1. Run a short command with `-c`](#131-run-a-short-command-with--c)
    - [1.3.2. Run a module with `-m`](#132-run-a-module-with--m)
    - [1.3.3. Run a script and then enter interactive mode with `-i`](#133-run-a-script-and-then-enter-interactive-mode-with--i)
  - [1.4. Command-line arguments](#14-command-line-arguments)
  - [1.5. Exit the interpreter](#15-exit-the-interpreter)
  - [1.6. Source-code encoding](#16-source-code-encoding)
  - [1.7. Key takeaways](#17-key-takeaways)
- [2. An Informal Introduction to Python](#2-an-informal-introduction-to-python)
  - [2.1. Comments and Basics](#21-comments-and-basics)
  - [2.2. Using Python as a Calculator](#22-using-python-as-a-calculator)
    - [2.2.1. Numbers](#221-numbers)
    - [2.2.2. Text (Strings)](#222-text-strings)
    - [2.2.3. Lists](#223-lists)
  - [2.3. First Steps Towards Programming](#23-first-steps-towards-programming)
    - [2.3.1. Core Concepts Introduced:](#231-core-concepts-introduced)
- [3. More Control Flow Tools](#3-more-control-flow-tools)
  - [3.1. `if` Statements](#31-if-statements)
  - [3.2. `for` Statements](#32-for-statements)
  - [3.3. The `range()` Function](#33-the-range-function)
  - [3.4. `break`, `continue`, and `else` Clauses on Loops](#34-break-continue-and-else-clauses-on-loops)
  - [3.5. The `pass` Statement](#35-the-pass-statement)
  - [3.6. `match` Statements](#36-match-statements)
    - [3.6.1. Pattern Matching with Shapes / Classes](#361-pattern-matching-with-shapes--classes)
  - [3.7. Defining Functions](#37-defining-functions)
  - [3.8. More on Function Arguments](#38-more-on-function-arguments)
    - [3.8.1. Default Argument Values](#381-default-argument-values)
    - [3.8.2. Keyword Arguments](#382-keyword-arguments)
    - [3.8.3. Special Parameters (`/` and `*`)](#383-special-parameters--and-)
    - [3.8.4. Arbitrary Argument Lists (`*args` and `**kwargs`)](#384-arbitrary-argument-lists-args-and-kwargs)
    - [3.8.5. Unpacking Argument Lists](#385-unpacking-argument-lists)
    - [3.8.6. Lambda Expressions](#386-lambda-expressions)
    - [3.8.7. Documentation Strings (Docstrings)](#387-documentation-strings-docstrings)
    - [3.8.8. Function Annotations](#388-function-annotations)
  - [3.9. Intermezzo: Coding Style (PEP 8)](#39-intermezzo-coding-style-pep-8)
- [4. Data Structures](#4-data-structures)
  - [4.1. More on Lists](#41-more-on-lists)
    - [4.1.1. Common List Methods](#411-common-list-methods)
    - [4.1.2. Using Lists as Stacks (LIFO)](#412-using-lists-as-stacks-lifo)
    - [4.1.3. Using Lists as Queues (FIFO)](#413-using-lists-as-queues-fifo)
    - [4.1.4. List Comprehensions](#414-list-comprehensions)
    - [4.1.5. Nested List Comprehensions](#415-nested-list-comprehensions)
  - [4.2. The `del` Statement](#42-the-del-statement)
  - [4.3. Tuples and Sequences](#43-tuples-and-sequences)
  - [4.4. Sets](#44-sets)
  - [4.5. Dictionaries](#45-dictionaries)
  - [4.6. Looping Techniques](#46-looping-techniques)
  - [4.7. Conditions \& Comparing Sequences](#47-conditions--comparing-sequences)
- [5. Modules](#5-modules)
  - [5.1. More on Modules](#51-more-on-modules)
    - [5.1.1. Importing Specific Names or All Names](#511-importing-specific-names-or-all-names)
  - [5.2. Executing Modules as Scripts](#52-executing-modules-as-scripts)
  - [5.3. The Module Search Path](#53-the-module-search-path)
    - [5.3.1. "Compiled" Python Files](#531-compiled-python-files)
  - [5.4. Standard Modules](#54-standard-modules)
  - [5.5. The `dir()` Function](#55-the-dir-function)
  - [5.6. Packages](#56-packages)
    - [5.6.1. Directory Structure Example:](#561-directory-structure-example)
    - [5.6.2. Importing Packages](#562-importing-packages)
    - [5.6.3. Note on `import *`](#563-note-on-import-)
- [6. Input and Output](#6-input-and-output)
  - [6.1. Fancier Output Formatting](#61-fancier-output-formatting)
    - [6.1.1. Formatted String Literals (f-strings)](#611-formatted-string-literals-f-strings)
    - [6.1.2. The String `format()` Method](#612-the-string-format-method)
    - [6.1.3. Manual String Formatting](#613-manual-string-formatting)
  - [6.2. Reading and Writing Files](#62-reading-and-writing-files)
    - [6.2.1. Opening Files](#621-opening-files)
    - [6.2.2. Using `with` Statements](#622-using-with-statements)
    - [6.2.3. Methods of File Objects](#623-methods-of-file-objects)
  - [6.3. Saving Structured Data with `json`](#63-saving-structured-data-with-json)
- [7. Errors and Exceptions](#7-errors-and-exceptions)
  - [7.1. Syntax Errors vs. Exceptions](#71-syntax-errors-vs-exceptions)
    - [7.1.1. Syntax Errors (Parsing Errors)](#711-syntax-errors-parsing-errors)
    - [7.1.2. Exceptions](#712-exceptions)
  - [7.2. Handling Exceptions](#72-handling-exceptions)
    - [7.2.1. Handling Multiple Exceptions](#721-handling-multiple-exceptions)
    - [7.2.2. Accessing the Exception Instance](#722-accessing-the-exception-instance)
    - [7.2.3. The `else` Clause](#723-the-else-clause)
  - [7.3. Raising Exceptions](#73-raising-exceptions)
  - [7.4. Exception Chaining](#74-exception-chaining)
  - [7.5. User-defined Exceptions](#75-user-defined-exceptions)
  - [7.6. Clean-up Actions (`finally`)](#76-clean-up-actions-finally)
  - [7.7. Predefined Clean-up Actions](#77-predefined-clean-up-actions)
  - [7.8. Raising and Handling Multiple Unrelated Exceptions (`ExceptionGroup`)](#78-raising-and-handling-multiple-unrelated-exceptions-exceptiongroup)
  - [7.9. Enriching Exceptions with Notes](#79-enriching-exceptions-with-notes)
- [8. Classes](#8-classes)
  - [8.1. A Word About Namespaces and Scopes](#81-a-word-about-namespaces-and-scopes)
    - [8.1.1. Global and Nonlocal Keywords](#811-global-and-nonlocal-keywords)
  - [8.2. A First Look at Classes](#82-a-first-look-at-classes)
    - [8.2.1. Class Definition Syntax](#821-class-definition-syntax)
    - [8.2.2. Class Objects \& Instantiation](#822-class-objects--instantiation)
    - [8.2.3. The `__init__()` Method](#823-the-__init__-method)
  - [8.3. Class and Instance Variables](#83-class-and-instance-variables)
  - [8.4. Inheritance](#84-inheritance)
    - [8.4.1. Overriding Methods \& Built-in Functions](#841-overriding-methods--built-in-functions)
    - [8.4.2. Multiple Inheritance](#842-multiple-inheritance)
  - [8.5. Private Variables (`__name`)](#85-private-variables-__name)
  - [8.6. Iterators](#86-iterators)
  - [8.7. Generators](#87-generators)
  - [8.8. Generator Expressions](#88-generator-expressions)
- [9. Brief Tour of the Standard Library (Part - I)](#9-brief-tour-of-the-standard-library-part---i)
  - [9.1. Operating System Interface](#91-operating-system-interface)
  - [9.2. File Wildcards](#92-file-wildcards)
  - [9.3. Command Line Arguments](#93-command-line-arguments)
  - [9.4. Error Output Redirection and Program Termination](#94-error-output-redirection-and-program-termination)
  - [9.5. String Pattern Matching](#95-string-pattern-matching)
  - [9.6. Mathematics](#96-mathematics)
  - [9.7. Internet Access](#97-internet-access)
  - [9.8. Dates and Times](#98-dates-and-times)
  - [9.9. Data Compression](#99-data-compression)
  - [9.10. Performance Measurement](#910-performance-measurement)
  - [9.11. Quality Control](#911-quality-control)
    - [9.11.1. `doctest`](#9111-doctest)
    - [9.11.2. `unittest`](#9112-unittest)
  - [9.12. Batteries Included](#912-batteries-included)
- [10. Brief Tour of the Standard Library — Part II](#10-brief-tour-of-the-standard-library--part-ii)
  - [10.1. Output Formatting](#101-output-formatting)
    - [10.1.1. `reprlib`](#1011-reprlib)
    - [10.1.2. `pprint`](#1012-pprint)
    - [10.1.3. `textwrap`](#1013-textwrap)
    - [10.1.4. `locale`](#1014-locale)
  - [10.2. Templating](#102-templating)
  - [10.3. Working with Binary Data Record Layouts](#103-working-with-binary-data-record-layouts)
  - [10.4. Multi-threading](#104-multi-threading)
  - [10.5. Logging](#105-logging)
  - [10.6. Weak References](#106-weak-references)
  - [10.7. Tools for Working with Lists](#107-tools-for-working-with-lists)
    - [10.7.1. `array`](#1071-array)
    - [10.7.2. `deque`](#1072-deque)
    - [10.7.3. `bisect`](#1073-bisect)
    - [10.7.4. `heapq`](#1074-heapq)
  - [10.8. Decimal Floating Point Arithmetic](#108-decimal-floating-point-arithmetic)
- [11. Virtual Environments and Packages](#11-virtual-environments-and-packages)
  - [11.1. Introduction \& Motivation](#111-introduction--motivation)
  - [11.2. Creating Virtual Environments](#112-creating-virtual-environments)
  - [11.3. Activating Virtual Environments](#113-activating-virtual-environments)
  - [11.4. Managing Packages with `pip`](#114-managing-packages-with-pip)
    - [11.4.1. Installing Packages](#1141-installing-packages)
    - [11.4.2. Displaying Installed Packages](#1142-displaying-installed-packages)
    - [11.4.3. Reproducing Environments with Requirements Files](#1143-reproducing-environments-with-requirements-files)
- [12. Floating-Point Arithmetic: Issues and Limitations](#12-floating-point-arithmetic-issues-and-limitations)
  - [12.1. Representation Error](#121-representation-error)
  - [12.2. Practical Consequences of Imprecision](#122-practical-consequences-of-imprecision)
    - [12.2.1. Unexpected Arithmetic Results](#1221-unexpected-arithmetic-results)
    - [12.2.2. Rounding and Comparison Issues](#1222-rounding-and-comparison-issues)
  - [12.3. Best Practices \& Mitigations](#123-best-practices--mitigations)
    - [12.3.1. Avoid Equality Comparison on Floats](#1231-avoid-equality-comparison-on-floats)
    - [12.3.2. Exact Decimal Arithmetic (`decimal`)](#1232-exact-decimal-arithmetic-decimal)
    - [12.3.3. Exact Rational Arithmetic (`fractions`)](#1233-exact-rational-arithmetic-fractions)
    - [12.3.4. Floating-Point Summation (`math.fsum`)](#1234-floating-point-summation-mathfsum)
  - [12.4. Helper Methods (`float.hex` \& `float.fromhex`)](#124-helper-methods-floathex--floatfromhex)

# 1. Using the Python Interpreter

Source: [The official Python Tutorial: Using the Python Interpreter](https://docs.python.org/3/tutorial/interpreter.html)

## 1.1. Start Python

Open a terminal or command prompt and run the command appropriate for your installation:

```bash
python
```

Other common commands include:

```bash
python3       # Common on Linux and macOS
py            # Windows, when the Python launcher is installed
```

The exact command depends on how Python was installed and configured.

## 1.2. Two ways to run Python

### 1.2.1. Interactive mode (REPL)

Run Python without a script to enter the interactive interpreter. Type an expression or statement and press Enter to execute it immediately.

```pycon
>>> 2 + 3
5
>>> message = "Hello, Python!"
>>> print(message)
Hello, Python!
```

- `>>>` is the primary prompt.
- `...` is the continuation prompt for a statement that spans multiple lines.
- Interactive mode is useful for experimenting with syntax and testing small ideas.

Example of a multi-line statement:

```pycon
>>> number = 5
>>> if number > 0:
...     print("Positive")
...
Positive
```

### 1.2.2. Run a Python file

Save code in a file such as `hello.py`:

```python
print("Hello from a Python file!")
```

Run it from the terminal:

```bash
python hello.py
```

Use `python3 hello.py` or `py hello.py` if that is the command configured on your system.

## 1.3. Useful command-line options

### 1.3.1. Run a short command with `-c`

Use `-c` to execute Python code directly from the terminal:

```bash
python -c "print(2 + 3)"
```

Quote the command because spaces and special characters may be interpreted by the shell.

### 1.3.2. Run a module with `-m`

Use `-m` to run a module as a script:

```bash
python -m http.server
```

This example starts Python's simple local HTTP server in the current directory. Stop it with `Ctrl+C`.

### 1.3.3. Run a script and then enter interactive mode with `-i`

```bash
python -i hello.py
```

Python runs the script and then opens the interactive interpreter, allowing you to inspect objects created by the script.

## 1.4. Command-line arguments

A script can receive arguments from the command line. Python makes them available as strings in `sys.argv`.

Create `show_args.py`:

```python
import sys

print(sys.argv)
```

Run:

```bash
python show_args.py apple 42
```

`sys.argv` contains the script name followed by the arguments, approximately:

```pycon
['show_args.py', 'apple', '42']
```

Remember: command-line arguments are strings. Convert them when you need another type, such as an integer.

## 1.5. Exit the interpreter

To leave interactive mode:

- Type `quit()` and press Enter.
- Or use the end-of-file shortcut: `Ctrl+D` on Unix-like systems, or `Ctrl+Z` on Windows (then press Enter if required by the terminal).

## 1.6. Source-code encoding

Python source files use **UTF-8 by default**. This supports text from many languages in strings, comments, and identifiers.

If a file must use a different supported encoding, an encoding declaration can be placed at the beginning of the file, for example:

```python
# -*- coding: cp1252 -*-
```

For most modern projects, keep files saved as UTF-8 and ensure your editor uses UTF-8.

## 1.7. Key takeaways

- Use the interactive interpreter to try small examples quickly.
- Use `.py` files for programs you want to save and run repeatedly.
- Know the basics of `-c`, `-m`, and `-i`.
- Use `sys.argv` when a script needs command-line arguments.
- Python source files default to UTF-8.

# 2. An Informal Introduction to Python

This tutorial provides a concise summary of Chapter 3 from the official Python Documentation ("An Informal Introduction to Python"), covering basic data types, string/list manipulation, and introductory control flow.

---

## 2.1. Comments and Basics

Comments in Python start with `#` and continue to the end of the line.

```python
# this is the first comment
spam = 1 # and this is the second comment
text = "# This is not a comment because it's inside quotes."
```

---

## 2.2. Using Python as a Calculator

### 2.2.1. Numbers

Python supports integer (`int`) and floating-point (`float`) numbers out of the box.

- **Basic Arithmetic**: `+`, `-`, `*`, `/` (division always returns a `float`).
- **Floor Division & Modulo**: `//` discards the fractional part, while `%` returns the remainder.
- **Power Operator**: `**` calculates powers.

```python
>>> 2 + 2
4
>>> 8 / 5
1.6
>>> 17 // 3
5
>>> 17 % 3
2
>>> 5 ** 2
25
```

- **Variables**: Assignment uses `=`. Unassigned variables trigger a `NameError`.
- **Last Printed Expression**: In interactive mode, the variable `_` holds the last printed result.

```python
>>> price = 100.50
>>> tax = 12.5 / 100
>>> price * tax
12.5625
>>> price + _
113.0625
```

---

### 2.2.2. Text (Strings)

Strings are enclosed in single quotes (`'...'`) or double quotes (`"..."`).

- **Escaping & Raw Strings**: Use `\` to escape characters. Prefix a string with `r` to treat it as a raw string where backslashes are not escaped.

```python
>>> 'doesn\'t'
"doesn't"
>>> print('C:\this\name')    # \t is tab, \n is newline
C:	his
ame
>>> print(r'C:\this\name')   # raw string prevents escaping
C:\this\name
```

- **Multiline Strings**: Triple quotes (`"""..."""` or `'''...'''`) allow spanning multiple lines. A trailing `\` prevents an unwanted initial newline.

```python
print("""\
Usage: thingy [OPTIONS]
     -h                        Display this usage message
     -H hostname               Hostname to connect to
""")
```

- **Concatenation & Repetition**: Use `+` to concatenate and `*` to repeat. Adjacent string literals are automatically concatenated.

```python
>>> 3 * 'un' + 'ium'
'unununium'
>>> 'Py' 'thon'
'Python'
```

- **Indexing & Slicing**:
    - Positive indices start at `0` from the left.
    - Negative indices start at `-1` from the right.
    - Slicing format: `[start:end]` (start is included, end is excluded).

```python
>>> word = 'Python'
>>> word[0]
'P'
>>> word[-1]
'n'
>>> word[0:2]
'Py'
>>> word[2:]
'thon'
```

> **Key Rule**: Strings are **immutable**. You cannot assign a new value to a string index. Use `len(s)` to get string length.

---

### 2.2.3. Lists

Lists group values enclosed in square brackets `[...]`. Unlike strings, **lists are mutable**.

- **Indexing, Slicing & Concatenation**: Works identically to strings.

```python
>>> squares = [1, 4, 9, 16, 25]
>>> squares[0]
1
>>> squares + [36, 49]
[1, 4, 9, 16, 25, 36, 49]
```

- **Modifying and Appending**: Items can be replaced, and new items added with `.append()`.

```python
>>> cubes = [1, 8, 27, 65, 125]
>>> cubes[3] = 64                  # Fix incorrect value
>>> cubes.append(216)              # Append new item
>>> cubes
[1, 8, 27, 64, 125, 216]
```

- **Slice Assignment & Clearing**: Slices can replace multiple elements or clear the list.

```python
>>> letters = ['a', 'b', 'c', 'd', 'e']
>>> letters[2:4] = ['C', 'D']
>>> letters
['a', 'b', 'C', 'D', 'e']
>>> letters[:] = []                 # Clear list
>>> letters
[]
```

- **Shallow Copies & Nesting**:
    - Assignment (`rgba = rgb`) creates a reference, not a copy.
    - Slicing `rgb[:]` creates a shallow copy.
    - Lists can contain other lists (nested lists).

```python
>>> a = ['a', 'b', 'c']
>>> n = [1, 2, 3]
>>> x = [a, n]
>>> x[0][1]
'b'
```

---

## 2.3. First Steps Towards Programming

Here is a practical example using a `while` loop to output the Fibonacci sequence:

```python
# Fibonacci series: the sum of two elements defines the next
a, b = 0, 1
while a < 10:
    print(a)
    a, b = b, a + b
```

### 2.3.1. Core Concepts Introduced:

1. **Multiple Assignment**: `a, b = 0, 1` assigns `a = 0` and `b = 1` simultaneously. Right-hand expressions are evaluated before any assignment.
2. **Control Flow (`while`)**: Executes as long as the condition remains true. Any non-zero value is true; zero and empty sequences are false.
3. **Indentation**: Python uses indentation (spaces/tabs) to group statements within blocks.
4. **`print()` function**: Converts arguments to printable strings. Use `end=...` to suppress or change the default trailing newline.

```python
>>> a, b = 0, 1
>>> while a < 10:
...     print(a, end=', ')
...     a, b = b, a + b
...
0, 1, 1, 2, 3, 5, 8,
```

# 3. More Control Flow Tools

This section provides a concise summary of Chapter 4 from the official Python Documentation ("More Control Flow Tools"), covering control structures, function definitions, standard coding styles, and key features introduced in recent Python releases like match/case.

---

## 3.1. `if` Statements

The `if` statement evaluates expressions to control execution flow. It can include zero or more `elif` (short for "else if") parts, and an optional `else` block.

```python
x = int(input("Please enter an integer: "))

if x < 0:
    x = 0
    print('Negative changed to zero')
elif x == 0:
    print('Zero')
elif x == 1:
    print('Single')
else:
    print('More')
```

---

## 3.2. `for` Statements

Python’s `for` statement iterates over the items of any sequence (such as a list or a string) in the order they appear.

```python
# Measure some strings:
words = ['cat', 'window', 'defenestrate']
for w in words:
    print(w, len(w))
```

To modify a collection while iterating over it, iterate over a copy or build a new collection:

```python
# Create a sample collection
users = {'Hans': 'active', 'Éléonore': 'inactive', 'Kaguya': 'active'}

# Strategy: Iterate over a copy
for user, status in users.copy().items():
    if status == 'inactive':
        del users[user]
```

---

## 3.3. The `range()` Function

`range()` generates arithmetic progressions. It returns an iterable object that yields items on demand to save memory.

```python
>>> for i in range(5):
...     print(i)
... # Outputs: 0, 1, 2, 3, 4

>>> list(range(5, 10))
[5, 6, 7, 8, 9]

>>> list(range(0, 10, 3))
[0, 3, 6, 9]
```

Combine `range()` and `len()` to iterate over sequence indices:

```python
a = ['Mary', 'had', 'a', 'little', 'lamb']
for i in range(len(a)):
    print(i, a[i])
```

---

## 3.4. `break`, `continue`, and `else` Clauses on Loops

Loops can have an `else` clause that runs when the loop terminates normally (without hitting a `break`).

- **`break`**: Exits the innermost enclosing `for` or `while` loop.
- **`continue`**: Skips the rest of the current iteration and continues with the next.

```python
# Search for prime numbers
for n in range(2, 10):
    for x in range(2, n):
        if n % x == 0:
            print(n, 'equals', x, '*', n//x)
            break
    else:
        # loop fell through without finding a factor
        print(n, 'is a prime number')
```

---

## 3.5. The `pass` Statement

The `pass` statement does nothing. It is used as a syntactical placeholder.

```python
while True:
    pass  # Busy-wait for keyboard interrupt (Ctrl+C)

class MyEmptyClass:
    pass

def initlog(*args):
    pass  # Remember to implement this!
```

---

## 3.6. `match` Statements

Introduced in Python 3.10, `match` compares a value against pattern shapes. Only the first matching pattern executes.

```python
def http_error(status):
    match status:
        case 400:
            return "Bad request"
        case 404:
            return "Not found"
        case 418:
            return "I'm a teapot"
        case 401 | 403 | 404:
            return "Not allowed"
        case _:
            return "Something's else"
```

### 3.6.1. Pattern Matching with Shapes / Classes

```python
class Point:
    def __init__(self, x, y):
        self.x = x
        self.y = y

def where_is(point):
    match point:
        case Point(x=0, y=0):
            print("Origin")
        case Point(x=0, y=y):
            print(f"Y={y}")
        case Point(x=x, y=0):
            print(f"X={x}")
        case Point():
            print("Somewhere else")
        case _:
            print("Not a point")
```

---

## 3.7. Defining Functions

Functions are defined using the `def` keyword.

```python
def fib(n):    # write Fibonacci series up to n
    """Print a Fibonacci series up to n."""
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a + b
    print()

# Now call the function:
fib(2000)
```

Functions without an explicit `return` statement return `None`.

---

## 3.8. More on Function Arguments

### 3.8.1. Default Argument Values

Default values are evaluated **only once** at the point of function definition.

```python
def ask_ok(prompt, retries=4, reminder='Please try again!'):
    while True:
        reply = input(prompt)
        if reply in ('y', 'ye', 'yes'):
            return True
        if reply in ('n', 'no', 'nop', 'nope'):
            return False
        retries = retries - 1
        if retries < 0:
            raise ValueError('invalid user response')
        print(reminder)
```

> **Warning**: Avoid mutable default arguments (e.g., lists or dictionaries).

```python
# Correct pattern for mutable defaults:
def f(a, L=None):
    if L is None:
        L = []
    L.append(a)
    return L
```

### 3.8.2. Keyword Arguments

Functions can be called using keyword arguments of the form `kwarg=value`.

```python
def parrot(voltage, state='a stiff', action='voom', type='Norwegian Blue'):
    print("-- This parrot wouldn't", action, end=' ')
    print("if you put", voltage, "volts through it.")
    print("-- Lovely plumage, the", type)
    print("-- It's", state, "!")

# Valid calls:
parrot(1000)
parrot(voltage=1000000, action='VOOOOOM')
parrot('a thousand', state='pushing up the daisies')
```

### 3.8.3. Special Parameters (`/` and `*`)

Python allows specifying whether parameters are positional-only, positional-or-keyword, or keyword-only using `/` and `*`.

```
def f(pos1, pos2, /, pos_or_kwd, *, kwd1, kwd2):
      -----------    ----------     ----------
        |                 |             |
        |        Positional or keyword  |
        |                               - Keyword only
        -- Positional only
```

```python
def standard_arg(arg):
    print(arg)

def pos_only_arg(arg, /):
    print(arg)

def kwd_only_arg(*, arg):
    print(arg)

# Usage:
pos_only_arg(1)        # Allowed
# pos_only_arg(arg=1)  # Raises TypeError

kwd_only_arg(arg=1)    # Allowed
# kwd_only_arg(1)      # Raises TypeError
```

### 3.8.4. Arbitrary Argument Lists (`*args` and `**kwargs`)

- `*args` collects arbitrary positional arguments into a tuple.
- `**kwargs` collects arbitrary keyword arguments into a dictionary.

```python
def concat(*args, sep="/"):
    return sep.join(args)

>>> concat("earth", "mars", "venus")
'earth/mars/venus'
```

### 3.8.5. Unpacking Argument Lists

Use `*` to unpack lists/tuples for positional arguments, and `**` to unpack dictionaries for keyword arguments.

```python
>>> args = [3, 6]
>>> list(range(*args))
[3, 4, 5]

>>> d = {"voltage": "four million", "state": "bleedin' demised", "action": "VOOM"}
>>> parrot(**d)
```

### 3.8.6. Lambda Expressions

Small anonymous functions can be created with the `lambda` keyword:

```python
>>> pairs = [(1, 'one'), (2, 'two'), (3, 'three'), (4, 'four')]
>>> pairs.sort(key=lambda pair: pair[1])
>>> pairs
[(4, 'four'), (1, 'one'), (3, 'three'), (2, 'two')]
```

### 3.8.7. Documentation Strings (Docstrings)

```python
def my_function():
    """Do nothing, but document it.

    No, really, it doesn't do anything.
    """
    pass

print(my_function.__doc__)
```

### 3.8.8. Function Annotations

Annotations provide type hints for parameters and return values.

```python
def f(ham: str, eggs: str = 'eggs') -> str:
    print("Annotations:", f.__annotations__)
    return ham + ' and ' + eggs

f('spam')
```

---

## 3.9. Intermezzo: Coding Style (PEP 8)

Key guidelines from PEP 8 for clean Python code:

- Use **4-space indentation**, and no tabs.
- Wrap lines so that they don't exceed **79 characters**.
- Use blank lines to separate functions/classes and blocks of code.
- Place comments on their own line when possible.
- Use **docstrings** for functions, classes, and modules.
- Use `camelCase` for lower-level conventions only if needed, but prefer `snake_case` for functions and variable names, and `PascalCase` for class names.
- Use UTF-8 encoding for scripts.

# 4. Data Structures

This section provides a concise summary of Chapter 5 from the official Python Documentation ("Data Structures"), covering list methods, list comprehensions, `del`, tuples, sets, dictionaries, and loop techniques.

---

## 4.1. More on Lists

### 4.1.1. Common List Methods

- `append(x)`: Add an item to the end of the list.
- `extend(iterable)`: Extend the list by appending elements from the iterable.
- `insert(i, x)`: Insert an item at a given position `i`.
- `remove(x)`: Remove the first item whose value is equal to `x`.
- `pop([i])`: Remove and return the item at position `i` (defaults to the last item).
- `clear()`: Remove all items from the list.
- `index(x)`: Return zero-based index of the first item matching `x`.
- `count(x)`: Return number of times `x` appears.
- `sort(key=None, reverse=False)`: Sort items in place.
- `reverse()`: Reverse elements in place.
- `copy()`: Return a shallow copy of the list.

```python
>>> fruits = ['orange', 'apple', 'pear', 'banana', 'kiwi', 'apple', 'banana']
>>> fruits.count('apple')
2
>>> fruits.index('banana')
3
>>> fruits.reverse()
>>> fruits
['banana', 'apple', 'kiwi', 'banana', 'pear', 'apple', 'orange']
>>> fruits.sort()
>>> fruits
['apple', 'apple', 'banana', 'banana', 'kiwi', 'orange', 'pear']
>>> fruits.pop()
'pear'
```

---

### 4.1.2. Using Lists as Stacks (LIFO)

To use a list as a stack (Last-In, First-Out), use `append()` to push items and `pop()` (without arguments) to retrieve items.

```python
>>> stack = [3, 4, 5]
>>> stack.append(6)
>>> stack.append(7)
>>> stack
[3, 4, 5, 6, 7]
>>> stack.pop()
7
>>> stack
[3, 4, 5, 6]
```

---

### 4.1.3. Using Lists as Queues (FIFO)

Lists are inefficient for queues (First-In, First-Out) because inserts/pops at the beginning are $O(n)$. Use `collections.deque` instead.

```python
>>> from collections import deque
>>> queue = deque(["Eric", "John", "Michael"])
>>> queue.append("Terry")           # Terry arrives
>>> queue.append("Graham")          # Graham arrives
>>> queue.popleft()                 # The first to arrive now leaves
'Eric'
>>> queue.popleft()                 # The second to arrive now leaves
'John'
>>> queue                           # Remaining queue in order of arrival
deque(['Michael', 'Terry', 'Graham'])
```

---

### 4.1.4. List Comprehensions

List comprehensions provide a concise way to create lists.

```python
# Create a list of squares
>>> squares = [x**2 for x in range(10)]
>>> squares
[0, 1, 4, 9, 16, 25, 36, 49, 64, 81]

# Combine elements from two lists if they are not equal
>>> [(x, y) for x in [1,2,3] for y in [3,1,4] if x != y]
[(1, 3), (1, 4), (2, 3), (2, 1), (2, 4), (3, 1), (3, 4)]
```

- **Flattening a list using a listcomp**:

```python
>>> vec = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
>>> [num for elem in vec for num in elem]
[1, 2, 3, 4, 5, 6, 7, 8, 9]
```

---

### 4.1.5. Nested List Comprehensions

The initial expression in a list comprehension can be any arbitrary expression, including another list comprehension.

```python
>>> matrix = [
...     [1, 2, 3, 4],
...     [5, 6, 7, 8],
...     [9, 10, 11, 12],
... ]

# Transpose rows and columns:
>>> [[row[i] for row in matrix] for i in range(4)]
[[1, 5, 9], [2, 6, 10], [3, 7, 11], [4, 8, 12]]

# Equivalent built-in approach:
>>> list(zip(*matrix))
[(1, 5, 9), (2, 6, 10), (3, 7, 11), (4, 8, 12)]
```

---

## 4.2. The `del` Statement

Unlike `pop()`, `del` removes an item or slice by index without returning a value, or deletes an entire variable.

```python
>>> a = [-1, 1, 66.25, 333, 333, 1234.5]
>>> del a[0]
>>> a
[1, 66.25, 333, 333, 1234.5]
>>> del a[2:4]
>>> a
[1, 66.25, 1234.5]
>>> del a[:]
>>> a
[]
```

---

## 4.3. Tuples and Sequences

A tuple consists of comma-separated values. Tuples are **immutable** and can contain mutable objects.

```python
>>> t = 12345, 54321, 'hello!'
>>> t[0]
12345
>>> t
(12345, 54321, 'hello!')

# Tuples may be nested:
>>> u = t, (1, 2, 3, 4, 5)
>>> u
((12345, 54321, 'hello!'), (1, 2, 3, 4, 5))

# Empty and single-item tuples:
>>> empty = ()
>>> singleton = 'hello',    # <-- note trailing comma
>>> len(empty)
0
>>> len(singleton)
1
```

- **Tuple Packing & Unpacking**:

```python
>>> t = 12345, 54321, 'hello!' # Tuple packing
>>> x, y, z = t                # Sequence unpacking
```

---

## 4.4. Sets

A set is an unordered collection with **no duplicate elements**. Sets support mathematical operations like union, intersection, difference, and symmetric difference.

```python
>>> basket = {'apple', 'orange', 'apple', 'pear', 'orange', 'banana'}
>>> print(basket)                      # show that duplicates have been removed
{'orange', 'banana', 'pear', 'apple'}
>>> 'orange' in basket                 # fast membership testing
True

# Set operations on unique letters from two words:
>>> a = set('abracadabra')
>>> b = set('alacazam')
>>> a - b                              # letters in a but not in b
{'r', 'd', 'b'}
>>> a | b                              # letters in a or b or both
{'a', 'c', 'r', 'd', 'b', 'm', 'z', 'l'}
>>> a & b                              # letters in both a and b
{'a', 'c'}
>>> a ^ b                              # letters in a or b but not both
{'r', 'd', 'b', 'm', 'z', 'l'}
```

- **Set Comprehensions**:

```python
>>> a = {x for x in 'abracadabra' if x not in 'abc'}
>>> a
{'r', 'd'}
```

---

## 4.5. Dictionaries

Dictionaries are indexed by **keys** (which can be any immutable type, such as strings, numbers, or tuples of immutable elements).

```python
>>> tel = {'jack': 4098, 'sape': 4139}
>>> tel['guido'] = 4127
>>> tel
{'jack': 4098, 'sape': 4139, 'guido': 4127}
>>> tel['jack']
4098
>>> del tel['sape']
>>> list(tel)
['jack', 'guido']
>>> 'guido' in tel
True
```

- **Constructing Dictionaries**:

```python
# Using dict() on sequence of key-value pairs:
>>> dict([('sape', 4139), ('guido', 4127), ('jack', 4098)])
{'sape': 4139, 'guido': 4127, 'jack': 4098}

# Dict comprehensions:
>>> {x: x**2 for x in (2, 4, 6)}
{2: 4, 4: 16, 6: 36}

# Keyword arguments (when keys are simple strings):
>>> dict(sape=4139, guido=4127, jack=4098)
{'sape': 4139, 'guido': 4127, 'jack': 4098}
```

---

## 4.6. Looping Techniques

- **`items()`**: Loop over key and value in dictionaries simultaneously.

```python
>>> knights = {'gallahad': 'the pure', 'robin': 'the brave'}
>>> for k, v in knights.items():
...     print(k, v)
...
gallahad the pure
robin the brave
```

- **`enumerate()`**: Retrieve position index and corresponding value.

```python
>>> for i, v in enumerate(['tic', 'tac', 'toe']):
...     print(i, v)
...
0 tic
1 tac
2 toe
```

- **`zip()`**: Loop over two or more sequences at the same time.

```python
>>> questions = ['name', 'quest', 'favorite color']
>>> answers = ['lancelot', 'the holy grail', 'blue']
>>> for q, a in zip(questions, answers):
...     print(f'What is your {q}?  It is {a}.')
...
What is your name?  It is lancelot.
What is your quest?  It is the holy grail.
What is your favorite color?  It is blue.
```

- **`reversed()`**: Loop over a sequence in reverse.

```python
>>> for i in reversed(range(1, 10, 2)):
...     print(i)
...
9
7
5
3
1
```

- **`sorted()`**: Loop over a sequence in sorted order without modifying the source.

```python
>>> basket = ['apple', 'orange', 'apple', 'pear', 'orange', 'banana']
>>> for i in sorted(set(basket)):
...     print(i)
...
apple
banana
orange
```

---

## 4.7. Conditions & Comparing Sequences

- **Operators**: `in` / `not in` (membership), `is` / `is not` (identity).
- **Chaining**: Comparisons can be chained (e.g., `a < b == c`).
- **Boolean Operators**: `and`, `or`, `not` (evaluated short-circuit).
- **Lexicographical Comparison**: Sequences are compared lexicographically by first comparing the first two items, then the next two, and so on.

```python
(1, 2, 3)              < (1, 2, 4)
[1, 2, 3]              < [1, 2, 4]
'ABC' < 'Pascal' < 'Python'
(1, 2, ('aa', 'ab'))   < (1, 2, ('abc', 'a'), 4)
```

# 5. Modules

This section provides a concise summary of Chapter 6 from the official Python Documentation ("Modules"), covering how to organize code into modules, use the module search path, inspect definitions with `dir()`, and structure packages.

---

## 5.1. More on Modules

A module is a file containing Python definitions and statements. The file name is the module name with the suffix `.py` appended.

Suppose you have a file named `fibo.py` containing:

```python
def fib(n):    # write Fibonacci series up to n
    a, b = 0, 1
    while a < n:
        print(a, end=' ')
        a, b = b, a + b
    print()

def fib2(n):   # return Fibonacci series up to n
    result = []
    a, b = 0, 1
    while a < n:
        result.append(a)
        a, b = b, a + b
    return result
```

You can import this module into another Python module or the interactive interpreter:

```python
>>> import fibo
>>> fibo.fib(1000)
0 1 1 2 3 5 8 13 21 34 55 89 144 233 377 610 987
>>> fibo.fib2(100)
[0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89]
>>> fibo.__name__
'fibo'
```

### 5.1.1. Importing Specific Names or All Names

```python
# Import a specific function directly
>>> from fibo import fib, fib2
>>> fib(500)

# Give an imported name an alias
>>> from fibo import fib as fibonacci
>>> fibonacci(500)

# Import all names defined in a module (not recommended for production code)
>>> from fibo import *
```

---

## 5.2. Executing Modules as Scripts

When you run a Python module with:

```bash
python fibo.py <arguments>
```

The code in the module will be executed, just as if you imported it, but with the `__name__` set to `"__main__"`.

You can add code at the end of your module to make it usable as a script as well as an importable module:

```python
if __name__ == "__main__":
    import sys
    fib(int(sys.argv[1]))
```

---

## 5.3. The Module Search Path

When a module named `spam` is imported, the interpreter searches for a file named `spam.py` in:

1. The directory from which the input script was run.
2. The list of directories in `sys.path` (derived from the directory containing the input script, `PYTHONPATH`, and installation defaults).

```python
>>> import sys
>>> sys.path.append('/path/to/my/modules')
```

### 5.3.1. "Compiled" Python Files

To speed up loading modules, Python caches a compiled version of each module in the `__pycache__` directory under the name `module.version.pyc`.

---

## 5.4. Standard Modules

Python comes with a library of standard modules. One particularly notable built-in module is `sys`, which is built into every Python interpreter.

```python
>>> import sys
>>> sys.ps1
'>>> '
>>> sys.ps2.      # Continuation prompt
...
```

---

## 5.5. The `dir()` Function

The built-in function `dir()` is used to find out which names a module defines. It returns a sorted list of strings.

```python
>>> import fibo
>>> dir(fibo)
['__name__', 'fib', 'fib2']
```

When called without arguments, `dir()` lists the names you currently have defined:

```python
>>> a = [1, 2, 3, 4, 5]
>>> import fibo
>>> dir()
['__builtins__', '__name__', 'a', 'fibo']
```

---

## 5.6. Packages

Packages are a way of structuring Python’s module namespace by using "dotted module names". For example, a module name `A.B` designates a submodule `B` in a package named `A`.

### 5.6.1. Directory Structure Example:

```text
sound/                          <- Top-level package
      __init__.py               <- Initialize the sound package
      effects/                  <- Subpackage for sound effects
              __init__.py
              echo_effect.py
      filters/                  <- Subpackage for filters
              __init__.py
              equalizer.py
```

### 5.6.2. Importing Packages

- **Importing a submodule**:
    ```python
    import sound.effects.echo_effect
    sound.effects.echo_effect.echofilter(input, output, delay=0.7)
    ```
- **Importing with `from ... import`**:
    ```python
    from sound.effects import echo_effect
    echo_effect.echofilter(input, output, delay=0.7)
    ```
- **Importing specific functions/attributes**:
    ```python
    from sound.effects.echo_effect import echofilter
    echofilter(input, output, delay=0.7)
    ```

### 5.6.3. Note on `import *`

If a package's `__init__.py` code defines a list named `__all__`, it is taken to be the list of module names that should be cuando `from package import *` is used.

```python
# In sound/effects/__init__.py
__all__ = [
    "echo_effect",
    "surround",
    "reverse",
]
```

# 6. Input and Output

This section provides a concise summary of Chapter 7 from the official Python Documentation ("Input and Output"), covering string formatting methods, basic file operations, and working with JSON.

## 6.1. Fancier Output Formatting

Python provides several ways to format string output:

- **Formatted string literals (f-strings)**
- **The `str.format()` method**
- **Manual string slicing and concatenation** using methods like `str.rjust()` or `str.zfill()`

---

### 6.1.1. Formatted String Literals (f-strings)

Prefix the string with `f` or `F` and include expressions written as `{expression}`.

- **Format Specifiers**: Add `:` followed by a format specifier to control rounding, padding, or alignment.

```python
>>> import math
>>> print(f'The value of pi is approximately {math.pi:.3f}.')
The value of pi is approximately 3.142.
```

- **Field Widths**: Passing an integer after `:` specifies minimum character width.

```python
>>> table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 7678}
>>> for name, phone in table.items():
...     print(f'{name:10} ==> {phone:10d}')
...
Sjoerd     ==>       4127
Jack       ==>       4098
Dcab       ==>       7678
```

- **Conversion Flags**: Use `!s` (applies `str()`), `!r` (applies `repr()`), or `!a` (applies `ascii()`).

```python
>>> animals = 'eels'
>>> print(f'My hovercraft is full of {animals!r}.')
My hovercraft is full of 'eels'.
```

- **Self-documenting Expressions (`=`)**: Introduced in Python 3.8, outputting the variable name and value.

```python
>>> bugs = 'roaches'
>>> count = 13
>>> print(f'{count=} {bugs=}')
count=13 bugs='roaches'
```

---

### 6.1.2. The String `format()` Method

Uses `{}` positional or keyword placeholders inside strings.

```python
>>> print('We are the {} who say "{}"!'.format('knights', 'Ni'))
We are the knights who say "Ni"!

# Positional indexing
>>> print('{0} and {1}'.format('spam', 'eggs'))
spam and eggs

# Keyword arguments
>>> print('This {food} is {adjective}.'.format(
...       food='spam', adjective='absolutely horrible'))
This spam is absolutely horrible.
```

- **Unpacking Dictionaries**: Use `**` to unpack keyword arguments directly.

```python
>>> table = {'Sjoerd': 4127, 'Jack': 4098, 'Dcab': 8637678}
>>> print('Jack: {Jack:d}; Sjoerd: {Sjoerd:d}; Dcab: {Dcab:d}'.format(**table))
Jack: 4098; Sjoerd: 4127; Dcab: 8637678
```

---

### 6.1.3. Manual String Formatting

- `str.rjust(width)`: Right-aligns string in a field of given width.
- `str.ljust(width)`: Left-aligns string.
- `str.center(width)`: Centers string.
- `str.zfill(width)`: Pads a numeric string with zeros on the left.

```python
>>> '12'.zfill(5)
'00012'
>>> '-3.14'.zfill(7)
'-0003.14'
```

---

## 6.2. Reading and Writing Files

### 6.2.1. Opening Files

`open(filename, mode, encoding=None)` returns a file object. Always specify `encoding="utf-8"` when reading or writing text files.

Modes:

- `'r'`: Read (default).
- `'w'`: Write (overwrites existing files).
- `'a'`: Append.
- `'r+'`: Read and write.
- `'b'`: Binary mode (appending `b` to mode).

### 6.2.2. Using `with` Statements

Using `with` ensures files are properly closed even if exceptions occur.

```python
with open('workfile', 'w', encoding='utf-8') as f:
    f.write('This is a test\n')
```

---

### 6.2.3. Methods of File Objects

- **`f.read(size)`**: Reads and returns specified content length (or entire file if size is omitted/negative).

```python
>>> f.read()
'This is a test\n'
>>> f.read()    # Returns empty string at end-of-file (EOF)
''
```

- **`f.readline()`**: Reads a single line ending in `\n`.

```python
>>> f.readline()
'This is the first line of the file.\n'
```

- **Iterating over a file line-by-line** (memory efficient):

```python
for line in f:
    print(line, end='')
```

- **`f.readlines()` or `list(f)`**: Reads all lines into a list.

```python
>>> list(f)
['This is the first line.\n', 'This is the second line.\n']
```

- **`f.write(string)`**: Writes the string content to the file and returns the number of characters written.

```python
>>> f.write('This is a test\n')
15
```

- **`f.tell()` and `f.seek(offset, whence=0)`**:
    - `f.tell()` returns the current file pointer position (bytes from start).
    - `f.seek(offset, whence)` changes file position.
        - `whence=0` (default): relative to start.
        - `whence=1`: relative to current position.
        - `whence=2`: relative to end.

```python
>>> f = open('workfile', 'rb+')
>>> f.write(b'0123456789abcdef')
16
>>> f.seek(5)      # Go to 6th byte
5
>>> f.read(1)
b'5'
>>> f.seek(-3, 2)  # Go to 3rd byte from end
13
>>> f.read(1)
b'd'
```

---

## 6.3. Saving Structured Data with `json`

Instead of manually parsing complex data types, Python’s built-in `json` module translates Python hierarchies into JSON string representations (serialization).

- **`json.dumps(obj)`**: Serializes `obj` to a JSON-formatted string.

```python
>>> import json
>>> x = [1, 'simple', 'list']
>>> json.dumps(x)
'[1, "simple", "list"]'
```

- **`json.dump(obj, fp)`**: Serializes `obj` directly to an open writeable file object.

```python
with open('data.json', 'w', encoding='utf-8') as f:
    json.dump(x, f)
```

- **`json.load(fp)`**: Reads and deserializes JSON data from an open readable file object back into a Python object.

```python
with open('data.json', 'r', encoding='utf-8') as f:
    x = json.load(f)
```

# 7. Errors and Exceptions

This section provides a concise summary of Chapter 8 from the official Python Documentation ("Errors and Exceptions"), covering syntax errors, handling exceptions, raising exceptions, user-defined exceptions, cleanup actions, and exception chaining.

---

## 7.1. Syntax Errors vs. Exceptions

### 7.1.1. Syntax Errors (Parsing Errors)

Syntax errors occur when Python cannot parse your code because it violates the language rules.

```python
>>> while True print('Hello world')
  File "<stdin>", line 1
    while True print('Hello world')
               ^^^^^
SyntaxError: invalid syntax
```

### 7.1.2. Exceptions

Even if a statement or expression is syntactically correct, it may cause an error when executed. Errors detected during execution are called _exceptions_.

```python
>>> 10 * (1/0)
ZeroDivisionError: division by zero
>>> 4 + spam * 3
NameError: name 'spam' is not defined
>>> '2' + 2
TypeError: can't concat str to int
```

---

## 7.2. Handling Exceptions

Use `try` ... `except` blocks to handle exceptions gracefully.

```python
while True:
    try:
        x = int(input("Please enter a number: "))
        break
    except ValueError:
        print("Oops!  That was no valid number.  Try again...")
```

### 7.2.1. Handling Multiple Exceptions

An `except` clause may name multiple exceptions as a parenthesized tuple:

```python
try:
    ...
except (RuntimeError, TypeError, NameError):
    pass
```

### 7.2.2. Accessing the Exception Instance

You can bind the exception instance to a variable using `as`:

```python
try:
    raise Exception('spam', 'eggs')
except Exception as inst:
    print(type(inst))    # <class 'Exception'>
    print(inst.args)     # ('spam', 'eggs')
    print(inst)          # ('spam', 'eggs')
    x, y = inst.args     # unpack args
    print('x =', x)
    print('y =', y)
```

### 7.2.3. The `else` Clause

The optional `else` clause executes if the `try` block **does not** raise an exception.

```python
for arg in sys.argv[1:]:
    try:
        f = open(arg, 'r')
    except OSError:
        print('cannot open', arg)
    else:
        print(arg, 'has', len(f.readlines()), 'lines')
        f.close()
```

---

## 7.3. Raising Exceptions

The `raise` statement allows you to force a specified exception to occur.

```python
>>> raise NameError('HiThere')
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: HiThere
```

If you want to determine whether an exception was raised but don't intend to handle it, a simpler form allows you to re-raise it:

```python
try:
    raise NameError('HiThere')
except NameError:
    print('An exception flew by!')
    raise
```

---

## 7.4. Exception Chaining

If an unhandled exception occurs inside an `except` section, it will have the exception being handled attached to it and included in the error message.

You can explicitly indicate that an exception is a direct consequence of another using `from`:

```python
def func():
    raise ConnectionError

try:
    func()
except ConnectionError as exc:
    raise RuntimeError('Failed to open database') from exc
```

To disable automatic exception chaining, use `from None`:

```python
try:
    open('database.sqlite')
except OSError:
    raise RuntimeError("Base is inaccessible") from None
```

---

## 7.5. User-defined Exceptions

Programs may create their own exceptions by defining a new class that inherits from `Exception` (directly or indirectly).

```python
class CustomError(Exception):
    """Exception raised for custom error conditions."""
    def __init__(self, message, code):
        self.message = message
        self.code = code
        super().__init__(self.message)

try:
    raise CustomError("Something went wrong", 500)
except CustomError as e:
    print(f"Error Code {e.code}: {e.message}")
```

---

## 7.6. Clean-up Actions (`finally`)

The `finally` clause always executes before leaving the `try` statement, whether an exception occurred or not.

```python
def bool_return():
    try:
        return True
    finally:
        return False

>>> bool_return()
False
```

A practical example involving file cleanup:

```python
def divide(x, y):
    try:
        result = x / y
    except ZeroDivisionError:
        print("division by zero!")
    else:
        print("result is", result)
    finally:
        print("executing finally clause")

>>> divide(2, 1)
result is 2.0
executing finally clause

>>> divide(2, 0)
division by zero!
executing finally clause
```

---

## 7.7. Predefined Clean-up Actions

Some objects define standard clean-up actions to be executed when the object is no longer needed, using the `with` statement.

```python
# Without 'with' - file might remain open if an error occurs
for line in open("myfile.txt"):
    print(line, end="")

# With 'with' - guarantees file is properly closed
with open("myfile.txt") as f:
    for line in f:
        print(line, end="")
```

---

## 7.8. Raising and Handling Multiple Unrelated Exceptions (`ExceptionGroup`)

Introduced in Python 3.11, `ExceptionGroup` allows raising multiple exceptions together, handled using `except*`.

```python
try:
    raise ExceptionGroup(
        "sys-group",
        [
            SystemError(1),
            TypeError("invalid type"),
        ]
    )
except* SystemError as eg:
    print("Handled SystemError")
except* TypeError as eg:
    print("Handled TypeError")
```

---

## 7.9. Enriching Exceptions with Notes

Python 3.11 introduced `add_note()` to attach contextual information to exceptions without modifying the exception message.

```python
try:
    raise TypeError('bad type')
except Exception as e:
    e.add_note('Happened in function process_data()')
    e.add_note('User ID: 12345')
    raise
```

# 8. Classes

This section provides a concise summary of Chapter 9 from the official Python Documentation ("Classes"), covering namespaces, class/instance objects, inheritance, private variables, iterators, generators, and generator expressions.

---

## 8.1. A Word About Namespaces and Scopes

- **Namespace**: A mapping from names to objects. Examples include built-in names, global names in a module, and local names in a function call.
- **Scope**: A textual region of a Python program where a namespace is directly accessible.
- **LEGB Rule**: Scope lookup follows **L**ocal $\rightarrow$ **E**nclosing $\rightarrow$ **G**lobal $\rightarrow$ **B**uilt-in.

### 8.1.1. Global and Nonlocal Keywords

- `global`: Rebinds variables in the module-level global scope.
- `nonlocal`: Rebinds variables in nearest outer enclosing scope (excluding globals).

```python
def scope_test():
    def do_local():
        spam = "local spam"

    def do_nonlocal():
        nonlocal spam
        spam = "nonlocal spam"

    def do_global():
        global spam
        spam = "global spam"

    spam = "test spam"
    do_local()
    print("After local assignment:", spam)       # test spam
    do_nonlocal()
    print("After nonlocal assignment:", spam)    # nonlocal spam
    do_global()
    print("After global assignment:", spam)      # nonlocal spam

scope_test()
print("In global scope:", spam)                  # global spam
```

---

## 8.2. A First Look at Classes

### 8.2.1. Class Definition Syntax

```python
class ClassName:
    <statement-1>
    ...
    <statement-N>
```

### 8.2.2. Class Objects & Instantiation

Classes support two kinds of operations: **attribute references** and **instantiation**.

```python
class MyClass:
    """A simple example class"""
    i = 12345

    def f(self):
        return 'hello world'

# Attribute references:
>>> MyClass.i
12345

# Instantiation:
>>> x = MyClass()
>>> x.f()
'hello world'
```

### 8.2.3. The `__init__()` Method

The `__init__()` method automatically runs when a class is instantiated.

```python
class Complex:
    def __init__(self, realpart, imagpart):
        self.r = realpart
        self.i = imagpart

x = Complex(3.0, -4.5)
>>> x.r, x.i
(3.0, -4.5)
```

---

## 8.3. Class and Instance Variables

- **Class variables**: Shared by all instances of the class.
- **Instance variables**: Unique to each instance.

```python
class Dog:
    kind = 'canine'         # Class variable shared by all instances

    def __init__(self, name):
        self.name = name    # Instance variable unique to each instance

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.kind                  # Shared
'canine'
>>> d.name                  # Unique
'Fido'
```

> **Warning with Mutable Class Variables**: If a class variable is mutable (like a `list`), modifying it affects **all** instances!

```python
class Dog:
    tricks = []             # Mistake: Shared mutable class variable

    def add_trick(self, trick):
        self.tricks.append(trick)

>>> d = Dog('Fido')
>>> e = Dog('Buddy')
>>> d.add_trick('roll over')
>>> e.tricks                # Unexpectedly shared!
['roll over']
```

**Correct implementation using instance variables:**

```python
class Dog:
    def __init__(self, name):
        self.name = name
        self.tricks = []    # Creates a new empty list for each dog

    def add_trick(self, trick):
        self.tricks.append(trick)
```

---

## 8.4. Inheritance

Python supports single and multiple inheritance.

```python
class DerivedClassName(BaseClassName):
    <statement-1>
    ...
    <statement-N>
```

### 8.4.1. Overriding Methods & Built-in Functions

- Derived methods can override base class methods.
- **`isinstance(obj, Class)`**: Returns `True` if `obj` is an instance of `Class` or a derived class.
- **`issubclass(sub, sup)`**: Returns `True` if `sub` is a subclass of `sup`.

```python
>>> isinstance(x, Complex)
True
>>> issubclass(bool, int)
True
```

### 8.4.2. Multiple Inheritance

```python
class DerivedClassName(Base1, Base2, Base3):
    <statement-1>
    ...
    <statement-N>
```

Python uses **Method Resolution Order (MRO)** (C3 Linearization) to resolve attributes across multiple base classes dynamically.

---

## 8.5. Private Variables (`__name`)

Python has no strict "private" keyword, but prefixes with **two leading underscores** trigger **name mangling** (converting `__item` to `_ClassName__item`).

```python
class Mapping:
    def __init__(self, iterable):
        self.items_list = []
        self.__update(iterable)

    def update(self, iterable):
        for item in iterable:
            self.items_list.append(item)

    __update = update   # Private copy of original update() method

class MappingSubclass(Mapping):
    # Overrides update() without breaking Mapping.__init__()
    def update(self, keys, values):
        for item in zip(keys, values):
            self.items_list.append(item)
```

---

## 8.6. Iterators

Most container objects can be looped over using a `for` statement. Behind the scenes, `for` calls `iter()` on the object, which returns an iterator defining `__next__()`.

```python
class Reverse:
    """Iterator for looping over a sequence backwards."""
    def __init__(self, data):
        self.data = data
        self.index = len(data)

    def __iter__(self):
        return self

    def __next__(self):
        if self.index == 0:
            raise StopIteration
        self.index = self.index - 1
        return self.data[self.index]

>>> rev = Reverse('spam')
>>> for char in rev:
...     print(char)
...
m
a
p
s
```

---

## 8.7. Generators

Generators are a simple and powerful tool for creating iterators. They are written like regular functions but use `yield` whenever they want to return data.

```python
def reverse(data):
    for index in range(len(data)-1, -1, -1):
        yield data[index]

>>> for char in reverse('golf'):
...     print(char)
...
f
l
o
g
```

Key features of Generators:

- State and local variables are saved automatically between calls.
- Automatically raise `StopIteration` when they exit.

---

## 8.8. Generator Expressions

Generator expressions are concise syntax for creating simple generators, written similarly to list comprehensions but using **parentheses `()`** instead of square brackets `[]`.

```python
>>> sum(i*i for i in range(10))                 # sum of squares
285

>>> xvec = [10, 20, 30]
>>> yvec = [7, 5, 3]
>>> sum(x*y for x, y in zip(xvec, yvec))         # dot product
260

>>> data = 'golf'
>>> list(data[i] for i in range(len(data)-1, -1, -1))
['f', 'l', 'o', 'g']
```

# 9. Brief Tour of the Standard Library (Part - I)

This section provides a concise summary of Chapter 10 from the official Python Documentation ("Brief Tour of the Standard Library"), covering key modules for operating system interfaces, file wildcarding, command-line arguments, math, internet access, dates, data compression, performance measurement, quality control, and batteries included.

---

## 9.1. Operating System Interface

The `os` module provides functions for interacting with the operating system.

```python
>>> import os
>>> os.getcwd()      # Return the current working directory
'C:\\Python313'
>>> os.chdir('/server/accesslogs')   # Change current working directory
>>> os.system('mkdir today')         # Run the command mkdir in the system shell
0
```

> **Tip**: Use `import os` instead of `from os import *` to prevent `os.open()` from shadowing the built-in `open()` function.

For daily file and directory management tasks, the `shutil` module provides a higher-level interface:

```python
>>> import shutil
>>> shutil.copyfile('data.db', 'archive.db')
'archive.db'
>>> shutil.move('/build/bin/notneeded', '/tmp/')
'/tmp/notneeded'
```

---

## 9.2. File Wildcards

The `glob` module provides a function for making file lists from directory wildcard searches.

```python
>>> import glob
>>> glob.glob('*.py')
['primes.py', 'random.py', 'quote.py']
```

---

## 9.3. Command Line Arguments

Command line arguments are stored in the `sys` module's `argv` attribute as a list.

```python
# Save as demo.py
import sys
print(sys.argv)
```

Running `python demo.py one two three` outputs:
`['demo.py', 'one', 'two', 'three']`

For parsing command-line options, use `argparse`:

```python
import argparse

parser = argparse.ArgumentParser(prog='top', description='Show top lines of a file')
parser.add_argument('filename')
parser.add_argument('-l', '--lines', type=int, default=10)
args = parser.parse_args()
```

---

## 9.4. Error Output Redirection and Program Termination

The `sys` module also has attributes for `stdin`, `stdout`, and `stderr`.

```python
>>> sys.stderr.write('Warning, log file not found\n')
Warning, log file not found
```

To terminate a script, use `sys.exit()`.

---

## 9.5. String Pattern Matching

The `re` module provides regular expression tools for advanced string processing.

```python
>>> import re
>>> re.findall(r'\bf[a-z]*', 'which foot or hand fell fastest')
['foot', 'fell', 'fastest']
>>> re.sub(r'(\b[a-z]+) \1', r'\1', 'cat in the the hat')
'cat in the hat'
```

When only simple string operations are needed, standard string methods are preferred:

```python
>>> 'tea for two'.replace('two', 'too')
'tea for too'
```

---

## 9.6. Mathematics

The `math` module gives access to the underlying C library functions for floating-point math:

```python
>>> import math
>>> math.cos(math.pi / 4)
0.7071067811865476
>>> math.log(1024, 2)
10.0
```

The `random` module provides tools for making random selections:

```python
>>> import random
>>> random.choice(['apple', 'pear', 'banana'])
'apple'
>>> random.sample(range(100), 10)   # sampling without replacement
[30, 83, 16, 4, 8, 81, 41, 50, 1, 63]
>>> random.random()    # random float in [0.0, 1.0)
0.17970987893696115
>>> random.randrange(6)    # random integer chosen from range(6)
4
```

The `statistics` module calculates basic statistical properties:

```python
>>> import statistics
>>> data = [2.75, 1.75, 1.25, 0.25, 0.5, 1.25, 3.5]
>>> statistics.mean(data)
1.6071428571428572
>>> statistics.median(data)
1.25
>>> statistics.variance(data)
1.3720238095238095
```

---

## 9.7. Internet Access

Modules exist for accessing the internet and processing protocols:

- `urllib.request` for retrieving data from URLs.
- `smtplib` for sending mail.

```python
from urllib.request import urlopen
with urlopen('http://worldtimeapi.org/api/timezone/etc/UTC.txt') as response:
    for line in response:
        line = line.decode()             # Convert bytes to a str
        if line.startswith('datetime'):
            print(line.rstrip())         # datetime: 2023-08-01T12:00:00.000000+00:00
```

---

## 9.8. Dates and Times

The `datetime` module supplies classes for manipulating dates and times.

```python
>>> from datetime import date
>>> now = date.today()
>>> now
datetime.date(2023, 8, 1)
>>> now.strftime("%m-%d-%y. %d %b %Y is a %A on the %d day of %B.")
'08-01-23. 01 Aug 2023 is a Tuesday on the 01 day of August.'

# Dates support calendar arithmetic:
>>> birthday = date(1964, 7, 31)
>>> age = now - birthday
>>> age.days
21550
```

---

## 9.9. Data Compression

Common data compression and archiving formats are supported directly through modules like `zlib`, `gzip`, `bz2`, `lzma`, `zipfile`, and `tarfile`.

```python
>>> import zlib
>>> s = b'witch which has which witches wrist watch'
>>> len(s)
41
>>> t = zlib.compress(s)
>>> len(t)
37
>>> zlib.decompress(t)
b'witch which has which witches wrist watch'
>>> zlib.crc32(s)
226805979
```

---

## 9.10. Performance Measurement

The `timeit` module measures code execution speed.

```python
>>> from timeit import Timer
>>> Timer('t=a; a=b; b=t', 'a=1; b=2').timeit()
0.032719300000000005
>>> Timer('a, b = b, a', 'a=1; b=2').timeit()
0.027007200000000002
```

---

## 9.11. Quality Control

### 9.11.1. `doctest`

Scans docstrings for tests embedded in example python interactive sessions:

```python
def average(values):
    """Computes the arithmetic mean of a list of numbers.

    >>> print(average([20, 30, 70]))
    40.0
    """
    return sum(values) / len(values)

import doctest
doctest.testmod()   # Automatically validates the embedded tests
```

### 9.11.2. `unittest`

A comprehensive framework for writing unit tests:

```python
import unittest

class TestStatisticalFunctions(unittest.TestCase):

    def test_average(self):
        self.assertEqual(average([20, 30, 70]), 40.0)
        self.assertEqual(round(average([1, 5, 7]), 1), 4.3)
        with self.assertRaises(ZeroDivisionError):
            average([])
        with self.assertRaises(TypeError):
            average(20, 30, 70)

unittest.main() # Calling from the command line invokes all tests
```

---

## 9.12. Batteries Included

Python philosophy is "batteries included," meaning standard packages handle many common tasks:

- `xmlrpc.client` and `xmlrpc.server` for remote procedure calls.
- `email` package for managing email messages (MIME, attachments).
- `html` and `xml` packages for parsing markup formats.
- `sqlite3` for light embedded relational SQL databases.
- `gettext`, `locale` for internationalization (i18n).

# 10. Brief Tour of the Standard Library — Part II

This section provides a concise summary of Chapter 11 from the official Python Documentation ("Brief Tour of the Standard Library — Part II"), covering advanced modules for output formatting, templating, binary data layout, multi-threading, logging, weak references, list tools, decimal arithmetic, and more.

---

## 10.1. Output Formatting

### 10.1.1. `reprlib`

Provides a version of `repr()` customized for abbreviated displays of large or deeply nested containers.

```python
>>> import reprlib
>>> reprlib.repr(set('supercalifragilisticexpialidocious'))
"{'a', 'c', 'd', 'e', 'f', 'g', ...}"
```

### 10.1.2. `pprint`

Pretty-prints Python data structures in a form that can be read by the interpreter.

```python
>>> import pprint
>>> t = [[[['black', 'cyan'], 'white'], ['green', 'red']], [['magenta', 'yellow'], 'blue']]
>>> pprint.pprint(t, width=30)
[[[['black', 'cyan'],
   'white'],
  ['green', 'red']],
 [['magenta', 'yellow'],
  'blue']]
```

### 10.1.3. `textwrap`

Formats paragraphs of text to fit a specified screen width.

```python
>>> import textwrap
>>> doc = """The wrap() method is like fill() except that it returns
... a list of strings instead of one big string with newlines to
... separate the wrapped lines."""
>>> print(textwrap.fill(doc, width=40))
The wrap() method is like fill() except
that it returns a list of strings
instead of one big string with newlines
to separate the wrapped lines.
```

### 10.1.4. `locale`

Accesses a database of culture-specific data formats (e.g., currency formatting).

```python
>>> import locale
>>> locale.setlocale(locale.LC_ALL, 'English_United States.1252')
'English_United States.1252'
>>> conv = locale.localeconv()          # get a mapping of conventions
>>> x = 1234567.8
>>> locale.format_string("%s%.*f", (conv['currency_symbol'],
...                     conv['frac_digits'], x), grouping=True)
'$1,234,567.80'
```

---

## 10.2. Templating

The `string` module includes a flexible `Template` class that allows users to customize formatting using simplified `$`-based placeholders.

```python
>>> from string import Template
>>> t = Template('${village}folk have $cause')
>>> t.substitute(village='Nottingham', cause='the plague')
'Nottinghamfolk have the plague'
```

`safe_substitute()` leaves placeholders intact if data is missing:

```python
>>> t = Template('Return the $item to $owner.')
>>> d = dict(item='unbound book')
>>> t.safe_substitute(d)
'Return the unbound book to $owner.'
```

---

## 10.3. Working with Binary Data Record Layouts

The `struct` module provides `pack()` and `unpack()` functions for working with variable-length binary data formats.

Example: Processing header information from a ZIP file without using the `zipfile` module:

```python
import struct

with open('myfile.zip', 'rb') as f:
    data = f.read()

start = 0
for i in range(3):                      # show the first 3 file headers
    start += 14
    fields = struct.unpack('<IIIHH', data[start:start+16])
    crc32, comp_size, uncomp_size, filenamesize, extra_size = fields

    start += 16
    filename = data[start:start+filenamesize]
    start += filenamesize + extra_size
    print(filename, hex(crc32), comp_size, uncomp_size)
```

---

## 10.4. Multi-threading

Threading allows running multiple tasks concurrently, decoupling tasks that are not mutually dependent.

```python
import threading, zipfile

class AsyncZip(threading.Thread):
    def __init__(self, infile, outfile):
        threading.Thread.__init__(self)
        self.infile = infile
        self.outfile = outfile

    def run(self):
        f = zipfile.ZipFile(self.outfile, 'w', zipfile.ZIP_DEFLATED)
        f.write(self.infile)
        f.close()
        print('Finished background zip of:', self.infile)

background = AsyncZip('mydata.txt', 'myarchive.zip')
background.start()
print('The main program continues to run in foreground.')
background.join()    # Wait for the background task to finish
print('Main program waited until background was done.')
```

---

## 10.5. Logging

The `logging` module offers a full-featured logging system.

```python
import logging
logging.debug('Debugging information')
logging.info('Informational message')
logging.warning('Warning:config file %s not found', 'server.conf')
logging.error('Error occurred')
logging.critical('Critical error -- shutting down')
```

Output:

```text
WARNING:root:Warning:config file server.conf not found
ERROR:root:Error occurred
CRITICAL:root:Critical error -- shutting down
```

---

## 10.6. Weak References

The `weakref` module enables tracking objects without creating a reference that prevents garbage collection.

```python
>>> import weakref, gc
>>> class A:
...     def __init__(self, value):
...         self.value = value
...     def __repr__(self):
...         return str(self.value)
...
>>> a = A(10)                   # create a reference
>>> d = weakref.WeakValueDictionary()
>>> d['primary'] = a            # does not create a full reference
>>> d['primary']                # fetch object if still alive
10
>>> del a                       # remove the one real reference
>>> gc.collect()                # run garbage collection
0
>>> d['primary']                # entry was automatically removed
Traceback (most recent call last):
  ...
KeyError: 'primary'
```

---

## 10.7. Tools for Working with Lists

### 10.7.1. `array`

Provides a sequence object that behaves like a list but stores homogeneous data compactly (e.g., 2-byte unsigned binary integers).

```python
>>> from array import array
>>> a = array('H', [4000, 10, 700, 22222])
>>> sum(a)
26932
>>> a[1:3]
array('H', [10, 700])
```

### 10.7.2. `deque`

Double-ended queues optimized for fast appends and pops from both ends ($O(1)$ time complexity).

```python
>>> from collections import deque
>>> d = deque(["task1", "task2", "task3"])
>>> d.append("task4")
>>> print("Handling", d.popleft())
Handling task1
```

### 10.7.3. `bisect`

Provides functions for manipulating sorted lists.

```python
>>> import bisect
>>> scores = [100, 200, 400, 500]
>>> bisect.insort(scores, 300)
>>> scores
[100, 200, 300, 400, 500]
```

### 10.7.4. `heapq`

Provides functions for implementing heaps based on standard lists.

```python
>>> import heapq
>>> data = [1, 3, 5, 7, 9, 2, 4, 6, 8, 0]
>>> heapq.heapify(data)                      # rearrange list into a heap
>>> heapq.heappush(data, -5)                 # add a new item
>>> [heapq.heappop(data) for i in range(3)]  # fetch the three smallest items
[-5, 0, 1]
```

---

## 10.8. Decimal Floating Point Arithmetic

The `decimal` module offers fixed-point and floating-point arithmetic designed for exact representation (e.g., financial calculations).

```python
>>> from decimal import *
>>> round(Decimal('0.70') * Decimal('1.05'), 2)
Decimal('0.74')
>>> round(0.70 * 1.05, 2)            # binary float gives 0.73 due to representation limits
0.73
```

Decimal tracks exact precision and significance:

```python
>>> Decimal('1.00') % Decimal('.10')
Decimal('0.00')
>>> 1.00 % 0.10
0.09999999999999995

>>> sum([Decimal('0.1')]*10) == Decimal('1.0')
True
>>> sum([0.1]*10) == 1.0
False
```

# 11. Virtual Environments and Packages

This tutorial provides a concise summary of Chapter 12 from the official Python Documentation ("Virtual Environments and Packages"), covering how to create, activate, and manage isolated Python environments using `venv` and manage dependencies with `pip`.

---

## 11.1. Introduction & Motivation

Python applications often require specific versions of packages or third-party libraries. When multiple applications require conflicting versions of the same package (e.g., Application A needs version 1.0 while Application B needs version 2.0), installing packages globally creates conflicts.

**Virtual environments** solve this by creating self-contained directory trees that contain a Python installation for a particular version of Python, plus a number of additional packages.

---

## 11.2. Creating Virtual Environments

The module used to create and manage virtual environments is `venv`.

To create a virtual environment, run:

```bash
python -m venv tutorial-env
```

This creates the `tutorial-env` directory containing a copy/symlink of the Python interpreter and standard library, along with supporting files.

Common directory locations for virtual environments:

- `.venv` (a hidden folder in your project directory)
- `tutorial-env` or custom env names

---

## 11.3. Activating Virtual Environments

Before using the virtual environment, you must **activate** it.

- **On Windows (Command Prompt)**:
    ```cmd
    tutorial-env\Scripts\activate.bat
    ```
- **On Windows (PowerShell)**:
    ```powershell
    tutorial-env\Scripts\Activate.ps1
    ```
- **On Unix or macOS (bash/zsh)**:
    ```bash
    source tutorial-env/bin/activate
    ```

Once activated, your command prompt displays the environment name in parentheses:

```bash
(tutorial-env) $ python
Python 3.12.0 (main, Oct  2 2023, 12:00:00)
>>>
```

To exit and return to system Python, run:

```bash
deactivate
```

---

## 11.4. Managing Packages with `pip`

You can install, upgrade, and remove packages using the program named **`pip`**.

### 11.4.1. Installing Packages

- **Install the latest version** of a package:
    ```bash
    pip install novas
    ```
- **Install a specific version**:
    ```bash
    pip install requests==2.6.0
    ```
- **Install with version specifiers**:
    ```bash
    pip install "requests>=2.0.0,<3.0.0"
    ```
- **Upgrade a package** to the latest version:
    ```bash
    pip install --upgrade requests
    ```

---

### 11.4.2. Displaying Installed Packages

- **`pip show`**: Displays information about a specific package.
    ```bash
    pip show requests
    ```
- **`pip list`**: Displays all installed packages in the current environment.
    ```bash
    pip list
    ```

---

### 11.4.3. Reproducing Environments with Requirements Files

`pip freeze` generates a list of installed packages in a format that can be saved to a file (conventionally named `requirements.txt`).

1. **Export installed packages**:

    ```bash
    pip freeze > requirements.txt
    ```

2. **Inspect `requirements.txt`**:

    ```text
    novas==3.1.1.3
    numpy==1.9.2
    requests==2.7.0
    ```

3. **Replicate environment in another system/venv**:
    ```bash
    pip install -r requirements.txt
    ```

# 12. Floating-Point Arithmetic: Issues and Limitations

This tutorial provides a concise summary of Chapter 15 (and Appendix) from the official Python Documentation ("Floating-Point Arithmetic: Issues and Limitations"), covering base-2 representations, representation error, precision issues, and practical mitigation techniques.

---

## 12.1. Representation Error

Floating-point numbers are represented in computer hardware as base-2 (binary) fractions. Most decimal fractions cannot be represented exactly as binary fractions.

For example, the decimal fraction `0.1`:
$$\frac{1}{10} = \frac{1}{2^4} + \frac{1}{2^5} + \frac{0}{2^6} + \frac{0}{2^7} + \frac{1}{2^8} + \dots$$

Just as $\frac{1}{3}$ repeats endlessly in decimal ($0.3333\dots$), $\frac{1}{10}$ repeats endlessly in binary ($0.0001100110011\dots$).

Because hardware allocates fixed storage (IEEE 754 double precision: 53 bits of precision), the continuous fraction must be truncated, resulting in **representation error**.

```python
>>> 0.1
0.1
>>> format(0.1, '.17f')
'0.10000000000000001'
```

---

## 12.2. Practical Consequences of Imprecision

### 12.2.1. Unexpected Arithmetic Results

Because stored values are approximations, operations on them can produce unexpected outcomes:

```python
>>> 0.1 + 0.2
0.30000000000000004
>>> 0.1 + 0.1 + 0.1 == 0.3
False
```

### 12.2.2. Rounding and Comparison Issues

Due to binary representation error, `round()` behavior can sometimes seem surprising:

```python
>>> round(2.675, 2)
2.67
```

> **Why?** The floating-point value stored for `2.675` is actually slightly less than `2.675` in binary, so it rounds down to `2.67`.

---

## 12.3. Best Practices & Mitigations

### 12.3.1. Avoid Equality Comparison on Floats

Instead of testing whether two float values are strictly equal with `==`, check if they are close within an acceptable tolerance using `math.isclose()`:

```python
>>> import math
>>> math.isclose(0.1 + 0.2, 0.3)
True
```

### 12.3.2. Exact Decimal Arithmetic (`decimal`)

For applications requiring exact decimal representation (such as financial or accounting applications), use the built-in `decimal` module:

```python
>>> from decimal import Decimal
>>> Decimal('0.1') + Decimal('0.2')
Decimal('0.3')
>>> Decimal('0.1') + Decimal('0.1') + Decimal('0.1') == Decimal('0.3')
True
```

### 12.3.3. Exact Rational Arithmetic (`fractions`)

For exact arithmetic involving fractional ratios without losing precision, use the `fractions` module:

```python
>>> from fractions import Fraction
>>> Fraction(1, 10) + Fraction(2, 10)
Fraction(3, 10)
```

### 12.3.4. Floating-Point Summation (`math.fsum`)

To avoid loss of precision when adding multiple floats, use `math.fsum()`:

```python
>>> import math
>>> sum([0.1] * 10)
0.9999999999999999
>>> math.fsum([0.1] * 10)
1.0
```

---

## 12.4. Helper Methods (`float.hex` & `float.fromhex`)

To inspect or pass floating-point numbers without losing precision due to decimal conversion, use hexadecimal float strings:

```python
>>> x = 0.125
>>> x.hex()
'0x1.0000000000000p-3'

>>> float.fromhex('0x1.0000000000000p-3')
0.125
```
