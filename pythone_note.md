### Python 3 Keywords (35)

1. **False**: A boolean value representing "false" in Python.
2. **None**: A special value representing the absence of a value or "null".
3. **True**: A boolean value representing "true" in Python.
4. **and**: A logical operator used to combine two conditions, both of which must be true for the overall condition to be true.
5. **as**: Used in the context of importing modules to give them an alias (alternate name) for easier use.
6. **assert**: Used for debugging to check if a condition is true and raises an error if it's false.
7. **async**: Used to define a coroutine function, which allows for asynchronous programming (introduced in Python 3.5).
8. **await**: Used inside an asynchronous function to pause its execution until the awaited coroutine completes (introduced in Python 3.5).
9. **break**: Used to exit out of a loop prematurely.
10. **class**: Used to define a new class, which is a blueprint for creating objects.
11. **continue**: Used to skip the rest of the current loop iteration and move to the next one.
12. **def**: Used to define a new function.
13. **del**: Used to remove a variable or an element from a list or dictionary.
14. **elif**: Short for "else if," used in conditional statements to check additional conditions.
15. **else**: Used in conditional statements to define what happens when the previous conditions are not met.
16. **except**: Used in exception handling to specify a block of code that will be executed if an exception occurs.
17. **finally**: Used in exception handling to specify a block of code that will always be executed, whether an exception occurs or not.
18. **for**: Used to iterate over elements in a sequence (e.g., list, tuple, string) or other iterable objects.
19. **from**: Used in the context of importing to specify the module or package from which you want to import.
20. **global**: Used inside a function to indicate that a variable declared within the function should refer to the global scope.
21. **if**: Used to define a conditional statement that executes a block of code if a certain condition is true.
22. **import**: Used to import modules or specific objects from modules.
23. **in**: Used to check if a value is present in a sequence (e.g., list, tuple, string) or other iterable objects.
24. **is**: Used to check if two objects refer to the same memory location.
25. **lambda**: Used to create anonymous functions (functions without a name).
26. **nonlocal**: Used inside a nested function to indicate that a variable should refer to the nearest enclosing scope outside of the global scope.
27. **not**: A logical operator used to negate a condition.
28. **or**: A logical operator used to combine two conditions, at least one of which must be true for the overall condition to be true.
29. **pass**: A placeholder statement that does nothing. It's used when a statement is syntactically required but you don't want any action.
30. **raise**: Used to raise an exception manually.
31. **return**: Used to return a value from a function.
32. **try**: Used to enclose a block of code that might raise an exception. It is followed by `except` and/or `finally`.
33. **while**: Used to create a loop that executes as long as a certain condition is true.
34. **with**: Used to define a context for objects that support the context management protocol (e.g., files opened with `open()`).
35. **yield**: Used inside a generator function to produce a value to be iterated over.

### Example Usage of Keywords

#### False, True, and None
```python
# Boolean values
is_sunny = True
is_raining = False

# None - represents the absence of a value
result = None
```

#### and, or, and not
```python
x = 10
y = 5

# Logical AND - both conditions must be true
if x > 5 and y < 10:
    print("Both conditions are true.")

# Logical OR - at least one condition must be true
if x > 10 or y > 10:
    print("At least one condition is true.")

# Logical NOT - negates the condition
if not x == y:
    print("x is not equal to y.")
```

#### if, elif, and else
```python
age = 25

if age < 18:
    print("You are a minor.")
elif age >= 18 and age < 65:
    print("You are an adult.")
else:
    print("You are a senior citizen.")
```

#### while and break
```python
count = 0

while count < 5:
    print("Count:", count)
    count += 1
    if count == 3:
        break
```

#### for and continue
```python
numbers = [1, 2, 3, 4, 5]

for num in numbers:
    if num == 3:
        continue  # Skip the number 3
    print("Number:", num)
```

#### def and return
```python
def add_numbers(a, b):
    result = a + b
    return result

sum_result = add_numbers(10, 20)
print("Sum:", sum_result)
```

#### try, except, and finally
```python
try:
    num = int(input("Enter a number: "))
    result = 10 / num
    print("Result:", result)
except ValueError:
    print("Invalid input. Please enter a valid number.")
except ZeroDivisionError:
    print("Cannot divide by zero.")
finally:
    print("Execution completed.")
```

#### assert
```python
age = 15
assert age >= 18, "You must be 18 years or older to access this content."
print("Access granted.")
```

#### import and from
```python
# Importing entire module
import math
print("Square root of 16:", math.sqrt(16))

# Importing specific function from a module
from random import randint
random_num = randint(1, 100)
print("Random number:", random_num)
```

#### as
```python
# Giving a module an alias for shorter reference
import datetime as dt
current_date = dt.date.today()
print("Current date:", current_date)
```

#### lambda
```python
# Using lambda to create an anonymous function
add = lambda x, y: x + y
result = add(5, 3)
print("Result:", result)
```

#### global
```python
# Modifying a global variable from within a function
count = 0

def increment():
    global count
    count += 1

increment()
print("Count:", count)  # Output: 1
```

#### del
```python
# Deleting a variable
name = "Alice"
print("Hello,", name)

del name

# The variable 'name' no longer exists
print("Hello,", name)  # Raises NameError: name 'name' is not defined
```

#### yield
```python
# Using a generator function with yield
def countdown(n):
    while n > 0:
        yield n
        n -= 1

for num in countdown(5):
    print(num, end=' ')  # Output: 5 4 3 2 1
```

#### async and await (requires Python 3.5+)
```python
import asyncio

async def hello():
    await asyncio.sleep(1)
    print("Hello, asyncio!")

asyncio.run(hello())
```

#### nonlocal
```python
def outer_function():
    x = "outer"

    def inner_function():
        nonlocal x
        x = "inner"

    inner_function()
    print("x inside outer_function:", x)

outer_function()
```

#### pass
```python
# Using pass as a placeholder for empty code blocks
def some_function():
    # TODO: Implement this function later
    pass
```

#### in
```python
# Checking if an element exists in a list
fruits = ["apple", "banana", "orange"]

if "banana" in fruits:
    print("Yes, 'banana' is in the list.")
```

#### is
```python
# Comparing object identities
x = [1, 2, 3]
y = [1, 2, 3]

if x is y:
    print("x and y refer to the same object.")
else:
    print("x and y refer to different objects.")
```

#### try, except, else, and finally (together)
```python
try:
    num = int(input("Enter a number: "))
except ValueError:
    print("Invalid input. Please enter a valid number.")
else:
    result = 10 / num
    print("Result:", result)
finally:
    print("Execution completed.")
```

---

### Python Built-in Functions

#### 1. Type Conversion Functions:
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
```

python
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

#### 2. Mathematical Functions:
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
max_num = max(1, 5, 3)
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

#### 3. Iterable Functions:
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

#### 4. Input/Output Functions:
- **print()**: Already demonstrated in previous examples.
- **input()**
```python
name = input("Enter your name: ")
print("Hello, " + name)
```

#### 5. Object Type Functions:
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

#### 6. String Functions:
- **str()**: Already demonstrated in previous examples.
- **len()**: Already demonstrated in previous examples.
- **ord()**: Already demonstrated in previous examples.
- **chr()**: Already demonstrated in previous examples.
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

#### 7. List Functions:
- **list()**: Already demonstrated in previous examples.
- **len()**: Already demonstrated in previous examples.
- **max()**: Already demonstrated in previous examples.
- **min()**: Already demonstrated in previous examples.
- **sum()**: Already demonstrated in previous examples.
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

#### 8. Tuple Functions:
- **tuple()**

: Already demonstrated in previous examples.
- **len()**: Already demonstrated in previous examples.
- **max()**: Already demonstrated in previous examples.
- **min()**: Already demonstrated in previous examples.
- **sum()**: Already demonstrated in previous examples.
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
print(index_3)  # Output: 2 (index of the first occurrence of 3)
```

#### 9. Dictionary Functions:
- **dict()**: Already demonstrated in previous examples.
- **len()**: Already demonstrated in previous examples.
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

#### 10. Set Functions:
- **set()**: Already demonstrated in previous examples.
- **len()**: Already demonstrated in previous examples.
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

#### 11. Miscellaneous Functions:
- **input()**: Already demonstrated in previous examples.
- **abs()**: Already demonstrated in previous examples.
- **pow()**: Already demonstrated in previous examples.
- **open()**
```python
with open("myfile.txt", "w") as file:
    file.write("Hello, World!")
```

- **sorted()**: Already demonstrated in previous examples.
- **range()**: Already demonstrated in previous examples.
- **id()**: Already demonstrated in previous examples.
- **format()**: Already demonstrated in previous examples.
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

# Exponentiation
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
print("Divide and assign

 (integer):", x)  # Output: 3.0

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
