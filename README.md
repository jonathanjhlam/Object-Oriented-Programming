# Object Oriented Programming
Unit Notes: Object Oriented Programming   

# **Lesson 1**        

**For examples, refer to the lesson 1 PPT: [https://docs.google.com/presentation/d/1wJ1SqLBaVSahdJUO41QRkyyLDmXpMWCROxV5TzdWsvU/edit?usp=sharing](url)**

**Class:**    
- Contains attributes       
  - Human class: race, gender, age, height, hair color, weight, etc.       
- Contains actions        
  - Human class: eat, drink, sleep, talk, regulate breathing and temperature (automatic), etc.       
- Everything is contained and are objects within the class (for the examples, they are objects of the human class)         

**Object:**  

**In Computer Science (CS):**       
- Object can be a variable, a data structure, a function, or a method; therefore, a location in memory having a value that can be referenced by an identifier
        
**In Object Oriented Programming (OOP):**          
- An object in OOP is an instance of a class where this object can be either a variable, a function, a data structure or a combination of such       

**The OOP Paradigm:**          

**Object Oriented Programming (OOP):**           

- Programming practice to design modular reusable software systems        
- OOP designs programs with creation of **Objects**        
- Focuses on the definition of data rather than the input → processing → output logic            
  - OOP vs procedure-oriented programming
- Goal: create an object that we can define and provide functionality to solve problems           

**Conceptual Differentiation:**           

**Procedure-Oriented:**              
- Human may require: calculations, logical evaluations, complete repetitive tasks, database        

**OOP:**           
- Human Object: What's their name? What's their address? What functions can this object have?               

NOTE: OOP focuses on how to manipulate the data of the object rather than the logic required to manipulate them             

**Objects:**             
- **Object**: A combination of data and functional code. This is because real-world objects have states and behavior.              
- **RECALL THAT AN OBJECT IS AN INSTANCE**
- **States:** The characteristic, measurable data of an object
- **Behavior:** The available functionality of the object (what can it do?)
- Object’s Data → attributes
- Object’s Code → methods          

**Dog Example:**          

**Attributes:**           
- Name, Color, Breed, isHungry, isThirsty

**Methods:**          
- bark(); eat(); sleep()             

If attributes are populated, then we have an instance; therefore an object.          

**Classes & Objects:**          
- **Class:** An abstract description of all objects that can be made from this set class where an object can be instantiated from
- A class contains **attributes**
- **Attributes:** An Object’s accessible **tools**
1. Fields: Variables that belong to an object or a class
  - Type 1: It belongs to the instance of the class
  - Type 2: It belongs to the class itself
2. Methods: Functions that the object or the object can call               

**OOP in Python 3:**         

**Keyword: Class**       
- A built-in keyword in Python 3 that allows to create our own classes.
- Example:

**The Most Basic Class**
```
class ClassName: # Notice that Class names are capitalized
	pass # An Empty Block
#end of ClassName

obj = ClassName()
print(obj)
```
**Create a Class:**
1. Define the name of the class with the keyword: **class**
2. In its code block (indentation) define its attributes
3. Then you can assign a variable with an instantiation of the class to interact with it
	- Make sure to use parentheses when calling the class name.

**Creating a Method for a Class:**
- Classes can have **methods**. In Python 3, we just declare them like a new function (it doesn’t always need to return).

**The init method & self parameter**
- def __init__(self): → The __init__ method (double underscores)
- The **initialization** method is executed as soon as an object of the class is instantiated
- It helps us to do any initialization for the object’s attributes
- **self** parameter is used to denote that the method is applied and accessible for the object itself
- **self** will also treat its own attributes as local
- **Double Underscore:** These are key hidden features of Python that allow us to do some overwriting of Python features and hidden content      

**List is an Object in Python 3**
- L = [1,2,3,4]        
	- L is an instance of a <list class>; therefore, L is an object
- **Features:**
	- L[i] → indexing … L[i:j] → Slicing
	- functions → len(), min(), max()
	- operators → + and *
	- methods → L.append(), L.count(), L.extend(), L.sort(), L.reverse()

# **Lesson 2**     
**For examples, refer to the lesson 2 PPT: [https://docs.google.com/presentation/d/1BSBVPl27YKaFtiNa_6EPyUd5gnM5o60fKHdrmtp2jGk/edit?usp=sharing](url)**
	
**Encapsulation:**        
- Encapsulation → Information Hiding: Restricting the access to the classes/objects’ certain attributes and methods
- Encapsulation protects data
- Encapsulation restricts certain methods to be callable
- **Note:** In Python, this isn’t really possible: hence we use a special system. We hide attributes and methods by using a double underscore __ as a prefix.

**Python Example:**
```
class Student:
  def __init__(self,nameF, nameL, num):
    self.firstName = nameF
    self.lastName = nameL
    self.__studentNumber = num
  
  def __getStudentNumber(self):
    return self.__studentNumber

#end of Student
s1 = Student("Mr.", "Park", 10)
print(s1.__getStudentNumber()) # Will cause an error
print(s1.__studentNumber) # Will also cause an error
```
	
**Importance of Encapsulation:**
```
class Student:
  def __init__(self,nameF, nameL, num):
    self.firstName = nameF
    self.lastName = nameL
    self.__studentNumber = num

#end of Student

s1 = Student("Mr.", "Park", 10)
print(s1.firstName) # Returns/Outputs “Mr.”

s1.firstName = "Ms."
print(s1.firstName) # Returns/Outputs “Ms.”
```

**Common Practice:**
```
class Student:
  def __init__(self,nameF, nameL, num):
    self.__firstName = nameF
    self.__lastName = nameL
    self.__studentNumber = num
  
  def setFirstName(self, newName):
    self.__firstName = newName
    
  def getFirstName(self):
    return self.__firstName
```

**Overrides:**
- **Overloading:** Two methods in one class that have the same method name, but different parameters
- **Overriding:** Two methods with the same method name and parameters
	- One method is in the parent class 
	- One method is in the child class 
	- Overriding allows the child class to provide specific implementation for a method that exists in the parent class
	- You can also override built-in magic-methods **OR** Base-functions
- **NO OVERLOADING IN PYTHON 3**

**Polymorphism:**
- **Polymorphism:** A method that can be used across different classes and object that is dependent on the parameters
	- Poly → Many
	- Morphism → Forms
- Different Classes (non-inherited) can have the same named methods (Simple) → Polymorphism
- Within a set of inherited classes have the same methods

**Two Different Classes - Same Method**
```
class Bear:
    def sound(self):
        print("Groarrr")
 
class Dog:
    def sound(self):
        print("Woof woof!")
 
def makeSound(animalType):
    animalType.sound()

bearObj = Bear()
dogObj = Dog()
 
makeSound(bearObj)
makeSound(dogObj)

“”” In Conclusion:
We can give two different classes same methods; hence, Polymorphism.
“””
```

**Polymorphism and Inheritance:**
- Overloading is illegal in Python 3 but it is a type of Polymorphism
- **Inherited Classes modifying Inherited Methods** (Overriding) 
	- Polymorphism in Python 3

**Illegal Overloading:**
```
class Person:
    def __init__(self, name, age):
        self.__name = name
        self.__age = age

    def show(self):
        return self.__name

    def show(self, num):
        return "%s %d" % (self.__name, self.__age)
```

**Base Overrides:**
- Override and Polymorphism with Python can have:
	- Two different classes have a same _attributes_ and _methods_
	- A child of a parent have an _overrided_ method where the child would utilize the method differently
- These are the two fundamental concepts of overriding and polymorphism
- We can override a built-in methods/operators that we use as well for our own objects - _magic methods_
```
class Dog:
	def __init__(self,name):
		self.__name = name
	
	def __str__(self):
		return “Woof, I’m %s.” % self.__name

corgi = Dog(“Tobasco”)
print(corgi) → “Woof, I’m Tobasco.”
```
	
**Benefits of override built-in methods and operators:**
- Can start to complete mathematical operations on custom Objects
- Can start to compare equality between custom Objects
	- Can start to manipulate how the Object behaves when met with built-in methods and operators

**__repr__() base function:**
- return a string containing a printable representation of an object
- this function makes an attempt to return a string that would yield an object with the same value when passed to **eval()**
	- otherwise the representation is a string enclosed in angle brackets that contains the name of the type of the object together with additional information often including the name and address of the object
- A class can control what this function returns for its instances by defining a **repr ()** method
- When we try to make our custom objects printable, we actually need to **override** __repr__ and __str__
	- **__repr__** → Allows us to present a printable version of our object
	- **__str__** → Allows us to convert our object to a string

# **Lesson 3**
**For examples, refer to the lesson 3 PPT: [https://docs.google.com/presentation/d/1Y_By4kpgBXSZrrpH0JwcwBKgZf3GcTAweFDXrnMZx-U/edit?usp=sharing](url)**

**Inheritance:**
- **Inheritance:** When an object or class is based on another class; where its features are from a **parent class**
- **Types:**
	- **Single Inheritance:** A subclass inheriting the features of a single superclass/parent class
	- **Multiple Inheritance:** A subclass inheriting the features of a multiple parent classes
	- **Multilevel Inheritance:** A subclass is inheriting from another subclass… A → B → C
- **Inheritance** can have an **hierarchy** (branching like a tree) **and/or** be a **hybrid**
	- mixing the types of inheritances
- **What can we do?**
	- A child will receive all attributes and methods of the parent
	- A child can then enhance itself with new attributes and new methods
	- A child can **OVERRIDE** attributes and methods for their own liking/speciality
- **NOTE:**
	- If a child class inherits the parent class:
		- The child does not need a new __init__() method **UNLESS** it **requires new attributes**
		- The child does not need to reinstate the parent’s methods **UNLESS** you override them
	
**Single Inheritance**
```
class ParentClassName:
	“”” Define Parent Class “””
	.
	.
	.

class InheritanceClass(ParentClassName):
	“”” Define Inherited Class “””

	def __init__(self, param, param2):
		ParentClassName.__init__(self, param)
		self.param2 = param2
```
	
```
Parent Class
	
class Person:
  def __init__(self, name):
  	self.__name = name 
  
  def getName(self):
    return self.__name

Inherited Class
	
class Student(Person):
  def __init__(self, name, num):
    Person.__init__(self, name)
    self.__sNum = num
  
  def getStudentName(self):
    return("%s: %s" % (self.__sNum,self.getName()))
	
Execution
	
p = Person(“Mr. Park”)
s = Student(“Random Child”, “1234”)
print(p.getName()) # Output: “Mr. Park”
print(s.getStudentName(), “and” , s.getName()) # Output: “1234: Random Child and Random Child”
```

**super()**
- super() → is a built-in method for classes to refer their parent class
	- This prevents us from doing ParentClass.method(self)
	- The self with self gets confusing

**Example with super()**
```
Parent Class
	
class Person:
  def __init__(self, name):
  	self.__name = name 
  
  def getName(self):
    return self.__name

Inherited Class

class Student(Person):
  def __init__(self, name, num):
    super().__init__(name)
    self.__sNum = num
  
  def getStudentName(self):
    return("%s: %s" % (self.__sNum,self.getName()))

Execution
	
p = Person(“Mr. Park”)
s = Student(“Random Child”, “1234”)
print(p.getName())
print(s.getStudentName(), “and” , s.getName())
```

**Inheritance Extended:**
- **Rule of Thumb:**
	- if you think you need multiple inheritance, you're probably wrong 
	- but if you know you need it, you're probably right
- **Types of Multiple Inheritances:**
	- **Multi-Generational**
		- Grandparent → Parent → Child
	- **Multi-Parent (Not limited to two)**
		- Parent A + Parent B = Child
	- **Mixture of 1 and 2**

**Polymorphism:**
- **Polymorphism:** A method that can be used across different classes and object that is dependent on the parameters
	- Poly → Many
	- Morphism → Forms
- Different Classes (non-inherited) can have the same named methods (Simple) → Polymorphism
- Within a set of inherited classes have the same methods

**Polymorphism and Inheritance**
- **Overloading** → Illegal in Python 3, but it is a type of Polymorphism
- **Inherited Classes modifying Inherited Methods** (Overriding) → Polymorphism in Python 3
	
**Polymorphism in Inherited Classes**
```
class Parent:
	def method(self):
		pass

class Child(Parent):
	def method(self):
		# something different
		# Polymorphed to something else…
		# Same method name!
		pass
```
	
# **Lesson 4**














