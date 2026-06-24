# Post-Mock Exam

## Multiple Choice Questions

### Unit 1
1. What is printed when this code is executed??

   ```
   int a = 10;
   int b = 2;
   double d = a / b; 
   System.out.println(d);
   ```
   
   Answer:  3.0


2.  What is the value of X after execution?
  
   ```
   int x = 2;
   x += 3;
   x *= 2;
   x -= 5;
   ```

   Answer: 5

3.  Which is a correct constructor call?
   * A.  `Scanner s = Scanner(System.in);`
   * B.  `Scanner s = new Scanner();`
   * C.  `Scanner s = new Scanner(System.in);`
   * D.  `new Scanner s(System.in);`

### Unit 2

4.  What is printed when the code below executes?
   ```
   int n = 7;
   while (n > 0) {
       n -= 3;
       System.out.print(n + " ");
   }
   ```
   
   Answer:  "4 1 -2"

5.  What is printed?
   ```
   String s = "banana";
   for (int i = 0; i < s.length(); i++)
      if (s.charAt(i) == 'n')
          System.out.print(i + " ");
   ```
   Answer: "2 4"

6.  What is printed?
   ```
   int sum = 0;
   for (int i = 2; i <= 5; i++)
       sum += i;
   System.out.println(sum);
   ```

   Answer: 14 (2+3+4+5)

7.  Which question generates a random number from 1-4 inclusive?

   * A.  `(int)(Math.random() * 4)` 
   * B.  `(int)(Math.random() * 4) + 1`
   * C.  `(int)(Math.random() * 3) + 1`
   * D.  `(int)(Math.random() * 5)`

   Answer: B

8.  What is printed?
   ```
   String s = "hello";
   s.toUpperCase();
   System.out.println(s);
   ```

   Answer: "hello".  s.toUpperCase() returns an upper cased String, the original String is immutable.


9.  Which expression is equivalent to !(a >= 5 && a <= 10)?

   * A. a < 5 || a > 10
   * B. a < 5 && a > 10
   * C. !(a > 5 || a < 10)
   * D. a == 5 || a == 10

   Answer: A

10.  What is printed?

   ```
   int x = 3;
   for (int i = 0; i < x; i++) {
       x--;
       System.out.print(i + " ");
   }
   ```
   Answer: "0 1 "

### Unit 3

11.  What is printed when this code runs?

   ```
   public class Student {
       private String name;
       private double gpa;
       
       public void printInfo() {
           System.out.println(name + " " + gpa);
       }
   }
   
   // In main method:
   Student s = new Student();
   s.printInfo();
   ```

   Answer:  "null 0.0"

12.  Which line causes a compile error?

   ```
   public class BankAccount {
       private double balance;
       public double getBalance() { return balance; }
   }

   // In a separate class:
   public class Main {
       public static void main(String[] args) {
           BankAccount acct = new BankAccount();
           double x = acct.balance;      // Line A
           double y = acct.getBalance(); // Line B
       }
   }
   ```
   
   Answer:  Line A only

13.  Which represents a "has-a" relationship (composition)?  

   ```
   // Option 1:
   public class Car {
       private Engine engine;
   }
   
   // Option 2:
   public class Car extends Engine { }
   ```

   Answer:  Option 1

14.  What is the result of this code? (Look carefully at the constructor!)
   ```
   public class Cat {
       private String name;
       
       public Cat(String name) {
           name = name;  // Bug here!
       }
       
       public String getName() { return name; }
   }
   
   // In main:
   Cat c = new Cat("Whiskers");
   System.out.println(c.getName());
   ```
   
   Answer:  Prints 'null'

15.  Consider the following class. What is printed?
   ```
   public class Counter {
       private static int shared = 0;
       private int local = 0;
   
       public void bump() {
           shared++;
           local++;
       }
   
       public String report() {
           return shared + "," + local;
       }
   }

   // In main:
   Counter x = new Counter();
   Counter y = new Counter();
   x.bump(); x.bump(); x.bump();
   y.bump();
   System.out.println(x.report());
   System.out.println(y.report());
   ```

   Answer:  "4 3 \n 4 1"

### Unit 4 

16.  What is printed?
   ```
   int[] arr = {1, 2, 3, 4, 5};
   System.out.println(arr[5]);
   ```

   Answer:  ArrayIndexOutOfBoundsException

17.  What does this method return for arr = {2, 4, 6, 8}?
   ```
   public static boolean check(int[] arr) {
       for (int val : arr) {
           if (val % 2 != 0) {
               return false;
           }
       }
       return true;
   }
   ```
   Answer: true

18.  What is printed?
   ```
   int[][] arr = {{1, 2, 3}, {4, 5, 6}};
   System.out.println(arr[1][2]);
   ```

   Answer: 6

19. What is printed? 
   ```
   int[][] arr = {{1, 2, 3}, {4, 5, 6}};
   arr[0] = arr[1];
   arr[1][0] = 99;
   System.out.println(arr[0][0]);
   ```

   Answer:  99

20.  What is printed?
   ```
   ArrayList list = new ArrayList();
   list.add(10);
   list.add(20);
   list.add(30);
   list.add(1, 15);
   System.out.println(list.get(2));
   ```

21.  What is printed?
   ```
   public static int operate(int n) {
       if (n == 1) { return 1; }
       return n * operate(n-1);
   }

   public static void main(String[] args) {
       System.out.println(operate(4));
   }
   ```
   Answer: 4*3*2*1 = 24

## Free Response

1. We have one class representing names, and another class which is intended to compose letters from a sender to a recipient.  

```
public class Name {
    private String firstName;
    private String lastName;

    public Name(String firstName, String lastName) {
        this.firstName = firstName;
        this.lastName = lastName;
    }

    public String getFirstName() { return firstName; }
    public String getLastName() { return lastName; }
    public String asSignature() { /* To be implemented in part A */ }
}
```

A.  Complete the body of the asSignature() method using the following rules:  Signatures should be the first initial, capitalized, of the first name, followed by a period.  i.e. "H." for "Herbert".  Then the last name should be rendered with only the first letter capitalized.  Examples:  "geoff sanchez" -> "G. Sanchez".  "ABBY MARTIN" -> "A. Martin".

B.  Add a second class in it's entirety, named Letter.  Letter should have instance variables for two Names, the sender and the recipent of the letter, as well as a String of the letter text.  It should provide a method `public String render()` which builds the full letter text, consisting of:

Dear recipient.firstName, (with only the first letter capitalized)

letter text

Sincerely,
Sender's signature.

For example, if we are sending the letter "I miss you terribly.", from "geoff sanchez" to "ABBY MARTIN", it should render as:

Dear Abby,

I miss you terribly.

Sincerely,
G. Sanchez.

2. You have a class representing your schedule for the day, with per-minute availability, as follows:

```
public class Appointment {
  int hour;
  int minute;
  int duration;

  public Appointment(int hour, int minute, int duration) {
      this.hour = hour;
      this.minute = minute;
      this.duration = duration;
  } 
}
public class Schedule {
  boolean busy = new boolean[24][60];

  public Schedule() {
  }
  
  public int findAvailability(int hour, int numMinutes) { /* Implement in part A */ }

  public boolean bookApointment(int hour, int numMinutes) { /* Implement in part B */ }

  public Appointment bookFirstAvailable(int hour, int numMinutes) { /* Implement in part B */ }

}
```

The Schedule class maintains a 2-D array of booleans indicating whether you are busy in a given minute of a given hour of the day.  The first index is hours, and the second is minutes.

Part A:  Write a function which, when given an hour and numMinutes, locates the beginning of the first chunk of contiguous free minutes at least numMinutes in length, and 
