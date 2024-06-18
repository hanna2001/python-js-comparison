## Declaring Variables
### Python
```
    a = 10
```
### Javascript
```
    let a = 10
```

## Unpacking/ Destructing
### Python
```
    fruits=['afdv','bvfv','cda']
    a,b,c=fruits
    print(a,b,c)
    ------------------------------------------------------
    afdv bvfv cda
```
### Javascript
```
    [a, b] = [10, 20];
    [a, b, ...rest] = [10, 20, 30, 40, 50];
```

## Operations
### Python
```
    + 	Addition 	    
    - 	Subtraction 	
    * 	Multiplication 	
    / 	Division 	   
    % 	Modulus 	    
    ** 	Exponentiation 	
    // 	Floor division 	
```
### Javascript
```
    + 	Addition
    - 	Subtraction
    * 	Multiplication
    / 	Division
    % 	Modulus (Division Remainder)
    ** 	Exponentiation (ES2016)
    ++ 	Increment
    -- 	Decrement
```

## Ternary Operator
### Python
```
    true_value if condition else false_value
```
### Javascript
```
    isMember ? '$2.00' : '$10.00';
```

## Data Type
### Python
```
    Text Type       : 	str
    Numeric Types   : 	int, float, complex
    Sequence Types  : 	list, tuple, range
    Mapping Type    : 	dict
    Set Types       : 	set, frozenset
    Boolean Type    : 	bool
    Binary Types    : 	bytes, bytearray, memoryview
    None Type       : 	NoneType
```
### Javascript
```
    Null      : intentional absence of any object value
                object
                methods that interact with PROTOTYPE return null

    Undefined : absence of a value
                - automatically assigned when a variable is not initialized
                - return statement with no value (function)
                - accessing a nonexistent object property 
                    // obj={a:"11"} => obj.b 

    Number    : indicates for numeric values
                64 bit floating point
                NaN : result of an arithmetic operation cannot be expressed as a number : cannot be compared to any other value, even to itself
                - Number.MAX_VALUE (+/-)
                - Number.MIN_VALUE
                - Number.POSITIVE_INFINITY
                - Number.NEGATIVE_INFINITY

    BigInt    : BigInt is created by appending n to the end of an integer OR BigInt()
                not strictly equal but loosely equal

    String    : 16 bit
                \u{xxxxxx}
                immutable
    
    Boolean   : 1 byte / 8 bit

    Symbol    : unique and immutable primitive value

    Object    : when an object is created, a reference (or pointer) to that object's memory location can be assigned to an identifier
                mutable


```

## Pass by reference 
### Python
```
    List
    Dictionary

    ------------------------------------------
    def check(param):
      print(param)    
    
    a=[1,2,3]
    b=3
    d={"a":'1',"b":"2"}

    check(a)
    check(b)
    check(d)
```
### Javascript
```
    Objects
    Array
    Function
    -------------------------------------------
```

## Equality
### Python
```
    == : compares the value or equality of two objects
    is : checks whether two variables point to the same object in memory
    ------------------------------------------------------
    a=3
    b='3'
    c=3
    a_={'a':1}
    b_={'a':1}
    c_=a_

    print(a==b)       # False
    print(a==c)       # True
    print(a_==c_)     # True
    print(a_==b_)     # True
    print(a is b)     # False
    print(a is c)     # True  -> uses value 
    print(a_ is c_)   # True
    print(a_ is b_)   # False -> uses reference

```
### Javascript
```
    === : strict equality operator always considers operands of different types to be different
    ==  : convert and compare operands that are of different types
            const a = 100;
            const b = '100';

            console.log(a == b)
            ---------------------------
            true

            coercion
            either operand is a string  -> string
            either operand is a number  -> number
            either operand is a bool    -> number
            either operand is an object -> primitivd
            undefined/null              -> undefined/null

    Object.is() :   comparing objects
                    ----------------------------------
                        Object.is(25, 25); // true
                        Object.is("foo", "bar"); // false
                        const foo = { a: 1 };
                        const bar = { a: 1 };
                        const sameFoo = foo;
                        Object.is(foo, foo); // true
                        Object.is(foo, bar); // false
                        Object.is(foo, sameFoo); // true


``` 

## Check Type
### Python
```
    type(x)
```
### Javascript
```
    typeof(x)
```

## Function
### Python
```
    def keyword
```
### Javascript
```
    function keyword

    arrow functions and methods wont use keyword function

    arrow functions and constructor => anonymous function



    Can also have properties and methods

    Function expression and function decleration

        const square = function (n) {  # Function expression 
            return n * n;
        };

        function square(n) {           # Function decleration
            return n * n;
        }

        function name and variable the function is assigned to
    Function hoisting: 
        function can be called before decleration

    First-class Function : 
        functions are treated like any other variable
        a function can be - passed as an argument to other functions
                          - returned by another function (callback)
                          ------------------------------------------
                          function returnFunction(){
                            return=()=>{
                                console.log("hello");
                            }
                          }
    Function() constructor : 
        constructor can be slower than defining functions
        ----------------------------------------------------
        let args = 'a, b';
        let body = 'return a + b;';
        let sumFunction = new Function(args, body);
       
    
    --------------------------------------------------

    Accessing a function without () returns the function and not the function result
    --------------------------------------------------
    function toCelsius(fahrenheit) {
        return (5/9) * (fahrenheit-32);
    }

    let value = toCelsius; 

    toCelsius refers to the function object, and toCelsius() refers to the function result.
```

## Function Params
### Python
```
    arbitrary number of params:
        using * -> tuple
        def abc(*numbers)

    keyword arguements:
        def abc(number1,number2): -> Dictionary

        abc(number1:1,number2:2);
    Arbitrary Keyword Arguments:
        def abc(**numbers) -> Dictionary

        abc(number1:1,number2:2);

    Positional-Only Arguments: 
        def abc(numbers,/)

        abc(3)

    Keyword-Only Arguments:
        def abc(*,number1)

        abc(number1:1)

```
### Javascript
```
    defalt params:
        function abc(a=1,b)
    rest params:
        function abc(...numbers){}
        ---------------------------------
        abc(1,2,3)
        abc(1,2,3,4,5)
    destructing
        function abc(numbers1,number2){}
        --------------------
        abc([1,2])
```

# Type casting
## to Int
### Python
```
    c=int(a)
```
### Javascript
```
    Number("3.14")
    Number("") => 0
```

## to String
### Python
```
    c=str(a)
```
### Javascript
```
    String(3)
    String([1,2,3])
```


## Objects
### Python
```
    Dictionaries
```
### Javascript
```
    assigns many values in a variable

    defining:
        JavaScript Object Literal
            {firstName:"John", lastName:"Doe", age:50, eyeColor:"blue"}
        Using the new Keyword

    Objects are mutable

    can have methods

```

## Object property delete
### Python
```
    dictionary.clear()            -> clears the whole dictionary        
    dictionary.pop(key, default)  -> pops the key, and returns its value else default
    dictionary.popitem()          -> delete last entry
```
### Javascript
```
    delete obj.property_name
```


## Object display
### Python
```
    dict_name[key]
    dict_name.get(key,default)


    dict_name.keys()   -> return all keys as a list
    dict_name.values() -> return all values as a list
    dict_name.items()  -> return all key, value as a list of tuple [ (key1,val1), (key2,val2)..]
```
### Javascript
```
    Object.keys(obj)   -> return all keys as an array
    Object.values(obj)    -> return all value as an array
    Object.entries(obj)   -> Array of entries // [ [ key1 , val1 ] , [ key2 , val2] ]

```

## Index of an element 
### Python
```
    index()
    x = fruits.index("cherry")

    method only returns the first occurrence

    rindex(element,beg,end)  
        raises execption in case of failure
```
### Javascript
```
  - indexOf()       -> starts at a specified index and searches from left to right -> faster
    lastIndexOf()   -> finds the last index and rest same as indexOf()

  - findIndex()     -> uses a callback -> not on empty arrays
    find()
    findLastIndex()
    findLast()

   array=[1,2,3,5,6,2]
   array.indexOf(2)   // 1
   array.indexOf(2,2) // 6
   
   const isLarger=(ele)=>ele>4;
   array.findIndex(isLarger);    // 3 -> gets the index of first value that satisfies the condition
    returns -1 : failure
   array.find(isLarger);         // 5 -> gets the first value that satisfies the condition
    returns undefined : failure


```


## Sort Reverse in python
### Python
```
    list.sort(reverse=True,key)
    list=list[::-1]
    
```
### Javascript
```
   array.reverse()     -> reverses the original array , array is modified
   array.toReveresed() -> new array created

```

