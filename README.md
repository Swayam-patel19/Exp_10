# Exp_10

# Aim

To study and implement Pointer Operations (Call by value and Call by reference).

# Theory

Pointers are symbolic representations of addresses.
We can pass arguments to funtions using different methods mainly call by value and call by reference.

Call by value
In the call-by-value method, function arguments are passed by copying the value of the actual parameter, ensuring the original values remain unchanged.
The value is copied to the formal parameter.
Any changes made to the parameters within the function do not change the original values outside the function.

Call by reference
In the call-by-reference method, the memory address (reference) of the actual parameter is passed to the function, allowing direct access and modification of the original values.
The actual and the formal parameters point to the same memory address.

Any changes made to the parameters within the function are directly reflected in the original values outside the function.

# Code and Output

(A)

```
// Printing the values by using callby value 

#include<iostream> 
using namespace std; 
void swap(int x, int y) 
{
    int swap;
    swap=x;
    x=y;
    y=swap;
}

int main() 
{
    int a=4, b=7;
    swap(a,b);
    cout<<"Value of a is: "<<a<<"\n";
    cout<<"Value of b is: "<<b<<"\n";
    return 0;
}
```

<img width="362" alt="Screenshot 2024-08-23 at 11 10 33" src="https://github.com/user-attachments/assets/ff00818c-fea8-4439-a85f-84a87de0879d">



(B)
```
// Swapping the values 

#include<iostream> 
using namespace std; 
void swap(int *x, int *y) 
{
    int *swap;
    swap=x;
    x=y;
    y=swap;
}

int main() 
{
    int a=4,b=7;
    swap(a,b);
    cout<<"Value of a is: "<<a<<"\n";
    cout<<"Value of b is: "<<b<<"\n";
    return 0;
}
```

<img width="124" alt="Screenshot 2024-08-23 at 11 10 51" src="https://github.com/user-attachments/assets/bfe8b8d5-049c-4a2a-af96-23933f05254d">



(C)
```
// Swapping the values using call by reference  

#include<iostream> 
using namespace std; 
void swap(int *x, int *y) 
{
    int swap;
    swap=*x;
    *x=*y;
    *y=swap;
}

int main() 
{
    int a=4,b=7;
    swap(&a,&b);
    cout<<"Value of a is: "<<a<<"\n";
    cout<<"Value of b is: "<<b<<"\n";
    return 0;
}
```

<img width="257" alt="Screenshot 2024-08-23 at 11 12 56" src="https://github.com/user-attachments/assets/7ebf4402-a68e-492a-925a-1b93e096ef33">


# Conclusion 

We learnt about pointers and how to pass arguments to functions using call by value and call by reference methods. I also learnt how to swap values using call by reference.
