
# Printing
In Python, we ask a computer to print a message for us by writing print() and putting the message inside the parentheses and enclosed in quotation marks. Below, we ask the computer to print the message **Hello, world!**.

```shell
print("Hello, World!")
```

# Arithmetics 
Python can be used to perform some arithmetic operations such as:
* Addition 
* Subtraction 
* Multiplication 
* Division

In general, Python follows the **PEDMAS rule**, when deciding the order of operations.

- Note:
Unlike when simply printing text, we do not use any quotation marks.

```shell
print(2+1) # 3
```
The output will be 3

```bash
print(9-4) # 5
```
The output will be 5

One can actually do a lot of calculations with Python!

Example
* Addition: `+`: 1 + 2 = 3
* Subtraction: `-`: 5-4 = 1
* Multiplication `*`: 2 * 4 = 8
* Division `/`: 6/3 = 2
* Exponent `**`: 3**2 = 9


# Comments. 
Comments are used to annotate what code is doing. 
- They help other people to understand your code, and they can also be helpful if you haven't looked at your own code in a while.

To indicate a that a line is a comment (and not Python code), you need to write a pound sign `(#)` as the very first character.
- Once Python sees the pound sign and recognizes that the line is a comment, it is completely ignored by the computer.

Example
```shell 
# Multiply 3 by 2
print(3 * 2) # The output will be 6
```

# Variables 
Imagine that you might want to save the result of a calculation you just did somewhere, to work with it later, for this you'll need to use **_variables_**

In general to work with a variable, you will need to begin by selecting the name you want to use.
- Variable names are ideally short and descriptive.
- They need to satisfy several requirements:
    * They cannot have spaces (e.g., test var) this is not allowed.
    * They can only include letters, numbers, and underscores (e.g., test_var! is not allowed).
    * They have to start with a letter or underscore (e.g., 1_var is not allowed).

Creating the variable you need to use = to assign the value that you want it to have.

Example
```shell
# Create a variable called test_var and give it a value of 4+5

test_var = 4+5

# Print the value of test_var
print(test_var)
```
The output is 9

## Manipulating Variables
One can change the value assigned to a variable by overriding the previous value.

In the example below, we change the value of `my_var` from 3 to 100

Example 
```shell
# Set the value of a new variable called my_var to 3
my_var = 3

# Print the value assigned to my_var 
print(my_var)

## The output is 3

# Change the value of the my_var (variable) to 100
my_var = 100

# Print the bew value assigned to my_var 
print(my_var)

## The output will be 100
```

Note:
- Whenever you define a variable in a code cell, all the code cells that follow also have access to the variables.

## Using Multiple Variables 
It's common for code to use multiple variables. 
- This is especially useful when we have to do a long calculation with multiple inputs.

Example
Calculating the number of seconds in four years. This calculation uses five inputs.

```shell
# Create variables 
num_years = 4

days_per_year = 365

hour_per_day = 24

min_per_hour = 60

sec_per_min = 60

# Calculate number of seconds in four years
total_secs = sec_per_min * min_per_hour * hour_per_day * days_per_year * num_years

print(total_secs)
```
The output is 126144000

Note 
- It is possible to do this calculation without variables as just 60 * 60 * 24 * 365 * 4, but it is much harder to check that the calculation without variables does not have some error, because it is not as readable. When we use variables (such as num_years, days_per_year, etc), we can better keep track of each part of the calculation and more easily check for and correct any mistakes.

Note 
- It is particularly useful to use variables when the values of the inputs can change. For instance, say we want to slightly improve our estimate by updating the value of the number of days in a year from 365 to 365.25, to account for leap years. Then we can change the value assigned to days_per_year without changing any of the other variables and redo the calculation.

Example
```shell
# Update to include leap years
days_per_year = 365.25

# Calculate number of seconds in four years
total_secs = secs_per_min * mins_per_hour * hours_per_day * days_per_year * num_years
print(total_secs)
```
The output is 126230400.0

Note: 
- You might have noticed the .0 added at the end of the number, which might look unnecessary. This is caused by the fact that in the second calculation, we used a number with a _fractional part (365.25)_, whereas the first calculation multiplied just numbers with no fractional part. 




