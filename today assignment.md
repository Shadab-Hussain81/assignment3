Q1. why are functions advantages to have in your program ?

Ans: Code Reusability and Libraries: Functions can be reused across different programs and projects. By creating reusable functions, you can build libraries or modules that provide useful functionality, which can be utilized in various contexts. This reusability saves time and effort by leveraging existing code and promotes code sharing among developers.


Q2.when does the code in a function run:when it specified or when is called?

Ans: The code within a function in most programming languages is executed when the function is called. When you define a function, you are essentially creating a reusable block of code that will be executed when the function is invoked or called in your program.




```python
#example
def say_hello():
    print("hello,world!")  #function defined ,but code inside not executed
    
say_hello()  # call the function which executes the code inside  
    
```

    hello,world!
    

 Q3.what statement create a functions

Ans:  Function Declaration/Definition: This statement defines the name and parameters of the function. It establishes the function's signature and serves as a blueprint for its behavior. In Python, the syntax for function declaration is as follows:


 def function_name(parameter1, parameter2, ...):
  #Function body
    # Code block executed when the function is called 


```python
# example
def add_numbers(a, b):
    return a + b
```

Que4.what is the difference between function and function call?

Ans:function:A function is a block of reusable code that performs a specific task or a set of instructions. It is designed to receive input, perform computations or operations on that input, and then return a result. Functions are used to modularize code, improve code reusability, and enhance the overall structure and readability of a program. They allow you to break down complex tasks into smaller, more manageable parts.
 

 functions call:On the other hand, a function call (also known as invoking or executing a function) is the action of actually running or using a function in your code. It is the statement that initiates the execution of the function and provides any necessary arguments or parameters that the function expects. When a function is called, the program temporarily transfers control to that function, executes its statements, and then returns back to the point where the function call was made.

 
 A function is a defined piece of code that encapsulates a specific task or functionality.
 A function call is the act of using that function by invoking or executing it in your program.
 Here's a simple example in Python to illustrate the difference:
 


```python
#Function definition
def greet(name):
    print("Hello, " + name + "!")
 
 #Function call
greet("Alice")
 #In this example, the function greet is defined with a single parameter name, which is used to print a greeting message. The function call greet("Alice") actually executes the greet function with the argument "Alice," resulting in the output "Hello, Alice!"

```

    Hello, Alice!
    

 Q5.how many global scopes are there in a python program?how many locl scopes?

In a Python program, there is typically one global scope, which is the outermost scope of the program. The global scope includes all the global variables and functions defined in the program.
 
 On the other hand, local scopes are created whenever a function is called or when entering a block of code such as a loop or conditional statement. Each function call or block of code creates a new local scope. Local scopes are used to store variables that are specific to that particular function or block of code.


Q6.what happen to variable in a local scope?when the functions call returns?

Ans:In a local scope, variables are created and stored in memory when the function is called. These variables are accessible only within the scope of that function. When the function call returns, the local variables are typically destroyed, and the memory allocated to them is freed.
 The lifetime of local variables is limited to the duration of the function call. Once the function execution is complete, the local variables cease to exist, and any data they held is no longer accessible. Subsequent function calls will create new instances of the local variables, with their own separate memory allocations.


Q7. what is the concept of return value?is it possible to have a return value expression?

Ans: In programming, a return value is the data that a function sends back to the caller once it has finished executing. It represents the output or result of the function's computation. When a function is called, it performs certain operations and may produce a value that can be useful to the code that called it. The return value allows the function to communicate this value back to the calling code.
 
 A return value can be of any data type, such as numbers, strings, booleans, objects, or even more complex data structures. When a function has a return statement, it specifies the value to be returned to the caller. For example, consider a function that calculates the sum of two numbers:




def add_numbers(a, b):
    return a + b



```python
#expression
def square(x):
    return x * x

```

Q8. if a function does not have a return statement ,what is the return value of a call to that function?

Ans:If a function does not have a return statement, the return value of a call to that function is None. In Python, None is a special object that represents the absence of a value. When a function execution reaches the end without encountering a return statement, it implicitly returns None




```python
#Example
def my_function():
    print("Hello!")

result = my_function()
print(result)  # Output: None


```

    Hello!
    None
    

Q.9 how do you make a function variable refer to the global variable?


local_variable = 10

def my_function():
    global_variable  # Declare the variable as global
    global_variable = 20    # Modify the global variable

print(global_variable)  # Output: 10
my_function()
print(global_variable)  # Output: 20


Q10.what is the the data type of none?

Ans:In terms of data type, None has its own specific type, which is NoneType. It is the only instance of the NoneType class, and it is considered a singleton. This means that None is the only value that can be assigned to variables of type NoneType.




```python
x = None
print(type(x))  # Output: <class 'NoneType'>

```

    <class 'NoneType'>
    

Q11.what does the sentence import areallyourspetsnamederic do?

Ans:mport areallyourspetsnamederic" does not have a specific meaning or functionality in the English language. It appears to be a syntactically incorrect Python statement that attempts to import a module called "areallyourspetsnamederic." In Python, the import statement is used to bring modules or packages into a program, allowing access to their functions, classes, or variables. However, module names typically adhere to certain naming conventions, and "areallyourspetsnamederic" does not follow those conventions. Therefore, it would result in a syntax error if executed in a Python program.


 Q12.if you had a bacon()feature in a spam module what would you call it after importing spam?


Ans: If you had a bacon() feature in a spam module after importing it, you would simply call it using the module name followed by the function name. Assuming the module is named "spam", you would call the bacon() function as spam.bacon().






 

 Que13:what can you do to save a program from crashing if it encounters an error?

 Ans: 1.Exception handling: Implement exception handling mechanisms in your code to catch and handle exceptions gracefully. This involves using try-catch blocks to capture and handle specific types of errors. By catching exceptions, you can execute alternative code paths or display meaningful error messages instead of allowing the program to crash.
 
 2.Error checking and validation: Prioritize error checking and input validation throughout your code. Validate user input and data from external sources to ensure they meet the expected criteria. Check for potential issues such as invalid values, null references, or division by zero before performing operations. By proactively detecting and handling errors, you can prevent crashes caused by unexpected data.
 
 3.Logging: Implement a logging system that records important information, such as error messages and stack traces, when an error occurs. Logging can help you identify the root cause of a problem and provide valuable insights for troubleshooting. It also allows you to handle errors gracefully while providing useful feedback to users.
 
 4.Graceful degradation: When interacting with external systems or dependencies, design your code to gracefully handle failures or unavailability. Instead of crashing, your program can display appropriate error messages, provide fallback functionality, or retry the operation later. This approach ensures that your program remains operational despite encountering errors.
 
 5.Robust error recovery: Design your program to recover from errors and resume execution whenever possible. This could involve saving program state, persisting data, or implementing transactional mechanisms. By allowing your program to recover from errors, you can avoid crashes and maintain the integrity of your application.
 
 6.Thorough testing: Perform comprehensive testing to identify and fix errors before deploying your program. This includes unit testing, integration testing, and system testing. By detecting and resolving issues during the testing phase, you can significantly reduce the chances of crashes when the program is running in production.


Que14.what is the purpose of the try clause?what is the purpose of except clause?


 Ans: 1.Try Clause: The try clause is used to enclose a block of code that might raise an exception. It allows you to specify a section of code that you want to monitor for exceptions. The primary purpose of the try clause is to identify potential exceptions and handle them gracefully. If an exception occurs within the try block, the remaining statements in the block are skipped, and the flow of execution jumps to the corresponding except block (if present).
 
 2.Except Clause: The except clause follows the try clause and defines how to handle specific exceptions that can be raised within the try block. It allows you to specify one or more specific exceptions to catch and define the actions to be taken when those exceptions occur. The purpose of the except clause is to provide an alternative flow of control when an exception of a particular type is raised. Within the except block, you can include error handling code to respond to the exception, log an error message, or perform any other necessary actions.




```python

```
