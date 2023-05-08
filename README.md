Download Link: https://assignmentchef.com/product/solved-solvedlab-7-designing-objects
<br>
1.1. Object-oriented languages like Java are designed to make it easy for programmers to implement software versions of real-world objects. An important skill to master is the ability to represent an object in code. Objects that we model are described using Java classes, so we have chosen to begin this lab by modeling a very simple, everyday object: a door.

Create a Door class that models a door object.

1.2. When modeling an object as a class, we also need to describe the properties or attributes an object possesses. An everyday object that we wish to model in software always has one or more properties that describe it. For instance a door object might have a name like â€œFrontâ€ or â€œSideâ€ to distinguish it from other doors. Another property that could describe a door is its state: â€œopenâ€ or â€œclosedâ€. Properties of objects are described in code by using nouns like â€œstateâ€ or â€œnameâ€ to create instance variables that hold values.

Add instance variables to your Door class body for the name of the door and its state. Experience has shown that we almost always want to limit the visibility of instance variables to code inside the same class, so make the access modifiers of state and name private. And because the state and name properties have values like â€œopenâ€ or â€œfrontâ€, let the instance variables you create be of type String.

1.3. Objects also have operations which can be invoked on the object and which may change the object in some way. For instance, the operations for a door object could be â€œopenâ€ and â€œcloseâ€. An operation on an object corresponds to a Java method and is described in code by using a verb like â€œopenâ€ or â€œcloseâ€. Invoking a method may change the value of an instance variable. For example, invoking close() would change the value of the state variable from â€œopenâ€ to â€œclosedâ€.

Declare methods for open and close. Because we usually want to allow free access to the methods a class contains, make the access modifier for each method public.

1.4. Now that we have a Door class, we would like to be able to create some Door objects. A constructor is a component of a class whose purpose is to create objects of the given class and to initialize the instance variables of the object. Java provides a default constructor for every class and the Door class is no exception. Unfortunately, the default constructor that Java provides initializes the state and name variables to null. This is not appropriate for this exercise.

Add a constructor for the Door class that takes two parameters: the name of the door and its initial state. Because we want to use the constructor outside of the class, make the access modifier for the constructor public.

1.5. It is often convenient to have accessor methods that operate on a single instance variable. Here is an accessor method for the name variable:

“`javapublic String getName(){return name;}“`

The word String in front of getName() indicates that the method returns a String when it is invoked. The body is simple and just returns the value of name.

Add this method to your class and write a similar accessor method for the instance variable state.

1.6. Many instance variables in a class will have corresponding mutator methods that allow you to change the value of the variable. Here is a mutator method for the name variable:

“`javapublic void setName(String newName){name = newName;}“`

The word void in front of setName() indicates that the method does not return a value when it is invoked. The body is simple and copies the value of the parameter newName to instance variable name.

Add this method to the class and write a similar mutator method for the instance variable state.

Use the following code to test your Door class:

“`java// A class to test the Door class.

public class DoorTester{

// Tests the methods of the Door class// @param args not used

public static void main(String[] args){Door frontDoor = new Door(“Front”, “open”);

System.out.println(“The front door is ” + frontDoor.getState());System.out.println(“Expected: open”);

Door backDoor = new Door(“Back”, “closed”);

System.out.println(“The back door is ” + backDoor.getState());System.out.println(“Expected: closed”);

// Use the mutator to change the state variable

backDoor.setState(“open”);

System.out.println(“The back door is ” + backDoor.getState());System.out.println(“Expected: open”);

// Use the mutator to change the name variable

backDoor.setName(“Kitchen”);

System.out.println(“The back door is called ” + backDoor.getName());System.out.println(“Expected: Kitchen”);

Door sideDoor = new Door(“Side”, “closed”);

System.out.println(“The side door is ” + sideDoor.getState());System.out.println(“Expected: closed”);

sideDoor.setState(“open”);

System.out.println(“The side door is ” + sideDoor.getState());System.out.println(“Expected: open”);}}“`

1.8. Consider the variable state in the class Door and the variable newState in the mutator for state. What kind of variable is state? What kind of variable is newState? When do these variables exist?

1.9. Consider the line below which was taken from the main method in 1.7 above.

“`javabackDoor.setState(“open”);“`

What is the implicit parameter that is passed by this method call? What is the explicit parameter?