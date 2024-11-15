## Introspection

`help(thing)`: prints a detailed help page for the type of thing. Thing can be an object, a library, etc.

`dir(thing)`: prints a list of the functions of thing


## main

```
if __name__ == '__main__':
```

Use `from scriptname import *` in interactive shell to import the functions and variables from `scriptname.py` without running the main function.

## Hashbang

Add `#!/usr/bin/env python3` at the beginning of a file and make it executeable to run it from a Unix shell.


## Dictionaries  
#### Making a dictionary 

`data = {}`  
OR  
`data = dict()`  

#### Initially adding values 

`data = {'a':1,'b':2,'c':3}`  
OR  
`data = dict(a=1, b=2, c=3)`  

#### Inserting/Updating value 

`data['a']=1  # updates if 'a' exists, else adds 'a'`  
OR  
`data.update({'a':1})`  
OR  
`data.update(dict(a=1))`  
OR  
`data.update(a=1)`  

#### Merging 2 dictionaries 

`data.update(data2)  # Where data2 is also a dict.`  

#### Deleting items in dictionary 

`del data[key] #Remove specific element in a dictionary`  
`data.pop(key) #Removes the key & returns the value`  
`data.clear() #Clear entire dictionary`  

## Function timer decorator
```python
import time

# Define a decorator to time function execution
def timing_decorator(func):
    def wrapper(*args, **kwargs):
        start_time = time.time()  # Record the start time
        result = func(*args, **kwargs)  # Call the function
        end_time = time.time()  # Record the end time
        elapsed_time = end_time - start_time  # Calculate elapsed time
        # Convert elapsed time to minutes and seconds
        minutes = int(elapsed_time // 60)  # Whole minutes
        seconds = elapsed_time % 60  # Remaining seconds
        print(f"{func.__name__} took {minutes}m{seconds:.1f}s to execute.")
        return result  # Return the result of the function
    return wrapper

# Example function to be timed
@timing_decorator
def my_function():
    time.sleep(125)  # Simulating a function that takes 125 seconds to execute

# Call the function
my_function()
```

## Python Debugger (pdb)
Add `breakpoint()` where you want to break the code (>Python 3.7)  
c: continue  
s: step  
unt 87: execute until line 87  
unt: execute until next line  
pp: pretty print value of an expression  
l: list code context  
b 87: set a breakpoint on line 87 in the current file  
  
[more](https://realpython.com/python-debugging-pdb/#essential-pdb-commands)  

## Things to add:
* proper way to do private functions in a class
* file read `with open("filename") as f:` 
* docstring format 
