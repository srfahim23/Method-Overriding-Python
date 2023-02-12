# Method-Overriding-Python

Method overriding is a powerful feature in object-oriented programming that allows you to redefine a method in a derived class. The method in the derived class is said to override the method in the base class. When you create an instance of the derived class and clall the overriddedn method, the version of the method in the derived class is executed, rather than the version in the base class.

In Python, method overriding is a way to customize the behaviour of a class based on its specific needs. For example, consider the following base class:

    class Shape:
        def area(self):
            pass

In this base class, the area method is defined, but does not have any implementation. If you want to create a derived class that represents a circle, you can override the area method any provide an implementation that calculates the area of a circle:

    class Circle(Shape):
        def __init__(self, radius):
            self.radius = radius

        def area(self):
            return 3.14 * self.radius * self.rarius


In this example, the Circle class inherits from the Shape class, and override the area method. The new implementation of the area method calculates the of a circle, based on its radius.

It's important to note that when you override a method, the new implementation must have the same method signature as the original method. This means that the number and type of arguments, as well a the return type, must be the same.

Another way to customize the behaviour of a class is to call the base class method from the derived class method. To do this, you can use the super function. The super functions allows you to call the base class method from the derived class method, and can be useful when you want to extent the behaviour of the base class method, rather than replace it.

For example, consider the following base class:

    class Shape:
        def area(self):
            print("Calculating area...")

In this base class, the area method prints a message indicating that the area is being calclated. If you want to create a derived class that represents a circle , and you also want to print a message indicating the type of shape, you can use the super function to call the base class method, and add your own message:

    class Circle(Shape):
        def __init__(self, radius):
            self.radius = radius

        def area(self):
            print("Calculating area of a circle..")
            super().area()
            return 3.14 * self.radius * self.radius
            
                