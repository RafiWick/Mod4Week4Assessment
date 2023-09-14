# Week 4 Assessment

### Setup
* Fork and clone this repository
* Open your forked repo in Visual Studio.
* Complete the two exercises and the questions

## Exercise 1: Inheritance and Dependency Injection (8 points)

Open up `Program.cs` and run your program. It should run with no errors, if you get an error reach out to your instructor.

This exercise involves some refactoring and some new features.

**Step 1:** Currently there are two classess `Student` and `Teacher` that have a lot of repeated code between them. Create a new class `Person` that will be the base class. Then update `Student` and `Teacher` to be derived from `Person`. Include as much in your `Person` class as you can to keep your code DRY (Don't Repeat Yourself). 

**Testing Step 1:** Uncomment the code under "Step 1:" in the Main method. That code should now run without error.

**Step 2:** Implement a new class called `School` that uses dependency injection and takes in a list of people as a dependency. Implement a method called `ListBirthdays` in your school class that calls the `GetBirthday` method and prints to the console each student and teacher's birthday.

**Testing Step 2:** Uncomment the code under "Step 2:" in the Main method. That code should now run without error and output a bunch of names and birthdays.

Ungraded extra challenge: If you have time, improve the way the birthdays are output. Can you group them by month or by Student/Teacher?

### Exercise 2: Interfaces (4 points)
Open up `InterfacePractice.cs`. You should not need to run this file, you will just edit it.

**Step 1:** Take a look at the two classes `Car` and `Bicycle`. They both implement an interface called `InterfaceNameHere`. Replace all three uses of `InterfaceNameHere` with a fitting name for this interface.

**Step 2:** The interface has already been created for you on line 5. Fill in the details for any methods and/or properties that make sense based on the two classes implementing this interface.

## Questions (8 points)

Edit this file with your answers.

1. What are some of the benefits of using inheritance? (1 point)
    * Polymorphism - being able to use any child class to fill a Parent class type variable
	* Its another way to abstract code out of the child classes to make them more readable and consise
	* Code that would be repeated in multiple classes can be written once in a parent class
2. What might be some of the disadvantages of using inheritance? (1 point)
    * Creates dependencys and if there is too much inheritence it can become a web of dependence that can be dificult to update and debug
	* Creates extra classes that may be unnessesary 

3. How would you describe the difference between the base class and the derived class when working with inheritance? (1 point)
	* The base class is not dependent on the derived class and a change in the derived class does not affect the base class. Conversly the derived class is dependent on the base class and chenges to the base class will affect the derived class.

4.  What happens if you define the same method in the parent class and the child class? (1 point)
	* If you define the same method in both the parent and child classes, then, when an Instance of the child class has that method called the implementation in the child class will be ran because it will override the implementation in the parent class.

5. In your own words, how would you define an Interface? (1 point)
    * An interface is a contract that stipulates what the derived classes must have in terms of properties and behaviors allowing polymorphism between the derived classes.

6. Does a class implementing an interface need to implement all of the methods in that interface? Why or why not? (1 point)
    * Yes all members of the interface must be present in all classes that implement the interface. all members are nessasary because when the derivative object is stored in the interface type variable all of the properties must be able to be referenced and all of the methods must be able to be called.

7. Both Inheritance and Interfaces use the `:` symbol after a class name. If you're looking at a class, what's one thing that can help you determine if the class is implementing an interface of extending a base class? (1 point)
	* If the code has been written to the standards we have learned for c# than we can tell if the class is inheriting from another class or is based on an interface based on the name of the class being inherited. If the name starts with an 'I' and the second letter is the capitalized first letter of the name of the interface.

8. If asked in an interview, how would you describe the purpose of the IOC container in a .NET application? (1 point)
	* In .Net the IOC container plays a roll in dependency injection. In the .Net MCV applications that I have made the purpose of the IOC container is to hold the database context and then deliver that context to the controller through dependency injection.  


## Rubric

This assessment has a total of 20 points.  A score of 15 or higher is a pass.

As a reminder, this assessment is for students and instructors to determine if there are any areas that need additional reinforcement!
