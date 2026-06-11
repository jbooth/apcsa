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

9.  What is printed?

   ```
   int x = 3;
   for (int i = 0; i < x; i++) {
       x--;
       System.out.print(i + " ");
   }
   ```
   Answer: "0 1 "

### Unit 3


