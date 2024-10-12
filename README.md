# CODTECH-TASK-1

The "Simple Calculator" is a console-based Java application that allows users to perform basic arithmetic operations like addition, subtraction, multiplication, and division on two numbers. Here's a detailed overview of the project:

### Purpose

The main purpose of the Simple Calculator project is to help users understand basic programming concepts in Java, such as:
- Input and output handling
- Control flow using conditionals (if statements and switch-case)
- Exception handling (specifically division by zero)

### Components

1. *Imports*:
   - The program imports the Scanner class from the Java util package to facilitate user input.

   java
   import java.util.Scanner;
   

2. *Class Declaration*:
   - The main class of the application is named Calculator.

   java
   public class Calculator {
   

3. *Main Method*:
   - The application starts execution from the main method, which is the entry point in any Java application.

   java
   public static void main(String[] args) {
   

4. *User Input*:
   - A Scanner object is created to read user input from the console.
   - The user is prompted to enter two numbers:

   java
   System.out.println("Enter the first number:");
   double num1 = scanner.nextDouble();
   System.out.println("Enter the second number:");
   double num2 = scanner.nextDouble();
   

5. *Choosing an Operation*:
   - The user is presented with options for operations using a simple menu system (a series of println statements).
   - The user selects an operation by entering a corresponding number (1, 2, 3, or 4).

   java
   System.out.println("Choose an operation:");
   System.out.println("1. Addition");
   System.out.println("2. Subtraction");
   System.out.println("3. Multiplication");
   System.out.println("4. Division");
   int operation = scanner.nextInt();
   

6. *Performing Calculations*:
   - A switch statement is used to execute different blocks of code based on the user's input.
   - For each case:
     - *Case 1*: Executes addition.
     - *Case 2*: Executes subtraction.
     - *Case 3*: Executes multiplication.
     - *Case 4*: Executes division but checks for division by zero to prevent runtime errors. If an attempt is made to divide by zero, an error message is displayed.

   java
   switch (operation) {
       case 1:
           result = num1 + num2;
           break;
       case 2:
           result = num1 - num2;
           break;
       case 3:
           result = num1 * num2;
           break;
       case 4:
           if (num2 != 0) {
               result = num1 / num2;
           } else {
               System.out.println("Error: Division by zero!");
               return;
           }
           break;
       default:
           System.out.println("Error: Invalid operation!");
           return;
   }
   

7. *Displaying the Result*:
   - The final result of the computation is displayed back to the user.

   java
   System.out.println("The result is: " + result);
   

### Error Handling

- *Division by Zero*: The program checks for division by zero and displays an error message if the user attempts to divide by zero.
- *Invalid Operation*: If the user inputs an invalid operation (i.e., any number other than 1 to 4), the program outputs an error message.

### Enhancements and Future Improvements

While the Simple Calculator provides fundamental functionality, it can be expanded or enhanced in various ways:

1. *More Operations*: Introduce more advanced mathematical functionalities like modulus, exponentiation, or square roots.
2. *Input Validation*: Add error handling for non-numerical inputs to prevent exceptions when the user enters invalid data (like letters).
3. *User Interface*: Develop a graphical user interface (GUI) using Java Swing for improved user experience.
4. *History Feature*: Implement a feature to keep track of previous calculations and allow users to view their calculation history.
5. *Refactoring*: Split the code into smaller methods for each individual operation to adhere to best practices in software design.

