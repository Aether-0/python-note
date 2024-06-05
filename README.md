---
### Python 3 Keywords and Example Usage

#### 1. **False**
```python
is_sunny = False
print(is_sunny)  # Output: False
```

#### 2. **None**
```python
result = None
print(result)  # Output: None
```

#### 3. **True**
```python
is_sunny = True
print(is_sunny)  # Output: True
```

#### 4. **and**
```python
x = 10
y = 5
if x > 5 and y < 10:
    print("Both conditions are true.")  # Output: Both conditions are true.
```

#### 5. **as**
```python
import datetime as dt
current_date = dt.date.today()
print(current_date)
```

#### 6. **assert**
```python
age = 25
assert age >= 18, "Age must be at least 18."
```

#### 7. **async** (Python 3.5+)
```python
import asyncio

async def main():
    print('Hello ...')
    await asyncio.sleep(1)
    print('... World!')

asyncio.run(main())
```

#### 8. **await** (Python 3.5+)
```python
import asyncio

async def say_hello():
    await asyncio.sleep(1)
    print("Hello")

asyncio.run(say_hello())
```

#### 9. **break**
```python
for i in range(5):
    if i == 3:
        break
    print(i)  # Output: 0 1 2
```

#### 10. **class**
```python
class MyClass:
    def __init__(self, name):
        self.name = name

obj = MyClass("Python")
print(obj.name)  # Output: Python
```

#### 11. **continue**
```python
for i in range(5):
    if i == 3:
        continue
    print(i)  # Output: 0 1 2 4
```

#### 12. **def**
```python
def greet():
    print("Hello, World!")

greet()
```

#### 13. **del**
```python
x = [1, 2, 3]
del x[1]
print(x)  # Output: [1, 3]
```

#### 14. **elif**
```python
x = 5
if x > 10:
    print("Greater than 10")
elif x > 5:
    print("Greater than 5")
else:
    print("5 or less")  # Output: 5 or less
```

#### 15. **else**
```python
x = 5
if x > 10:
    print("Greater than 10")
else:
    print("10 or less")  # Output: 10 or less
```

#### 16. **except**
```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")  # Output: Cannot divide by zero
```

#### 17. **finally**
```python
try:
    x = 1 / 0
except ZeroDivisionError:
    print("Cannot divide by zero")
finally:
    print("This is executed no matter what")  # Output: This is executed no matter what
```

#### 18. **for**
```python
for i in range(3):
    print(i)  # Output: 0 1 2
```

#### 19. **from**
```python
from math import sqrt
print(sqrt(16))  # Output: 4.0
```

#### 20. **global**
```python
x = 5
def set_global_x():
    global x
    x = 10

set_global_x()
print(x)  # Output: 10
```

#### 21. **if**
```python
x = 5
if x > 0:
    print("Positive number")  # Output: Positive number
```

#### 22. **import**
```python
import math
print(math.pi)  # Output: 3.141592653589793
```

#### 23. **in**
```python
fruits = ["apple", "banana", "cherry"]
if "banana" in fruits:
    print("Banana is in the list")  # Output: Banana is in the list
```

#### 24. **is**
```python
x = [1, 2, 3]
y = x
print(x is y)  # Output: True
```

#### 25. **lambda**
```python
add = lambda a, b: a + b
print(add(2, 3))  # Output: 5
```

#### 26. **nonlocal**
```python
def outer():
    x = "outer"
    def inner():
        nonlocal x
        x = "inner"
    inner()
    print(x)  # Output: inner

outer()
```

#### 27. **not**
```python
x = False
if not x:
    print("x is False")  # Output: x is False
```

#### 28. **or**
```python
x = 5
y = 10
if x > 0 or y > 0:
    print("At least one is positive")  # Output: At least one is positive
```

#### 29. **pass**
```python
def func():
    pass
```

#### 30. **raise**
```python
def check_positive(x):
    if x < 0:
        raise ValueError("x must be positive")
    return x

check_positive(-1)
```

#### 31. **return**
```python
def add(a, b):
    return a + b

print(add(2, 3))  # Output: 5
```

#### 32. **try**
```python
try:
    x = int("invalid")
except ValueError:
    print("Invalid value")  # Output: Invalid value
```

#### 33. **while**
```python
i = 0
while i < 3:
    print(i)  # Output: 0 1 2
    i += 1
```

#### 34. **with**
```python
with open("test.txt", "w") as file:
    file.write("Hello, World!")
```

#### 35. **yield**
```python
def generator():
    yield 1
    yield 2
    yield 3

for value in generator():
    print(value)  # Output: 1 2 3
```

---

### Python Built-in Functions and Example Usage

#### Type Conversion Functions

- **int()**
```python
num_str = "42"
num_int = int(num_str)
print(num_int)  # Output: 42
```

- **float()**
```python
num_str = "3.14"
num_float = float(num_str)
print(num_float)  # Output: 3.14
```

- **str()**
```python
num_int = 42
num_str = str(num_int)
print(num_str)  # Output: "42"
```

- **list()**
```python
num_tuple = (1, 2, 3)
num_list = list(num_tuple)
print(num_list)  # Output: [1, 2, 3]
```

- **tuple()**
```python
num_list = [1, 2, 3]
num_tuple = tuple(num_list)
print(num_tuple)  # Output: (1, 2, 3)
```

- **dict()**
```python
pairs = [("a", 1), ("b", 2), ("c", 3)]
num_dict = dict(pairs)
print(num_dict)  # Output: {'a': 1, 'b': 2, 'c': 3}
```

- **set()**
```python
num_list = [1, 2, 2, 3, 3, 3]
num_set = set(num_list)
print(num_set)  # Output: {1, 2, 3}
```

- **bool()**
```python
is_true = bool(1)
is_false = bool(0)
print(is_true)   # Output: True
print(is_false)  # Output: False
```

- **complex()**
```python
complex_num = complex(2, 3)
print(complex_num)  # Output: (2+3j)
```

- **chr()**
```python
char_code = chr(65)
print(char_code)  # Output: 'A'
```

- **ord()**
```python
char_code = ord('A')
print(char_code)  # Output: 65
```

#### Mathematical Functions

- **abs()**
```python
abs_value = abs(-5)
print(abs_value)  # Output: 5
```

- **round()**
```python
rounded_num = round(3.14159, 2)
print(rounded_num)  # Output: 3.14
```

- **pow()**
```python
result = pow(2, 3)
print(result)  # Output: 8
```

- **max()**
```python
max_num = max(1

, 5, 3)
print(max_num)  # Output: 5
```

- **min()**
```python
min_num = min(1, 5, 3)
print(min_num)  # Output: 1
```

- **sum()**
```python
numbers = [1, 2, 3, 4, 5]
sum_result = sum(numbers)
print(sum_result)  # Output: 15
```

- **divmod()**
```python
quotient, remainder = divmod(10, 3)
print(quotient, remainder)  # Output: 3 1
```

#### Iterable Functions

- **len()**
```python
str_len = len("Hello")
print(str_len)  # Output: 5
```

- **range()**
```python
numbers = list(range(1, 6))
print(numbers)  # Output: [1, 2, 3, 4, 5]
```

- **enumerate()**
```python
fruits = ['apple', 'banana', 'cherry']
for index, fruit in enumerate(fruits):
    print(index, fruit)
# Output:
# 0 apple
# 1 banana
# 2 cherry
```

- **zip()**
```python
names = ['John', 'Jane', 'Jim']
ages = [25, 30, 22]
for name, age in zip(names, ages):
    print(name, age)
# Output:
# John 25
# Jane 30
# Jim 22
```

- **sorted()**
```python
numbers = [3, 1, 4, 1, 5, 9, 2]
sorted_numbers = sorted(numbers)
print(sorted_numbers)  # Output: [1, 1, 2, 3, 4, 5, 9]
```

- **reversed()**
```python
numbers = [1, 2, 3, 4, 5]
reversed_numbers = list(reversed(numbers))
print(reversed_numbers)  # Output: [5, 4, 3, 2, 1]
```

- **all()**
```python
values = [True, False, True]
print(all(values))  # Output: False (since one value is False)
```

- **any()**
```python
values = [False, False, True]
print(any(values))  # Output: True (since one value is True)
```

#### Input/Output Functions

- **print()**
```python
print("Hello, World!")
```

- **input()**
```python
name = input("Enter your name: ")
print("Hello, " + name)
```

#### Object Type Functions

- **type()**
```python
x = 5
print(type(x))  # Output: <class 'int'>
```

- **id()**
```python
x = 5
print(id(x))  # Output: (some memory address)
```

- **isinstance()**
```python
x = 5
print(isinstance(x, int))  # Output: True
```

#### String Functions

- **str()**
```python
num_int = 42
num_str = str(num_int)
print(num_str)  # Output: "42"
```

- **len()**
```python
str_len = len("Hello")
print(str_len)  # Output: 5
```

- **ord()**
```python
char_code = ord('A')
print(char_code)  # Output: 65
```

- **chr()**
```python
char_code = chr(65)
print(char_code)  # Output: 'A'
```

- **capitalize()**
```python
text = "hello, world"
capitalized_text = text.capitalize()
print(capitalized_text)  # Output: "Hello, world"
```

- **upper()**
```python
text = "hello, world"
upper_case_text = text.upper()
print(upper_case_text)  # Output: "HELLO, WORLD"
```

- **lower()**
```python
text = "Hello, World"
lower_case_text = text.lower()
print(lower_case_text)  # Output: "hello, world"
```

- **strip()**
```python
text = "   hello, world   "
stripped_text = text.strip()
print(stripped_text)  # Output: "hello, world"
```

- **split()**
```python
text = "apple,banana,orange"
fruits = text.split(",")
print(fruits)  # Output: ['apple', 'banana', 'orange']
```

- **join()**
```python
fruits = ['apple', 'banana', 'orange']
text = ", ".join(fruits)
print(text)  # Output: "apple, banana, orange"
```

- **format()**
```python
name = "John"
age = 30
formatted_text = "My name is {} and I am {} years old.".format(name, age)
print(formatted_text)
# Output: "My name is John and I am 30 years old."
```

#### List Functions

- **list()**
```python
num_tuple = (1, 2, 3)
num_list = list(num_tuple)
print(num_list)  # Output: [1, 2, 3]
```

- **len()**
```python
str_len = len("Hello")
print(str_len)  # Output: 5
```

- **max()**
```python
max_num = max([1, 2, 3, 4, 5])
print(max_num)  # Output: 5
```

- **min()**
```python
min_num = min([1, 2, 3, 4, 5])
print(min_num)  # Output: 1
```

- **sum()**
```python
numbers = [1, 2, 3, 4, 5]
sum_result = sum(numbers)
print(sum_result)  # Output: 15
```

- **append()**
```python
numbers = [1, 2, 3]
numbers.append(4)
print(numbers)  # Output: [1, 2, 3, 4]
```

- **extend()**
```python
numbers = [1, 2, 3]
new_numbers = [4, 5]
numbers.extend(new_numbers)
print(numbers)  # Output: [1, 2, 3, 4, 5]
```

- **pop()**
```python
numbers = [1, 2, 3, 4, 5]
popped_item = numbers.pop()
print(popped_item)  # Output: 5
print(numbers)     # Output: [1, 2, 3, 4]
```

- **remove()**
```python
numbers = [1, 2, 3, 4, 5]
numbers.remove(3)
print(numbers)  # Output: [1, 2, 4, 5]
```

- **count()**
```python
numbers = [1, 2, 2, 3, 3, 3]
count_2 = numbers.count(2)
print(count_2)  # Output: 2
```

- **index()**
```python
numbers = [1, 2, 3, 4, 5]
index_3 = numbers.index(3)
print(index_3)  # Output: 2 (index of the first occurrence of 3)
```

- **sort()**
```python
numbers = [3, 1, 4, 1, 5, 9, 2]
numbers.sort()
print(numbers)  # Output: [1, 1, 2, 3, 4, 5, 9]
```

- **reverse()**
```python
numbers = [1, 2, 3, 4, 5]
numbers.reverse()
print(numbers)  # Output: [5, 4, 3, 2, 1]
```

#### Tuple Functions

- **tuple()**
```python
num_list = [1, 2, 3]
num_tuple = tuple(num_list)
print(num_tuple)  # Output: (1, 2, 3)
```

- **len()**
```python
str_len = len("Hello")
print(str_len)  # Output: 5
```

- **max()**
```python
max_num = max((1, 2, 3, 4, 5))
print(max_num)  # Output: 5
```

- **min()**
```python
min_num = min((1, 2, 3, 4, 5))
print(min_num)  # Output: 1
```

- **sum()**
```python
numbers = (1, 2, 3, 4, 5)
sum_result = sum(numbers)
print(sum_result)  # Output: 15
```

- **count()**
```python
numbers = (1, 2, 2, 3, 3, 3)
count_2 = numbers.count(2)
print(count_2)  # Output: 2
```

- **index()**
```python
numbers = (1, 2, 3, 4, 5)
index_3 = numbers.index(3)
print(index_3)  # Output: 2 (index of the first occurrence

 of 3)
```

#### Dictionary Functions

- **dict()**
```python
pairs = [("a", 1), ("b", 2), ("c", 3)]
num_dict = dict(pairs)
print(num_dict)  # Output: {'a': 1, 'b': 2, 'c': 3}
```

- **len()**
```python
str_len = len("Hello")
print(str_len)  # Output: 5
```

- **keys()**
```python
person = {'name': 'John', 'age': 30, 'city': 'New York'}
keys = person.keys()
print(keys)  # Output: dict_keys(['name', 'age', 'city'])
```

- **values()**
```python
person = {'name': 'John', 'age': 30, 'city': 'New York'}
values = person.values()
print(values)  # Output: dict_values(['John', 30, 'New York'])
```

- **items()**
```python
person = {'name': 'John', 'age': 30, 'city': 'New York'}
items = person.items()
print(items)
# Output: dict_items([('name', 'John'), ('age', 30), ('city', 'New York')])
```

- **get()**
```python
person = {'name': 'John', 'age': 30}
name = person.get('name')
print(name)  # Output: 'John'
```

- **pop()**
```python
person = {'name': 'John', 'age': 30}
age = person.pop('age')
print(age)  # Output: 30
```

- **popitem()**
```python
person = {'name': 'John', 'age': 30}
key, value = person.popitem()
print(key, value)  # Output: 'age' 30
```

- **update()**
```python
person = {'name': 'John', 'age': 30}
person.update({'city': 'New York'})
print(person)  # Output: {'name': 'John', 'age': 30, 'city': 'New York'}
```

- **clear()**
```python
person = {'name': 'John', 'age': 30}
person.clear()
print(person)  # Output: {}
```

#### Set Functions

- **set()**
```python
num_list = [1, 2, 2, 3, 3, 3]
num_set = set(num_list)
print(num_set)  # Output: {1, 2, 3}
```

- **len()**
```python
str_len = len("Hello")
print(str_len)  # Output: 5
```

- **add()**
```python
fruits = {'apple', 'banana', 'orange'}
fruits.add('mango')
print(fruits)  # Output: {'apple', 'banana', 'orange', 'mango'}
```

- **remove()**
```python
fruits = {'apple', 'banana', 'orange'}
fruits.remove('banana')
print(fruits)  # Output: {'apple', 'orange'}
```

- **discard()**
```python
fruits = {'apple', 'banana', 'orange'}
fruits.discard('banana')
print(fruits)  # Output: {'apple', 'orange'}
```

- **pop()**
```python
fruits = {'apple', 'banana', 'orange'}
removed_fruit = fruits.pop()
print(removed_fruit)  # Output: (any of the fruits in the set)
```

- **clear()**
```python
fruits = {'apple', 'banana', 'orange'}
fruits.clear()
print(fruits)  # Output: set()
```

- **union()**
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
union_set = set1.union(set2)
print(union_set)  # Output: {1, 2, 3, 4, 5}
```

- **intersection()**
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
intersection_set = set1.intersection(set2)
print(intersection_set)  # Output: {3}
```

- **difference()**
```python
set1 = {1, 2, 3}
set2 = {3, 4, 5}
difference_set = set1.difference(set2)
print(difference_set)  # Output: {1, 2}
```

- **issubset()**
```python
set1 = {1, 2, 3}
set2 = {1, 2, 3, 4, 5}
is_subset = set1.issubset(set2)
print(is_subset)  # Output: True
```

- **issuperset()**
```python
set1 = {1, 2, 3, 4, 5}
set2 = {1, 2, 3}
is_superset = set1.issuperset(set2)
print(is_superset)  # Output: True
```

#### Miscellaneous Functions

- **input()**
```python
name = input("Enter your name: ")
print("Hello, " + name)
```

- **abs()**
```python
abs_value = abs(-5)
print(abs_value)  # Output: 5
```

- **pow()**
```python
result = pow(2, 3)
print(result)  # Output: 8
```

- **open()**
```python
with open("myfile.txt", "w") as file:
    file.write("Hello, World!")
```

- **sorted()**
```python
numbers = [3, 1, 4, 1, 5, 9, 2]
sorted_numbers = sorted(numbers)
print(sorted_numbers)  # Output: [1, 1, 2, 3, 4, 5, 9]
```

- **range()**
```python
numbers = list(range(1, 6))
print(numbers)  # Output: [1, 2, 3, 4, 5]
```

- **id()**
```python
x = 5
print(id(x))  # Output: (some memory address)
```

- **format()**
```python
name = "John"
age = 30
formatted_text = "My name is {} and I am {} years old.".format(name, age)
print(formatted_text)
# Output: "My name is John and I am 30 years old."
```

- **help()**
```python
help(list)
# Output: (Help documentation for the list type)
```

---

### Operators

#### 1. Arithmetic Operators:
- `+`: Addition
- `-`: Subtraction
- `*`: Multiplication
- `/`: Division (float)
- `//`: Division (integer)
- `%`: Modulus (remainder)
- `**`: Exponentiation

#### 2. Assignment Operators:
- `=`: Assign value
- `+=`: Add and assign
- `-=`: Subtract and assign
- `*=`: Multiply and assign
- `/=`: Divide and assign
- `//=`: Divide and assign (integer)
- `%=`: Modulus and assign
- `**=`: Exponentiate and assign

#### 3. Comparison Operators:
- `==`: Equal to
- `!=`: Not equal to
- `<`: Less than
- `>`: Greater than
- `<=`: Less than or equal to
- `>=`: Greater than or equal to

#### 4. Logical Operators:
- `and`: Logical AND
- `or`: Logical OR
- `not`: Logical NOT

#### 5. Bitwise Operators:
- `&`: Bitwise AND
- `|`: Bitwise OR
- `^`: Bitwise XOR
- `~`: Bitwise NOT
- `<<`: Left shift
- `>>`: Right shift

#### 6. Identity Operators:
- `is`: Returns True if both variables are the same object
- `is not`: Returns True if both variables are not the same object

#### 7. Membership Operators:
- `in`: Returns True if a sequence with the specified value is present
- `not in`: Returns True if a sequence with the specified value is not present

#### 8. Ternary Operator (Conditional Expression):
- `expression1 if condition else expression2`: Returns `expression1` if `condition` is true; otherwise, it returns `expression2`

### Example Usage of Operators

#### 1. Arithmetic Operators:
```python
a = 5
b = 3

# Addition
result = a + b
print("Addition:", result)  # Output: 8

# Subtraction
result = a - b
print("Subtraction:", result)  # Output: 2

# Multiplication
result = a * b
print("Multiplication:", result)  # Output: 15

# Division (float)
result = a / b
print("Division (float):", result)  # Output: 1.6666666666666667

# Division (integer)
result = a // b
print("Division (integer):", result)  # Output: 1

# Modulus (remainder)
result = a % b
print("Modulus:", result)  # Output: 2

# Exponent

iation
result = a ** b
print("Exponentiation:", result)  # Output: 125
```

#### 2. Assignment Operators:
```python
x = 10

# Add and assign
x += 5
print("Add and assign:", x)  # Output: 15

# Subtract and assign
x -= 3
print("Subtract and assign:", x)  # Output: 12

# Multiply and assign
x *= 2
print("Multiply and assign:", x)  # Output: 24

# Divide and assign
x /= 4
print("Divide and assign:", x)  # Output: 6.0

# Divide and assign (integer)
x //= 2
print("Divide and assign (integer):", x)  # Output: 3.0

# Modulus and assign
x %= 2
print("Modulus and assign:", x)  # Output: 1.0

# Exponentiate and assign
x **= 3
print("Exponentiate and assign:", x)  # Output: 1.0
```

#### 3. Comparison Operators:
```python
a = 5
b = 10

# Equal to
print("Equal to:", a == b)  # Output: False

# Not equal to
print("Not equal to:", a != b)  # Output: True

# Less than
print("Less than:", a < b)  # Output: True

# Greater than
print("Greater than:", a > b)  # Output: False

# Less than or equal to
print("Less than or equal to:", a <= b)  # Output: True

# Greater than or equal to
print("Greater than or equal to:", a >= b)  # Output: False
```

#### 4. Logical Operators:
```python
x = True
y = False

# Logical AND
print("Logical AND:", x and y)  # Output: False

# Logical OR
print("Logical OR:", x or y)  # Output: True

# Logical NOT
print("Logical NOT (x):", not x)  # Output: False
print("Logical NOT (y):", not y)  # Output: True
```

#### 5. Bitwise Operators:
```python
a = 5   # Binary: 0101
b = 3   # Binary: 0011

# Bitwise AND
print("Bitwise AND:", a & b)  # Output: 1 (Binary: 0001)

# Bitwise OR
print("Bitwise OR:", a | b)  # Output: 7 (Binary: 0111)

# Bitwise XOR
print("Bitwise XOR:", a ^ b)  # Output: 6 (Binary: 0110)

# Bitwise NOT
print("Bitwise NOT (a):", ~a)  # Output: -6 (Binary: 11111111111111111111111111111010)

# Left shift
print("Left shift:", a << 1)  # Output: 10 (Binary: 1010)

# Right shift
print("Right shift:", a >> 1)  # Output: 2 (Binary: 0010)
```

#### 6. Identity Operators:
```python
a = [1, 2, 3]
b = a
c = [1, 2, 3]

# is
print("is (a and b):", a is b)  # Output: True
print("is (a and c):", a is c)  # Output: False

# is not
print("is not (a and b):", a is not b)  # Output: False
print("is not (a and c):", a is not c)  # Output: True
```

#### 7. Membership Operators:
```python
fruits = ["apple", "banana", "orange"]

# in
print("in:", "banana" in fruits)  # Output: True
print("in:", "grape" in fruits)  # Output: False

# not in
print("not in:", "banana" not in fruits)  # Output: False
print("not in:", "grape" not in fruits)  # Output: True
```

#### 8. Ternary Operator (Conditional Expression):
```python
age = 25

# Ternary operator
message = "You are an adult." if age >= 18 else "You are a minor."
print("Ternary Operator:", message)  # Output: "You are an adult."
```

---

### Data Types in Python

#### 1. Numeric Types:
- **int**: Integer data type (e.g., 1, -10, 100)
- **float**: Floating-point data type (e.g., 3.14, -0.5, 2.0)

#### 2. Sequence Types:
- **str**: String data type (e.g., "Hello", 'Python', "123")
- **list**: List data type (e.g., [1, 2, 3], ['apple', 'banana'])
- **tuple**: Tuple data type (e.g., (1, 2, 3), ('a', 'b', 'c'))

#### 3. Mapping Type:
- **dict**: Dictionary data type (e.g., {'key': 'value'}, {1: 'one', 2: 'two'})

#### 4. Set Types:
- **set**: Set data type (e.g., {1, 2, 3}, {'apple', 'banana'})

#### 5. Boolean Type:
- **bool**: Boolean data type (e.g., True, False)

#### 6. None Type:
- **None**: Represents the absence of a value (similar to null in other languages)

### Example Usage of Data Types

#### 1. Numeric Types:
```python
# Integer data type
age = 25
print("Age:", age)

# Floating-point data type
pi = 3.14159
print("Pi:", pi)
```

#### 2. Sequence Types:
```python
# String data type
name = "John Doe"
print("Name:", name)

# List data type
numbers = [1, 2, 3, 4, 5]
print("Numbers:", numbers)

# Tuple data type
coordinates = (10, 20)
print("Coordinates:", coordinates)
```

#### 3. Mapping Type:
```python
# Dictionary data type
person = {'name': 'John', 'age': 30, 'city': 'New York'}
print("Person:", person)
```

#### 4. Set Type:
```python
# Set data type
fruits = {'apple', 'banana', 'orange'}
print("Fruits:", fruits)
```

#### 5. Boolean Type:
```python
# Boolean data type
is_sunny = True
is_raining = False
print("Is it sunny?", is_sunny)
print("Is it raining?", is_raining)
```

#### 6. None Type:
```python
# None data type
result = None
print("Result:", result)
```
---
