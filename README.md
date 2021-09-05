# DSA_BootCamp_Assignment

1. Write a program to Swap to two numbers: 
#include<iostream.h>
#include<conio.h>

void main()
{
int a,b,c;
clrscr();
cout<<"Enter value of a: ";
cin>>a;
cout<<"Enter value of b: ";
cin>>b;
c=a;
a=b;
b=c;
cout<<"After swap a: "<<a<<"b: "<<b;
getch();
}

2. Write a program to find the largest number among three numbers entered by the user:
#include <iostream>
using namespace std;

int main() {    
    float n1, n2, n3;

    cout << "Enter three numbers: ";
    cin >> n1 >> n2 >> n3;

    if(n1 >= n2 && n1 >= n3)
        cout << "Largest number: " << n1;

    if(n2 >= n1 && n2 >= n3)
        cout << "Largest number: " << n2;

    if(n3 >= n1 && n3 >= n2)
        cout << "Largest number: " << n3;

    return 0;
}

3. Write a program to check whether a year entered by a user is Leap year or not:
#include <iostream>
using namespace std;

int main() {
    int year;

    cout << "Enter a year: ";
    cin >> year;

    if (year % 4 == 0) {
        if (year % 100 == 0) {
            if (year % 400 == 0)
                cout << year << " is a leap year.";
            else
                cout << year << " is not a leap year.";
        }
        else
            cout << year << " is a leap year.";
    }
    else
        cout << year << " is not a leap year.";

    return 0;
}

4. Write a program to display Fibonacci Series upto nth term. (Using loops): 
#include <iostream>
using namespace std;

int main() {
    int n, t1 = 0, t2 = 1, nextTerm = 0;

    cout << "Enter the number of terms: ";
    cin >> n;

    cout << "Fibonacci Series: ";

    for (int i = 1; i <= n; ++i) {
        // Prints the first two terms.
        if(i == 1) {
            cout << t1 << ", ";
            continue;
        }
        if(i == 2) {
            cout << t2 << ", ";
            continue;
        }
        nextTerm = t1 + t2;
        t1 = t2;
        t2 = nextTerm;

        cout << nextTerm << ", ";
    }
    return 0;
}

5. Write a program to check whether a number is Prime or Not:
#include <iostream>
using namespace std;

int main() {
    int i, n;
    bool isPrime = true;

    cout << "Enter a positive integer: ";
    cin >> n;

    // 0 and 1 are not prime numbers
    if (n == 0 || n == 1) {
        isPrime = false;
    }
    else {
        for (i = 2; i <= n / 2; ++i) {
            if (n % i == 0) {
                isPrime = false;
                break;
            }
        }
    }
    if (isPrime)
        cout << n << " is a prime number";
    else
        cout << n << " is not a prime number";

    return 0;
}

6.  Print this pattern using loops
For n=5
	    *
	   * *
	  * * *
	 * * * *
	* * * * *
#include<iostream>
using namespace std;
int main()
{
int n, s, i, j;
cout << "Enter number of rows: ";
cin >> n;
for(i = 1; i <= n; i++)
{
//for loop to put space
for(s = i; s < n; s++)
cout << " ";
//for loop for displaying star
for(j = 1; j <= i; j++)
cout << "* ";
// ending line after each row
cout << "\n";
}
return 0;
}

7. Write a program that takes n elements from the user and displays the second largest element of an array:
#include <iostream>
using namespace std;
int main(){
   int n, num[50], largest, second;
   cout<<"Enter number of elements: ";
   cin>>n;
   for(int i=0; i<n; i++){
      cout<<"Enter Array Element"<<(i+1)<<": ";
      cin>>num[i];
   }
   /* Here we are comparing first two elements of the
    * array, and storing the largest one in the variable
    * "largest" and the other one to "second" variable.
    */
   if(num[0]<num[1]){ 
      largest = num[1];
      second = num[0];
   }
   else{ 
      largest = num[0];
      second = num[1];
   }
   for (int i = 2; i< n ; i ++) {
      /* If the current array element is greater than largest
       * then the largest is copied to "second" and the element
       * is copied to the "largest" variable.
       */
      if (num[i] > largest) {
         second = largest;
         largest = num[i];
      }
      /* If current array element is less than largest but greater
       * then second largest ("second" variable) then copy the
       * element to "second"
       */
      else if (num[i] > second && num[i] != largest) {
         second = num[i];
      }
   }
   cout<<"Second Largest Element in array is: "<<second;
   return 0;
}

8. left rotation in c++:
#include <bits/stdc++.h>
using namespace std;
int main()
{
    int siz,op;
    cin>>siz>>op;
    long int arr[siz],arr1[siz]; // two array of same size
    for(int i=0; i<siz; i++)
    {
        cin>>arr[i]; // taking input
    }
    for(int i=0; i<siz; i++)
    {
        // if (index - number of operations) is -ve 
           if(i-op<0) 
        {
            int k = op-i;
            arr1[siz-k]=arr[i];
        }
        else  if (index - number of operations) is +ve 
        {   int k = i-op;
            arr1[k] = arr[i];
        }
    }
    for(int i=0; i<siz; i++)
    {
        cout<<arr1[i]<<" "; // printing the array
    }
    return 0;
}

9. grading students hackerrank solution in c++:
#include <iostream>
#include <algorithm>
#include <unordered_map>
using namespace std;
int main(){
int n;
cin >> n;
for(int a0 = 0; a0 < n; a0++){
int grade;
cin >> grade;
if (grade >= 38) {
int rem = grade % 5;
if (rem >= 3) grade += 5 - rem;
}
cout << grade << endl;
}
return 0;
}

10. Camel Case using C++:
#include <iostream>
#include <algorithm>
#include <unordered_map>
using namespace std;
int main(){
    string s;
    cin >> s;
    int t=1;
    for (int i=0;i<s.length();i++)
        if (isupper(s[i]))
        t++;
        cout<<t<<endl;
    return 0;
}
