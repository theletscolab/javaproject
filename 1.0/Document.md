In the Java programming language, every application must contain a main method whose signature is:

public static void main(String[] args)
The modifiers public and static can be written in either order (public static or static public), but the convention is to use public static as shown above. You can name the argument anything you want, but most programmers choose "args" or "argv".

The main method is similar to the main function in C and C++; it's the entry point for your application and will subsequently invoke all the other methods required by your program.

The main method accepts a single argument: an array of elements of type String.

public static void main(String[] args)
This array is the mechanism through which the runtime system passes information to your application. For example:

java MyApp arg1 arg2
Each string in the array is called a command-line argument. Command-line arguments let users affect the operation of the application without recompiling it. For example, a sorting program might allow the user to specify that the data be sorted in descending order with this command-line argument:

-descending
The "Hello World!" application ignores its command-line arguments, but you should be aware of the fact that such arguments do exist.

Finally, the line:

System.out.println("Hello World!");


Questions
Question 1: When you compile a program written in the Java programming language, the compiler converts the human-readable source file into platform-independent code that a Java Virtual Machine can understand. What is this platform-independent code called?

Answer 1: Bytecode.

Question 2: Which of the following is not a valid comment:

a. /** comment */
b. /* comment */
c. /* comment
d. // comment

Answer 2: c is an invalid comment.

Question 3: What is the first thing you should check if you see the following error at runtime:

Exception in thread "main" java.lang.NoClassDefFoundError:
HelloWorldApp.java.
Answer 3: Check your classpath. Your class cannot be found.

Question 4: What is the correct signature of the main method?

Answer 4: The correct signature is public static void main(String[] args) or public static void main(String... args)

Question 5: When declaring the main method, which modifier must come first, public or static?

Answer 5: They can be in either order, but the convention is public static.

Question 6: What parameters does the main method define?

Answer 6: The main method defines a single parameter, usually named args, whose type is an array of String objects.

Exercises
Exercise 1: Change the HelloWorldApp.java program so that it displays Hola Mundo! instead of Hello World!.

Answer 1: This is the only line of code that must change:

System.out.println("Hola Mundo!"); //Display the string.
Exercise 2: You can find a slightly modified version of HelloWorldApp here: HelloWorldApp2.java

The program has an error. Fix the error so that the program successfully compiles and runs. What was the error?

Answer 2: Here's the error you get when you try to compile the program:

HelloWorldApp2.java:7: unclosed string literal
System.out.println("Hello World!); //Display the string.
^
HelloWorldApp2.java:7: ')' expected
System.out.println("Hello World!); //Display the string.
^
2 errors
To fix this mistake, you need to close the quotation marks around the string. Here is the correct line of code:

System.out.println("Hello World!"); //Display the string.
