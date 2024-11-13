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


## Things to add:
* proper way to do private functions in a class
* file read `with open("filename") as f:` 
* docstring format 
