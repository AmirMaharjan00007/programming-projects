# 💻 Python Fundamentals

A beginner‑friendly, visual‑friendly guide to core Python concepts.  
Best for newcomers who want a **single page** that covers “everything you need to start”.

---

## ✅ 1. Variables and types

Variables store values under a name.

```python
name = "Alice"        # str  (text)
age = 15              # int  (whole number)
price = 9.99          # float (decimal)
is_active = True      # bool (True or False)
```

Check a type with `type()`:

```python
print(type(age))      # <class 'int'>
```

---

## ✅ 2. Basic math and operators

```python
x = 10
y = 3

print(x + y)          # 13
print(x - y)          # 7
print(x * y)          # 30
print(x / y)          # ≈3.33
print(x // y)         # 3 (integer division)
print(x % y)          # 1 (remainder)
print(x ** 2)         # 100 (x squared)
```

Comparison and logic:

```python
print(x > y)          # True
print(x == 10)        # True
print(x != 9)         # True

a = True
b = False
print(a and b)        # False
print(a or b)         # True
print(not a)          # False
```

---

## ✅ 3. Strings (text)

```python
msg = "Hello, Python"

print(len(msg))             # 13
print(msg.upper())          # HELLO, PYTHON
print(msg.lower())          # hello, python
print("Python" in msg)      # True
```

Modern string formatting:

```python
name = "Bob"
age = 12
print(f"My name is {name} and I am {age}.")
```

---

## ✅ 4. Lists

Ordered, changeable collection of items.

```python
colors = ["red", "green", "blue"]

print(colors)            # red
print(colors[-1])           # blue

colors.append("yellow")     # add item
print(len(colors))

for color in colors:
    print(color)
```

Slicing:

```python
numbers =[3][4][5][6]
print(numbers[1:4])         #[4][5][3]
print(numbers[:3])          #[3][4]
```

---

## ✅ 5. Tuples

Like lists, but **immutable** (can’t change after creation).

```python
point = (10, 20)
print(point)             # 10
print(point)             # 20[3]
```

This will fail:

```python
point = 15               # ❌ TypeError
```

---

## ✅ 6. Sets

Store **unique** items, no order.

```python
fruits = {"apple", "banana", "orange"}
fruits.add("apple")         # no effect; already there
print(len(fruits))          # 3
```

Set operations:

```python
a = {1, 2, 3}
b = {3, 4, 5}
print(a | b)                # union: {1, 2, 3, 4, 5}
print(a & b)                # intersection: {3}
```

---

## ✅ 7. Dictionaries

Map **keys** to **values**.

```python
person = {
    "name": "Alice",
    "age": 15,
    "city": "London",
}

print(person["name"])       # Alice
person["grade"] = "A"       # add entry

for key, value in person.items():
    print(key, ":", value)
```

Keys must be **immutable** (`str`, `int`, `tuple`).

---

## ✅ 8. If statements

```python
age = 16

if age >= 18:
    print("You are an adult")
elif age >= 13:
    print("You are a teenager")
else:
    print("You are a child")
```

Ternary (one‑line) `if`:

```python
status = "adult" if age >= 18 else "minor"
print(status)
```

---

## ✅ 9. Loops

`for` loop:

```python
names = ["Alice", "Bob", "Charlie"]

for name in names:
    print(f"Hello, {name}!")
```

`while` loop:

```python
count = 0
while count < 3:
    print("Iteration", count)
    count += 1
```

`break` and `continue`:

```python
for i in range(10):
    if i == 3:
        continue            # skip 3
    if i == 7:
        break               # stop at 7
    print(i)
```

---

## ✅ 10. Functions

Reusable code blocks.

```python
def greet(name):
    print(f"Hello, {name}!")

greet("Alice")
greet("Bob")
```

With `return`:

```python
def square(x):
    return x * x

print(square(4))            # 16
```

Default argument:

```python
def greet(name="User"):
    print(f"Hello, {name}!")

greet()                     # Hello, User!
greet("Alice")              # Hello, Alice!
```

---

## ✅ 11. Input / output and files

User input:

```python
name = input("Enter your name: ")
print(f"Hello, {name}")
```

Reading and writing files:

```python
# Write to a file
with open("hello.txt", "w") as f:
    f.write("Hello from Python!")

# Read from a file
with open("hello.txt", "r") as f:
    content = f.read()
    print(content)
```

The `with` statement automatically closes the file.

---

## ✅ 12. Error handling (`try`/`except`)

```python
try:
    num = int(input("Enter a number: "))
    print("You entered:", num)
except ValueError:
    print("That was not a valid number.")
```

Multiple exceptions:

```python
try:
    x = 10 / int(input("Divide by: "))
except ValueError:
    print("Please enter a valid integer.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
```

---

## ✅ 13. Modules and imports

Reuse Python’s built‑in modules:

```python
import random
print(random.randint(1, 10))

import math
print(math.sqrt(16))        # 4.0
```

Import specific items:

```python
from random import randint
print(randint(1, 5))
```

---

## ✅ 14. A quick intro to OOP

A **class** is a blueprint for objects.

```python
class Dog:
    def __init__(self, name):
        self.name = name

    def bark(self):
        print(f"{self.name} says woof!")

dog = Dog("Rex")
dog.bark()                  # Rex says woof!
```

Key ideas:
- `self` → the object instance  
- `__init__` → constructor (runs when you create `Dog(...)`)  

You don’t need deep OOP for basics, but this is a common next step.

---

## ✅ 15. Next‑step ideas (peek ahead)

Once you’re comfortable, you can add:

- List comprehensions:

  ```python
  squares = [x**2 for x in range(10)]
  ```

- `lambda` functions:

  ```python
  double = lambda x: x * 2
  print(double(4))          # 8
  ```

- Regular expressions (`import re`)  
- JSON handling (`json` module)  
- External packages (`pip install requests`)

But for your **beginner repo**, the material above is **all the core Python fundamentals** you need. You can add those extras later in a “Level Up: More Python” section.

---

## 📌 Quick fundamentals table

| Topic            | What it is                           | Example                                  |
|------------------|--------------------------------------|------------------------------------------|
| Variable         | Name for a value                    | `x = 10`                                 |
| List             | Ordered, changeable collection       | `my_list = [1, 2, 3]`                    |
| Dictionary       | Key → value mapping                 | `{"name": "Alice"}`                      |
| `if` / `else`    | Conditional logic                    | `if x > 5: ...`                          |
| `for` loop       | Loop over items                     | `for item in my_list:`                   |
| Function         | Reusable block                       | `def greet(name): ...`                   |
| `try` / `except` | Handle errors                       | `try: ... except ValueError:`            |
| File I/O         | Read/write files                    | `with open("file.txt", "w"):`            |

---
  
You’ll move from **Python beginner** to **confident beginner** faster than you think. 🚀

---

_Last Updated, May 2026
Amir Maharjan_
