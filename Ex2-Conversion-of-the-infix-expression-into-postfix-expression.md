# Ex 1b Conversion of the infix expression into postfix expression
## DATE:22/2/25
## AIM:
To write a C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule.

## Algorithm
1. Start the program. 
2. Initialize a stack and set the top index to -1. 
3. Define the push() and pop() functions to add and remove elements from the stack. 
4. Define the priority() function to assign priorities to operators. 
5. Traverse the expression in the IntoPost() function, handling operands, parentheses, and 
operators. 
6. After processing the expression, pop and print any remaining operators from the stack. 
7. End. 

## Program:
```
/*
Program to convert the infix expression into postfix expression
Developed by: Poojasree B
RegisterNumber: 212223040148
*/

#include<ctype.h> 
 
char stack[100]; 
int top = -1; 
void push(char x) 
{ 
stack[++top]=x; 
 
} 
 
char pop() 
{ 
if(top==-1) 
return 0; 
else 
return stack[top--]; 
} 
int priority(char x) 
{ 
if(x=='(') 
  
  
{ 
return 0; 
} 
if(x=='&'||x=='|') 
{ 
return 1; 
} 
if(x=='+'||x=='-') 
{ 
return 2; 
} 
if(x=='*'||x=='/'||x=='%') 
{ 
return 3; 
} 
if(x=='^') 
{ 
return 4; 
} 
return 0; 
} 
char IntoPost(char *exp) 
{ 
char *e,x; 
e=exp; 
while(*e!='\0') 
{ 
if(isalnum(*e)) 
{ 
printf("%c ",*e); 
} 
else if(*e=='(') 
{ 
push(*e); 
} 
else if(*e==')') 
{ 
while((x=pop())!='(') 
printf("%c ",x); 
} 
else 
{ 
while(priority(stack[top])>=priority(*e)) 
printf("%c ",pop()); 
push(*e); 
} 
e++; 
} 
while(top != -1) 
{ 
printf("%c ",pop()); 
}return 0; 
} 
int main() 
{ 
char exp[100]="3%2+4*(A&B)"; 
IntoPost(exp); 
return 1; 
}
```

## Output:

![Screenshot 2025-06-01 144443](https://github.com/user-attachments/assets/0254becd-1f11-4b2a-ae07-be9e84756bc8)



## Result:
Thus, the C program to convert the infix expression into postfix form using stack by following the operator precedence and associative rule is implemented successfully.
