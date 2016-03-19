# Item 1: Static factory methods  
## Purpose  
A static factory method in a class returns an instance of the class. Note that this means that a static factory methods do the same thing as constructors.  

## Advantages  
Static factory methods can have any name, unlike constructors that always have the same name as the class. Choosing a good name for a factory method can make the code clearer and cuts down on the need for additional documentation of the code.  

Static factory methods makes it possible to control the number of instances. Using a constructor to create an instance of a class will always create a new object but a factory method can be designed to return an existing object.  

A static factory method can return any subtype of their return type.  

## Disadvantages  
Using static factory methods implies that the constructor is private. This makes it impossible to subclass a class that uses static factory methods.  