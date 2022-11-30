# Python OOP Assignment
---
### Q1. What is the purpose of Python's OOP? 
A)  It aims to implement real-world entities like inheritance, polymorphisms, encapsulation, etc. in the programming.OOP models real-world entities as software objects that have some data associated with them and can perform certain functions.

---

### Q2. Where does an inheritance search look for an attribute??? 
A)In Python, inheritance happens when an object is qualified, and involves searching an attribute definition tree (one or more namespaces). Every time you use an expression of the form object.attr where object is an instance or class object, Python searches the namespace tree at and above object, for the first attr it can find.

---

### Q3. How do you distinguish between a class object and an instance object??? 
A) A class is a template for creating objects in a program, whereas the object is an instance of a class.
Instance is an object that belongs to a class.

---

### Q4. What makes the first argument in a class’s method function special? 
A) This is the reason the first parameter of a function in class must be the object itself.  It is always a reference to the current instance of the class. By convention, this argument is always named self.

---

### Q5. What is the purpose of the init method? 
A) The __init__ method lets the class initialize the object's attributes and serves no other purpose. It is only used within classes.

---

### Q6. What is the process for creating a class instance?
A) class instance is nothing but an "__object__".  In the below example com_1 and com_2 are class instances.

```
class computer:
    def __init__(self, cpu, ram):
        self.cpu = cpu
        self.ram = ram

    def config(self):
        print("system config is ",self.cpu, self.ram)




com_1 = computer("i5", 16) #com_1 is class instance 
com_2 = computer("i7", 32) #com_2 is class instance



com_1.config()
com_2.config()


output : 
system config is  i5 16
system config is  i7 32

```
---

### Q7. What is the process for creating a class?
A) A class is created using keyword __"class"__ followed by __":"__ (colon).
The first method __init__() is a special method, which is called class constructor or initialization method that Python calls when you create a new instance of this class.

---

### Q8. How would you define the superclasses of a class?
A) A superclass is the class from which many subclasses can be created. The subclasses inherit the characteristics of a superclass. The superclass is also known as the parent class or base class.

---

### Q9. What is the relationship between classes and modules?
A) **Classes** in python are templates for creating objects. They contain variables and functions which define the class objects. **Modules** are python programs that can be imported into another python program. Importing a module enables the usage of the module's functions and variables into another program.

---

### Q10. How do you make instances and classes?
A) The class statement creates a new class definition. The name of the class immediately follows the keyword class followed by a colon as follows

```
class clock:
    def __init__(self,battery):
        self.battery = battery

```
To create instances of a class, you call the class using class name and pass in whatever arguments its __init__ method accepts.

```
comp1 = computer("i10",32) # comp1 - creating object instances
comp2 = computer("i10",32) # comp2 - creating object instances

```
--- 
### Q11. Where and how should be class attributes created?
A) A class attribute is shared by all instances of the class. To define a class attribute, you place it outside of the __init__() method. In the below example self.battery is **class attribute**.

```
class clock:
    def __init__(self,battery):
        self.battery = battery

```

---

### Q12. Where and how are instance attributes created?
A) **Instance attributes**, which are defined in the __init__() function, are class variables that allow us to define different values for each object of a class. In the below example **battery, frame** are instance attributes.

```
class clock:
    def __init__(self,battery, frame):
        self.battery = battery
        self.frame = frame

```
---

### Q13. What does the term "self" in a Python class mean?
A)The self parameter is a reference to the **current instance of the class**, and is used to access variables that belongs to the class.

---

### Q14. How does a Python class handle operator overloading?
A)Operator Overloading means giving extended meaning beyond their predefined operational meaning.Consider that we have two objects which are a physical representation of a class (user-defined data type) and we have to add two objects with binary ‘+’ operator it throws an error, because compiler don’t know how to add two objects. So we define a method for an operator and that process is called operator overloading. we will need to implement __add__() function in the class.

---

### Q15. When do you consider allowing operator overloading of your classes?
A) It allows for reusability; instead of developing numerous methods with minor differences, we can simply write one method and overload it. It also increases code clarity and reduces complexity.

--- 

### Q16. What is the most popular form of operator overloading?
A) A very popular and convenient form of operator overloading is the Addition (+) operator. the ‘+’ operator operates on two numbers and the same operator operates on two strings. It performs “Addition” on numbers whereas it performs “Concatenation” on strings.

---

### Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?
A)**Inheritance** and **polymorphism** are key ingredients for designing robust, flexible, and easy-to-maintain software.

---

### Q18. Describe three applications for exception processing.
A) In Python, exceptions can be handled using a **try statement**.
The critical operation which can raise an exception is placed inside the try clause. The code that handles the exceptions is written in the except clause. The main aim of the exception handling is to prevent potential failures and uncontrolled stops.

```
<!-- try block -->
try:
    print(2/0)
except:
    print("code done")

output : code done


<!-- Handling specific exception -->
try:
    print(2/0)
except ZeroDivisionError:
    print("ZeroDivisionError")

output : ZeroDivisionError

<!-- try finally exception -->
<!-- regardless of an exception occurs or not finally blocks gets executed -->

try:
    print(2/0)
except ZeroDivisionError:
    print("ZeroDivisionError")
finally:
    print("finally always prited")

```

---

### Q19. What happens if you don't do something extra to treat an exception?
A)  An exception object is created when a Python script raises an exception. If the script explicitly doesn't handle the exception, the program will be forced to terminate abruptly.

--- 

### Q20. What are your options for recovering from an exception in your script?
A) Use  try...except statement to handle exceptions gracefully.
   Use specific exceptions in the except block as much as possible.
   Use the except Exception statement to catch other exceptions.

---


### Q21. Describe two methods for triggering exceptions in your script.
A)For example, a Python program has a function X that calls function Y, which in turn calls function Z. If an exception exists in function Z but is not handled within Z, the exception passes to Y and then to X. Simply, it will have a domino effect. 

An unhandled exception displays an error message and the program suddenly crashes. To avoid such a scenario, there are two methods to handle Python exceptions:

Try – This method catches the exceptions raised by the program.
Raise – Triggers an exception manually using custom exceptions.

---

### Q22. Identify two methods for specifying actions to be executed at termination time, regardless of  whether or not an exception exists.
A) try catch finally are the methods, that are executed at termination time.  

---

### Q23. What is the purpose of the try statement?
A) The try block lets you test a block of code for errors.

---

### Q24. What are the two most popular try statement variations?
A) 

```
<!-- variation one -->
try:
   print(x)
except Exception:
   print("Something broke!")


<!-- variation two -->
try:
   print(int(x))
except NameError:
  print("The variable is undefined")   
except Exception as e:
   print(e)

```

--- 

### Q25. What is the purpose of the raise statement?
A) Python raise Keyword is used to raise exceptions or errors. The raise keyword raises an error and stops the control flow of the program. It is used to bring up the current exception in an exception handler so that it can be handled further up the call stack.

---


### Q26. What does the assert statement do, and what other statement is it like?
A) Assertions are simply boolean expressions that check if the conditions return true or not. If it is true, the program does nothing and moves to the next line of code. However, if it's false, the program stops and throws an error.

It is also a debugging tool as it halts the program as soon as an error occurs and displays it.

---

### Q27. What is the purpose of the with/as argument, and what other statement is it like?
A) The with statement is a replacement for commonly used **try/finally** error-handling statements. A common example of using the with statement is opening a file. To open and write to a file in Python, you can use the with statement as follows:

```
with open("example.txt", "w") as file:
    file.write("Hello World!")

```
The with statement automatically closes the file after you’ve completed writing it.

---

### Q28. What are *args, **kwargs?
A) We use *args and **kwargs as an argument when we are not sure about the number of arguments to pass in the functions.

---

### Q29. How can I pass optional or keyword parameters from one function to another?
A) To pass optional or keyword parameters from one function to another, collect the arguments using the * and ** specifiers in the function’s parameter list.

**kwargs = keyword parameters

```
def demo(**car):
   print("Car Name: "+car["name"])
   print("Car Model: "+car["model"])


demo(name = "TATA", model = "2022")

output : Car Name: TATA
         Car Model: 2022

```
collect the arguments using the * and ** in the function’s parameter list. you will get the **positional arguments as a tuple** and the **keyword arguments as a dictionary**.

In the below example 'x' and 'text' are optional parameters.

```
def func(x=3, text="Hello"):
    print(x)
    if text == "Hello":
        print("Text = Hello")
    else:
        print("Text is not Hello")

func()

output : 3
        Text = Hello

```

---

### Q30. What are Lambda Functions?
A) A lambda function is a small anonymous function. Python Lambda Functions are anonymous function means that the function is without a name. 
syntax : lambda arguments : expression

```
x = lambda a, b : a * b
print(x(5, 6))

output : 30

```
---

### Q31. Explain Inheritance in Python with an example?
A) Inheritance allows us to define a class that inherits all the methods and properties from another class.
**Parent class** is the class being inherited from, also called base class.
**Child class** is the class that inherits from another class, also called derived class.

In the below example **camera** is a parent class / super class and **voice_assitance** is a child class / sub class. voice_assiatance can inherit all the features of parent class. This is single level inheritance.

```
class camera: #parent class/super class
    def cam_1(self):
        print("your mobile has Cam_1 is 8MP")

    def cam_2(self):
        print("your mobile has Cam_2 is 16MP")


class voice_assistance(camera): #child class/sub class
    def hey_google(self):
        print("your mobile's voice assitance is 'Hey Google'")

    def alexa(self):
        print("your mobile's voice assistance is 'Alexa'")



mobile = voice_assistance()
mobile.alexa()
mobile.hey_google()
mobile.cam_1()
mobile.cam_2()

output : your mobile's voice assistance is 'Alexa'
         your mobile's voice assitance is 'Hey Google'
         your mobile has Cam_1 is 8MP
         your mobile has Cam_2 is 16MP

```
---

### Q32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of class C, which version gets invoked?
A) class "A" gets invoked.

```
class ParentA:
    def show(self):
        print("Inside Parent A")

class ParentB:
    def show(self):
        print("Inside Parent B")

class C(ParentB,ParentA):
    def display(self):
        print("display c")

objC = C()
objC.show()

output : Inside Parent A

```
---

### Q33. Which methods/functions do we use to determine the type of instance and inheritance?
A) Use **isinstance()** to check an instance’s type: isinstance(obj, int) will be True only if obj.__class__ is int or some class derived from int.
Use **issubclass()** to check class inheritance: issubclass(bool, int) is True since bool is a subclass of int. However, issubclass(float, int) is False since float is not a subclass of int.

---

### Q34.Explain the use of the 'nonlocal' keyword in Python.
A) The nonlocal keyword is used to **work with variables inside nested functions, where the variable should not belong to the inner function**. Use the keyword nonlocal to declare that the variable is not local.

---

### Q35. What is the global keyword?
A) In Python, the global keyword allows us to modify the variable outside of the current scope. It is used to create a global variable and make changes to the variable in a local context.

```
c = 1

def add(a):
    # global keyword
    global c

    c = c + a
    print("c value is:",c," ", "a value is: ", a)

add(2)

output : c value is: 3   a value is:  2

```

---