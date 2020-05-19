# Engineering101
Guides to become the finest stalion of Wellcode.IO

TLDR;

#### 1. The use of HTTP request method according to its task

> POST, PUT/PATCH, DELETE
> This request is not cachable therefor it is safe to perform a database write operation and must using this method


> GET
> This request is cachable therefor it's not safe to perform a database write operation, only proper for read operation and its best to be cache if its possible



#### 2. Memoization in Rails
Memoization means the optimization technique where you memorize previously computed results, which will be used whenever the same result will be needed.
example:
```
def func
  @var ||= ...
end
```
Engineer tend to call the function instead of the variable inside the function.
It will leverage the readable of the code and the additional benefit of lazy initialization of the var itself



#### 3. Rule of use - IF/ELSE 
1. Only use `unless` in a oneliner if statement
2. oneliner `if/unless` statement must have characters's length less than half of screen view + NerdTree 


#### 4. View -> SLIM Template engine
> How to handle if element that have many attribute(dataset, etc.) which cause to a long oneline code?

Handling many attribute
```
.class-1.class-2[
  type=''
  action=''
]
```

Handling many dataset
```
.class-1.class-2[
  data={\
    id: '',\
    component: '',\
  }
]
```


#### 5. " & '
1. `"` should be used when there is string interpolation
2. `'` should be used when there just an ordinadry string without interpolation
