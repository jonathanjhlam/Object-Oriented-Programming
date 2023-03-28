# Object-Oriented-Programming
Unit Notes: Object Oriented Programming   

**Lesson 1:**        

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

class ClassName: # Notice that Class names are capitalized
	pass # An Empty Block
#end of ClassName

obj = ClassName()
print(obj)

**Create a Class:**
1. Define the name of the class with the keyword: **class**
2. In its code block (indentation) define its attributes
3. Then you can assign a variable with an instantiation of the class to interact with it
	- Make sure to use parentheses when calling the class name.

**Creating a Method for a Class:**
- Classes can have **methods**. In Python 3, we just declare them like a new function (it doesn’t always need to return).

**The init method & self parameter**
- def __init__(self): → The __init__ method (double underscores)

