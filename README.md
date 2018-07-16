Fibonacci
=========
Fibonaaci sequence contains a series of numbers where the nth digit is calculated by the sum of (n-2)th and (n-1)th.

This program deploys four functions for Fibonacci calculation including Vanilla Recursive, Tail Recursive, Top-down Dynamic, and Bottom-up Dynamic (iterative).


//////////////////// Brief explaination of each funtion /////////////////////////
For general case: If n is either 0 or 1, it will return 1.

Vanilla recursive: Starts from n and iterates all the way to 1 when it recursives forwards to calculate the values.

Tail recursive: Also starts from n but updates its additional parameters as n decreases (everytime a recursive is called). 

Top-down Dynamic: Solve the overall big problem and determines if the subproblems have been calculated yet. (f(10) = f(9) + f(8);...; f(3) = f(2) + f(1) = 1 + 1 = 2).

Bottom-up Dynamic: Calculates subproblems then uses the results to solve bigger problems. (In order to solve f(5), calculate f(3) and f(4) first).


//////////////////// How to determine the best methods of the four /////////////////////////

Apply the functions run_to_failure(...) and time(...) to the four different algorithms and observe time spent for each function. The method with the least amount of time spent without causing segmentation fault is the most effective.



//////////////////////////// Results ////////////////////////////

 Input n needed to make function take over 5 seconds:
 
 Vanilla Recursive (fib1): 44 
 
 Tail Recursive (fib2):    131072 (seg fault)
 
 Top-down Dynamic (fib3):  65536 (seg fault)
 
 Bottom-up Dynamic (fib4): 2147483648
 
 ===> The best method is Bottom-up Dynamic.
