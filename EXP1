#include<stdio.h>
#include<stdlib.h>
#include<stdbool.h>
#define MAXSIZE 100
struct stack
{
    int items[MAXSIZE];
    int top;
};
void push(struct stack *s,int val)
{
    if(s->top==MAXSIZE-1)
    {
        printf("Stack is full \n");
    }
    s->items[++s->top]=val;
}
int pop(struct stack *s)
{
    if(s->top==-1)
    {
        printf("Stack is empty \n");
        exit(1);
    }
    return s->items[s->top--];
}
int peep(struct stack *s)
{
    if(s->top==MAXSIZE-1)
    {
        printf("Stack is Empty \n");
        exit(1);
    }
    return s->items[s->top];
}
void viewstack(struct stack *s)
{
    for(int i=s->top;i>=0;i--)
    {
        printf("%d \n",s->items[i]);
    }
}

void main()
{
    struct stack s;
    s.top=-1;
    int select;
    while(1)
    {
        printf("Select 1 for push operation \n");
        printf("Select 2 for pop operation \n");
        printf("Select 3 for peep operation \n");
        printf("Select 4 to view the stack \n");
        printf("Select 5 to exit \n");
     
        
        printf("Enter the option :\n");
        scanf("%d",&select);
        switch(select)
        {
            case 1:{
                int uval;
                printf("Enter the element \n");
                scanf("%d",&uval);
                push(&s,uval);
                break;
            }
            case 2:
            {
                printf("Popped element is %d",pop(&s));
                break;
            }
            case 3:
            {
             printf("The element at top of stack is: %d \n",peep(&s));
             break;
            }
            case 4:
            {
                viewstack(&s);
                break;
            }
            case 5:
            {
                exit(0);
                break;
            }
            default:{
                printf("Invalid");
            }
        }
    }
}
