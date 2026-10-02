# Conditions 
In programming, **conditions** are statements that are either:
```shell
1. True
2. False
```
There are many different ways to write conditions in Python, but some of the most common ways of writing conditions just compare two different values.
- For instance, one can check if 2 is greater than 3:

```bash 
print (2 > 3) # The output is False, given 2 is less than 3
```

Conditions can also be used to compare the values of variables.

```bash
var_one = 1
var_two = 2

print(var_one < 1) # The output is False, given var_one is equal to 1
print(var_two >= var_one) # The output is True because var_two contains the number 2, which is greater than the value of var_one, which is 1
```
For a list of common symbols one can use to construct conditions, check the chart below:

<img src="control-structures/control_structures.png" width="400">

**Important Note:** 
When you check whether two values are equal, make sure to use the `==` sign and not the `=` sign
* var_one == 1 checks if the value of var_one is 1
* var_one = 1 sets the value of var_one to 1


## Conditional Statements

Conditional statements use conditions to modify how your function runs. They check the value of a condition and if the condition evaluates to `True`, then a certain block of code is executed.
(_Otherwise, if the condition is `False`, then the code is not run._)

### `if` statements
The simplest type of conditional statement is an `if` statement.
- Example

To evaluate body temperature (in Celsius)

* Initially, message is set to `Normal temperature`

* Then, if `temp > 38` is True (e.g., the body temperature is greater than 38 degrees Celsius), then the message is updated to `Fever!`.

* Otherwise, if `temp > 38` is False, then the message is not updated

* Finally, message is returned by the function

```bash
def evaluate_temp(temp):
    # Set the initial message
    message = "Normal temperature."

    # Update value of message only if the temperature is > than 38
    if temp > 38:
        message = "Fever!"
    return message

# Call the function, where the temperature is `39 degrees Celsius`
print(evaluate_temp(39))
```

- The message is `Fever`, because the temperature is greater than 38 degrees Celsius (temp > 38 evaluates to `True`) in this case.

However, if the temperature is instead `37` - `evaluate_temp(37)`, since this is less than 38 degrees Celsius, the message would be updated to `Normal temperature`, given the condition will be evaluated to `False.`  

_Note that there are two levels of indentation_ 
* The first level of indentation is because we always need to indent the code block inside a function  
* The second level of indentation is because we also need to indent the code block belonging to the `if` statement.

_Note:_
Because the return statement is not indented under the `if` statement, it is always executed, whether temp > 38 is True or False. 


### `if...else` statements
One can use `else` statement to run code if a statement is `False.`
- The code under the `if` statement is run if the statement evaluates to `True,` and the code under the `else`is run if the statement is evaluated to `False.`  

```bash 
def evaluate_temp(temp):
    if temp > 38:
        message = "Fever!"
    else:
        message = "Normal temperature!"
    return message 
print(evaluate_temp(37))
```

When the function is called `temperature 37 is less than 38,` thus the `if` statement evaluates to `False,` and so the code under the `else` statement is executed and `Normal temperature` is returned.

- As with the previous function, we indent the code blocks after the `if` and `else` statements.


### `if...elif...else` statements
One can use the `elif` (_which is short for `else if`_) to check if multiple conditions might be true.

Example:
* First check if `temp > 38`. If this is true, then the message is set to `Fever!`

* As long as the message has not already been set, the function then checks if `temp > 35`. If this is true, then the message is set to `Normal temperature!`

* Then, if still no message has been set, the `else` statement ensures that the message is set to `Low temperature`, message is printed.

Think of `elif` as saying...`okay, that previous condition (e.g., temp > 38) was false, so let's check if this new condition (e.g., temp > 35) might be true!` 

```bash 
def evaluate_temp(temp):
    if temp > 38:
        message = "Fever!"
    elif temp >35:
        message = "Normal temperature!" # The output is `Normal temperature!`
    else:
        message = "Low temperature!"
    return message
print(evaluate_temp(36))
```
In the code base above, we run the code under the `elif` statement because `temp > 38` is `False`, and `temp > 35` is `True`. Once this code runs, the function skips the `else` statement and returns the message. 

