# Using the Python Interpreter

Source: [The official Python Tutorial: Using the Python Interpreter](https://docs.python.org/3/tutorial/interpreter.html)

## 1. Start Python

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

## 2. Two ways to run Python

### Interactive mode (REPL)

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

### Run a Python file

Save code in a file such as `hello.py`:

```python
print("Hello from a Python file!")
```

Run it from the terminal:

```bash
python hello.py
```

Use `python3 hello.py` or `py hello.py` if that is the command configured on your system.

## 3. Useful command-line options

### Run a short command with `-c`

Use `-c` to execute Python code directly from the terminal:

```bash
python -c "print(2 + 3)"
```

Quote the command because spaces and special characters may be interpreted by the shell.

### Run a module with `-m`

Use `-m` to run a module as a script:

```bash
python -m http.server
```

This example starts Python's simple local HTTP server in the current directory. Stop it with `Ctrl+C`.

### Run a script and then enter interactive mode with `-i`

```bash
python -i hello.py
```

Python runs the script and then opens the interactive interpreter, allowing you to inspect objects created by the script.

## 4. Command-line arguments

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

## 5. Exit the interpreter

To leave interactive mode:

- Type `quit()` and press Enter.
- Or use the end-of-file shortcut: `Ctrl+D` on Unix-like systems, or `Ctrl+Z` on Windows (then press Enter if required by the terminal).

## 7. Source-code encoding

Python source files use **UTF-8 by default**. This supports text from many languages in strings, comments, and identifiers.

If a file must use a different supported encoding, an encoding declaration can be placed at the beginning of the file, for example:

```python
# -*- coding: cp1252 -*-
```

For most modern projects, keep files saved as UTF-8 and ensure your editor uses UTF-8.

## Key takeaways

- Use the interactive interpreter to try small examples quickly.
- Use `.py` files for programs you want to save and run repeatedly.
- Know the basics of `-c`, `-m`, and `-i`.
- Use `sys.argv` when a script needs command-line arguments.
- Python source files default to UTF-8.

# An Informal Introduction to Python

This tutorial provides a concise summary of Chapter 3 from the official Python Documentation ("An Informal Introduction to Python"), covering basic data types, string/list manipulation, and introductory control flow.

---

## 1. Comments and Basics

Comments in Python start with `#` and continue to the end of the line.

```python
# this is the first comment
spam = 1 # and this is the second comment
text = "# This is not a comment because it's inside quotes."
```

---

## 2. Using Python as a Calculator

### Numbers

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

### Text (Strings)

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

### Lists

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

## 3. First Steps Towards Programming

Here is a practical example using a `while` loop to output the Fibonacci sequence:

```python
# Fibonacci series: the sum of two elements defines the next
a, b = 0, 1
while a < 10:
    print(a)
    a, b = b, a + b
```

### Core Concepts Introduced:

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

# More Control Flow Tools

This section provides a concise summary of Chapter 4 from the official Python Documentation ("More Control Flow Tools"), covering control structures, function definitions, standard coding styles, and key features introduced in recent Python releases like match/case.

---

## 1. `if` Statements

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

## 2. `for` Statements

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

## 3. The `range()` Function

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

## 4. `break`, `continue`, and `else` Clauses on Loops

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

## 5. The `pass` Statement

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

## 6. `match` Statements

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

### Pattern Matching with Shapes / Classes

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

## 7. Defining Functions

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

## 8. More on Function Arguments

### Default Argument Values

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

### Keyword Arguments

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

### Special Parameters (`/` and `*`)

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

### Arbitrary Argument Lists (`*args` and `**kwargs`)

- `*args` collects arbitrary positional arguments into a tuple.
- `**kwargs` collects arbitrary keyword arguments into a dictionary.

```python
def concat(*args, sep="/"):
    return sep.join(args)

>>> concat("earth", "mars", "venus")
'earth/mars/venus'
```

### Unpacking Argument Lists

Use `*` to unpack lists/tuples for positional arguments, and `**` to unpack dictionaries for keyword arguments.

```python
>>> args = [3, 6]
>>> list(range(*args))
[3, 4, 5]

>>> d = {"voltage": "four million", "state": "bleedin' demised", "action": "VOOM"}
>>> parrot(**d)
```

### Lambda Expressions

Small anonymous functions can be created with the `lambda` keyword:

```python
>>> pairs = [(1, 'one'), (2, 'two'), (3, 'three'), (4, 'four')]
>>> pairs.sort(key=lambda pair: pair[1])
>>> pairs
[(4, 'four'), (1, 'one'), (3, 'three'), (2, 'two')]
```

### Documentation Strings (Docstrings)

```python
def my_function():
    """Do nothing, but document it.

    No, really, it doesn't do anything.
    """
    pass

print(my_function.__doc__)
```

### Function Annotations

Annotations provide type hints for parameters and return values.

```python
def f(ham: str, eggs: str = 'eggs') -> str:
    print("Annotations:", f.__annotations__)
    return ham + ' and ' + eggs

f('spam')
```

---

## 9. Intermezzo: Coding Style (PEP 8)

Key guidelines from PEP 8 for clean Python code:

- Use **4-space indentation**, and no tabs.
- Wrap lines so that they don't exceed **79 characters**.
- Use blank lines to separate functions/classes and blocks of code.
- Place comments on their own line when possible.
- Use **docstrings** for functions, classes, and modules.
- Use `camelCase` for lower-level conventions only if needed, but prefer `snake_case` for functions and variable names, and `PascalCase` for class names.
- Use UTF-8 encoding for scripts.

# Data Structures

This section provides a concise summary of Chapter 5 from the official Python Documentation ("Data Structures"), covering list methods, list comprehensions, `del`, tuples, sets, dictionaries, and loop techniques.

---

## 1. More on Lists

### Common List Methods

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

### Using Lists as Stacks (LIFO)

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

### Using Lists as Queues (FIFO)

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

### List Comprehensions

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

### Nested List Comprehensions

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

## 2. The `del` Statement

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

## 3. Tuples and Sequences

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

## 4. Sets

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

## 5. Dictionaries

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

## 6. Looping Techniques

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

## 7. Conditions & Comparing Sequences

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
