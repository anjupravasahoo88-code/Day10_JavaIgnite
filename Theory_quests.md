1)Explain Java Exception hierarchy:

Throwable
Exception
Error

Give one example for each.

ANSWER:-

-> Java exception hierarchy starts with Throwable.
-> Throwable → Parent class of all errors and exceptions.
      Example: Throwable t = new Exception();
-> Exception → Problems that can be handled by the programmer.
      Example: ArithmeticException, NullPointerException, InputMismatchException
-> Error → Serious problems that usually cannot be handled by the program.
       Example: OutOfMemoryError, StackOverflowError
-> Hierarchy:
Throwable
   |
   |-- Exception
   |
   |-- Error


2)Can we have multiple catch blocks?
Explain with example when it is useful.

ANSWER:-

-> Yes, we can use multiple catch blocks in one try block.It is useful when different exceptions need different handling.
Example:
try {
    int a = 10 / 0;
}
catch (ArithmeticException e) {
    System.out.println("Cannot divide by zero");
}
catch (Exception e) {
    System.out.println("Some other error");
}
-> Use: It helps us give different messages for different errors.

3)A program crashes when user enters text instead of number.

What exception occurs?

How will you handle it?

Where should try-catch be placed?

ANSWER:-

What exception occurs?
-> InputMismatchException
How will you handle it?
-> Using a try-catch block.
Where should try-catch be placed?
-> Around the code that takes input from the user.
Example:
try {
    int num = sc.nextInt();
}
catch (InputMismatchException e) {
    System.out.println("Invalid Input");
}
-> This prevents the program from crashing and shows a proper message.



4)try {
    int a = 10 / 0;
    
    System.out.println("Hello");

}

catch(Exception e) {

    System.out.println("Error handled");

}

System.out.println("End");

Predict the output - 
ANSWER:-
    Error handled
    End

What prints first?
ANSWER:-
  -> Error handled prints first because division by zero causes an exception.

Does program stop?
ANSWER:-
    -> No. The exception is caught by the catch block, so the program continues and prints End.




