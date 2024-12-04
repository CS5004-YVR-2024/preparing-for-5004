### Welcome to Java: A Transition Guide from Python
Welcome to your first steps in learning Java, especially if you're coming from a Python background! As you prepare for CS5004, which builds on what you learned in CS5001, we encourage you to enjoy the winter break in Vancouver. Take some time to explore the beauty of the season: try snowshoeing at Mount Seymour, visit the Vancouver Christmas Market at Jack Poole Plaza, or take a stroll through the enchanting lights at VanDusen Botanical Garden. There are also plenty of other winter activities around the city, like ice skating at Robson Square or exploring the festive decorations at Canada Place. Enjoying a break is important, but we also have a suggested exercise to help you get ready for the upcoming class.

To help you make this transition smoothly, here are some online resources and exercises to prepare for your journey in object-oriented design using Java. This guide aims to get you started with setting up your environment, writing basic programs, and understanding key concepts, drawing comparisons to what you've already learned in Python.

## Development Environment Setup
1. **Installing Java Development Kit (JDK)** - Guide to installing JDK, the necessary tool for Java development.  
    [Install Java JDK](https://docs.oracle.com/en/java/javase/17/install/overview-jdk-installation.html)

1. **Setting Up IntelliJ IDEA for Java** - A step-by-step guide to setting up IntelliJ IDEA, a powerful IDE for Java developers.  
    [Setting Up IntelliJ IDEA](https://www.jetbrains.com/idea/download/)



#### 2. "Hello, World!" in Java vs. Python

Let's start with a simple "Hello, World!" program. This is an easy way to understand the similarities and differences in syntax and structure between Python and Java.

**Python Version:**

```python
def main():
    print("Hello, World!")

main()
```

**Java Version:**

```java
public class Main {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

##### Challenge: Write Your Own "Hello, World!"

- Write and run a "Hello, World!" program in both Python and Java.
- Compare the structure of each program. What differences do you notice? Why might Java be more verbose?

#### 3. All Things Are Objects in Java

In Java, everything is centered around objects and classes. Unlike Python, where you can write simple scripts without defining classes, Java requires you to start every program with a class definition. This is because Java is a fully object-oriented language, and it encourages an object-oriented approach from the very beginning.

To execute a Java program, you need to define a `main` method that serves as the entry point. The `main` method must be `static` because it needs to be called by the Java runtime without creating an instance of the class first. This requirement helps enforce Java's object-oriented structure, ensuring that even the starting point of the program adheres to its class-based framework. This may not make sense to you right now but it will as we dive into this programming language. 

In the Python version of "Hello, World!", we artificially added a function called `main()` and then called it to help illustrate the concept of a starting point, similar to Java's `main` method. While Python doesn't require this, it is a good analogy to understand how Java programs are structured.

#### 4. Introduction to Data Types in Java


Java, like Python, has atomic (primitive) data types such as integers and booleans, but the syntax and naming conventions are slightly different.

| Type           | Python  | Java             |
| -------------- | ------- | ---------------- |
| Integer        | `int`   | `int`            |
| Floating Point | `float` | `float`/`double` |
| Boolean        | `bool`  | `boolean`        |
| String         | `str`   | `String`         |

Take time to explore and experiment with Java data types by writing small programs that declare and initialize these variables.



5\. Typing Variables in Java vs. Python



One significant difference between Python and Java is how they handle variable types. In Python, typing is dynamic, and you do not need to explicitly declare the type of a variable. Python will infer the type based on the value you assign.



In contrast, Java requires you to declare the type of every variable explicitly. This is called static typing, and it means that you need to specify whether a variable is an int, double, boolean, etc., at the time of declaration. This strict requirement can catch many errors at compile time that might otherwise only appear at runtime in Python.



Example: Typing Differences



Python Version:
```python
x = 10  # No need to declare type, Python infers it as an integer
x = "Hello"  # This is allowed in Python, as x can change its type
print(x)
```



Java Version:
```java
int x = 10;  // You must declare x as an int
x = "Hello";  // This will cause a compile-time error, as x is declared as an int
System.out.println(x);
```

In Java, once a variable is declared as a specific type, it cannot change to another type. This means that an int cannot suddenly become a String. This difference forces you to think about the type of data you are working with and ensures consistency throughout your code.


Another common error that is acceptable in Python but not in Java is the use of uninitialized variables. In Python, you can declare a variable without giving it an initial value, but in Java, every variable must be initialized before it is used.



Python Example:

```python
x = None  # This is fine in Python, though x is currently set to None
if x is None:
     x = 42

print(x)
```



Java Example:
```java
int x;  // Declaring x without initializing it
if (x == 0) {  // This will cause a compile-time error, as x must be initialized before use
    x = 42;
}

System.out.println(x);
```



Java's strict typing and initialization rules are part of what makes it a more verbose language, but also a safer one when it comes to type-related errors.6. Introducing Java Objects and Classes

Now, let’s dive into classes and objects, core components of Object-Oriented Programming (OOP). Below is a comparison of defining a simple class in both Python and Java. We are going to examine the differences between Python and Java so that you can start to get your head around this new way of thinking about programming.

**Interacting with the Calculator Class**

In Java, to interact with the `Calculator` class, you would first create an instance of the class and then call the methods using that instance. Here's an example of how you might use the `Calculator` class:

**Java Example: Using the Calculator**

```java
public class Main {
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        calc.push(10);
        calc.add(5);
        calc.mul(2);
        System.out.println("Current value: " + calc.value);  // Expected output: 30.0
    }
}
```

In Python, interacting with the `Calculator` class is quite similar. You create an instance and call the methods on that instance.

**Python Example: Using the Calculator**

```python
calc = Calculator()
calc.push(10)
calc.add(5)
calc.mul(2)
print("Current value:", calc.value)  # Expected output: 30.0
```

Now, let’s dive into classes and objects, core components of Object-Oriented Programming (OOP). Below is a comparison of defining a simple class in both Python and Java.

**Python Version: Calculator Class**

```python
class Calculator:
    def __init__(self):
        self.value = 0

    def push(self, number):
        self.value = number

    def add(self, number):
        self.value += number

    def sub(self, number):
        self.value -= number

    def mul(self, number):
        self.value *= number

    def div(self, number):
        if number != 0:
            self.value /= number
```

**Java Version: Calculator Class**

```java
public class Calculator {
    private double value;

    public Calculator() {
        this.value = 0;
    }

    public void push(double number) {
        this.value = number;
    }

    public void add(double number) {
        this.value += number;
    }

    public void sub(double number) {
        this.value -= number;
    }

    public void mul(double number) {
        this.value *= number;
    }

    public void div(double number) {
        if (number != 0) {
            this.value /= number;
        }
    }
}
```

##### Challenge: Implement and Compare the Calculator

- Write and run the Calculator class in both Python and Java.
- Notice the differences in how constructors and methods are defined.
- Pay attention to data types and access modifiers (like `private` in Java).

####

#### 7. Driving the Calculator


As you may recall from CS5001, we can create a driver script to interact with the `Calculator` class. This script will allow users to input an operator and a number, then perform the corresponding operation on the `Calculator` instance. Here is an example of how you could write a driver script in Python to interact with the `Calculator` class:

**Python Example: Driver Script**

```python
calc = Calculator()

while True:
    operator = input("Enter an operator (+, -, *, /) or 'exit' to quit: ")
    if operator == 'exit':
        break

    number = float(input("Enter a number: "))

    if operator == '+':
        calc.add(number)
    elif operator == '-':
        calc.sub(number)
    elif operator == '*':
        calc.mul(number)
    elif operator == '/':
        if number != 0:
            calc.div(number)
        else:
            print("Cannot divide by zero.")
    else:
        print("Invalid operator.")
        continue

    print("Current value:", calc.value)
```

Here is an example of how you could write a driver class in Java to interact with the `Calculator` class:

**Java Example: Driver Class**

```java
import java.util.Scanner;

public class CalculatorDriver {
    public static void main(String[] args) {
        Calculator calc = new Calculator();
        Scanner scanner = new Scanner(System.in);

        System.out.println("Enter an operator (+, -, *, /) or 'exit' to quit:");
        while (true) {
            String operator = scanner.nextLine();
            if (operator.equals("exit")) {
                break;
            }

            System.out.println("Enter a number:");
            double number = scanner.nextDouble();
            scanner.nextLine(); // Consume newline

            switch (operator) {
                case "+":
                    calc.add(number);
                    break;
                case "-":
                    calc.sub(number);
                    break;
                case "*":
                    calc.mul(number);
                    break;
                case "/":
                    if (number != 0) {
                        calc.div(number);
                    } else {
                        System.out.println("Cannot divide by zero.");
                    }
                    break;
                default:
                    System.out.println("Invalid operator.");
                    continue;
            }

            System.out.println("Current value: " + calc.value);
        }

        scanner.close();
    }
}
```

The above driver method allows users to input an operator (`+`, `-`, `*`, `/`) and a number from the keyboard. It performs the corresponding operation on the `Calculator` instance.
1. **Handling Division by Zero**

   - Think about what should happen when dividing by zero.
   - Implement a solution to handle division by zero in both the Python and Java versions of the `Calculator` class. Consider how you could provide meaningful feedback to the user or prevent the program from crashing.

2. **Interactive Driver Method**

   - Study the driver methods and see how the setting up of a object that we can interact with is quite similar in both languages.

**8. Summary**

By now, you should be comfortable:

- Setting up VS Code for Java development.
- Writing "Hello, World!" in Java and comparing it to Python.
- Understanding basic Java data types.
- Implementing and experimenting with classes in Java, using your Python knowledge as a reference.

Take your time to explore each of these resources and exercises. Java is more structured and strict than Python, but the foundational programming concepts are the same.

**Happy coding!**

