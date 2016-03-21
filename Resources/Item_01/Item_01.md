# Item 1: Static factory methods  
## Purpose  
A static factory method in a class returns an instance of the class. Note that this means that a static factory methods do the same thing as constructors.  

## Example Code  
```  
public class Point {
    private int x = 0;
    private int y = 0;

    // constructor is private so it can not be used to create objects
    private Point(int x, int y) {
        this.x = x;
        this.y = y;
    }

    // static factory method that returns an object of this class
    public static Point newInstance(int x, int y) {
	return new Point(x, y);	
    }
}
```

## Advantages  
Static factory methods can have any name, unlike constructors that always have the same name as the class. Choosing a good name for a factory method can make the code clearer and cuts down on the need for additional documentation of the code.  

Static factory methods makes it possible to control the number of instances. Using a constructor to create an instance of a class will always create a new object but a factory method can be designed to return an existing object.  

A static factory method can return any subtype of their return type.  

## Disadvantages  
Using static factory methods implies that the constructor is private. This makes it impossible to subclass a class that uses static factory methods.  
