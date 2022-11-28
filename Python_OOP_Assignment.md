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
A) 

--- 

Q16. What is the most popular form of operator overloading?

Q17. What are the two most important concepts to grasp in order to comprehend Python OOP code?

Q18. Describe three applications for exception processing.

Q19. What happens if you don't do something extra to treat an exception?

Q20. What are your options for recovering from an exception in your script?

Q21. Describe two methods for triggering exceptions in your script.

Q22. Identify two methods for specifying actions to be executed at termination time, regardless of  
whether or not an exception exists.

Q23. What is the purpose of the try statement?

Q24. What are the two most popular try statement variations?

Q25. What is the purpose of the raise statement?

Q26. What does the assert statement do, and what other statement is it like?

Q27. What is the purpose of the with/as argument, and what other statement is it like?

Q28. What are *args, **kwargs?

Q29. How can I pass optional or keyword parameters from one function to another?

Q30. What are Lambda Functions?

Q31. Explain Inheritance in Python with an example?

Q32. Suppose class C inherits from classes A and B as class C(A,B).Classes A and B both have their own versions of method func(). If we call func() from an object of 
class C, which version gets invoked?

Q33. Which methods/functions do we use to determine the type of instance and inheritance?

Q34.Explain the use of the 'nonlocal' keyword in Python.

Q35. What is the global keyword?
