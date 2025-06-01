# Ex 1e Stack Operations
## DATE: 1/3/25
## AIM:
To write a C function to perform push and pop operation of the stack in the infix to postfix conversion.

## Algorithm
1. Initialize top as -1 and declare stack as a character array. 
2. To push, increment top and assign the character to stack[top]. 
3. To pop, check if top is -1 and return -1 if true. 
4. If not, return stack[top] and decrement top.    

## Program:
```
/*
Program to find and display the priority of the operator in the given Postfix expression
Developed by: Poojasree B
RegisterNumber:  212223040148
*/
 
char stack[100]; 
int top = -1; 
void push(char x) 
{ 
    stack[++top] = x; 
} 
 
char pop() 
{ 
    if(top == -1) 
        return -1; 
    else 
        return stack[top--]; 
}
```

## Output:

<img width="248" alt="image" src="https://github.com/user-attachments/assets/d1e3139e-df34-4af3-a61c-4fa07a7f850d" />


## Result:
Thus the C program to perform push and pop operation of the stack in the infix to postfix conversion is implemented successfully.
