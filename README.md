# Engineering101
Guides to become the finest stalion of Wellcode.IO


### List of content
1. [The use of HTTP request method according to its task](#1-the-use-of-http-request-method-according-to-its-task)
2. [Memoization in Rails](#2-memoization-in-rails)
3. [Rule of use - IF/ELSE ](#3-rule-of-use---ifelse)
4. [View -> SLIM Template engine](#4-view---slim-template-engine)
5. [" & '](#5---)
6. [HTML class name convention](#6-html-class-name-convention)


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
1. `"` should be used when there are string interpolation
2. `'` should be used when there are just an ordinary string without interpolation


#### 6. HTML class name convention
1. Class name used particularly by JS and CSS should be differentiate to increase the ease of refactoring the code.
###### prefix class name with `js-` for class name that used by JS
```
.order__item--shipped.js-item
```
###### JS only allowed to call element with prefix `js-` in selecting element/s
```
document.querySelector('.js-item')
```
