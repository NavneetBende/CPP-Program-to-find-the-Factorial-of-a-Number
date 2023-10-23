# CPP-Program-to-find-the-Factorial-of-a-Number

Factorial of a Number in C++
Here we will discuss how to find the factorial of a number in C++ programming language.

Factorial of any number is the product of it and all the positive numbers below it for example factorial of 5 is 120

Factorial of n (n!) = 1 * 2 * 3 * 4....n
5! = 1 x 2 x 3 x 4 x 5 = 120 7! = 1 x 2 x 3 x 4 x 5 x 6 x 7 = 5040

Factorial
Ways discussed:-
Iterative approach
Recursive approach
Method 1 (Iterative)
C++ Code
Run
#include<iostream>
using namespace std;
int main ()
{
    int num = 6, fact = 1;
    
    // Factorial of negative number doesn't exist
    // Read more here - https://www.quora.com/Is-the-factorial-of-a-negative-number-possible
    if(num < 0)
        cout << "Not Possible";
    else
    {
        for(int i = 1; i <= num; i++)
            fact = fact * i;
    }
    
    cout << "Fact " << num << ": " << fact;
}
// Time complexity: O(N)
// Space complexity: O(1)
Output
Fact 6: 720
Related Pages
Fibonacci Series upto nth term

Find the Nth Term of the Fibonacci Series

Factorial of a number

Power of a number

Factor of a number

Strong number

Method 2 (Recursive)
This method uses recursion in C++

Run
#include<iostream>
using namespace std;

int getFactorial(int num)
{
    if(num == 0)
        return 1;
        
    return num * getFactorial(num-1);
}
int main ()
{
    int num = 8;
    
    int fact = getFactorial(num);
    
    cout << "Fact " << num << " : " << fact;
    
    return 0;
}
// Time complexity: O(N)
// Space complexity: O(1)
// Auxiliary Space complexity (Function call stack): O(N)
Output
Fact 8 : 40320
