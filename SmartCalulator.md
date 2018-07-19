# SmartCalculator
Few additional method apply in this code
#include<stdio.h>

int add( int n1,int n2)
{
    return n1+n2;
}
int sub (int n1,int n2)
{
    return n1-n2;
}
int mul (int n1,int n2)
{
    return n1*n2;

}
int div (int n1 ,int n2)
{
    return n1/n2;
}
int sumsqr(int n1,int n2)
{
    return n1*n1+2*n1*n2+n2*n2;
}
int subsqr(int n1,int n2)
{
    return n1*n1-2*n1*n2+n2*n2;
}
int suminsqr(int n1,int n2)
{
    return n1*n1+2*n1*n2+n2*n2-2*n1*n2;
}
int subinsqr(int n1,int n2)
{
    return (n1+n2)*(n1-n2);
}

int main ()

{
int number1,number2,result,n;

while(1)
{

   printf ("Enter two numbers (for two 0s to exit):\n" );
    scanf("%d %d",&number1,&number2);
    if (number1 ==0 && number2 ==0)
    {
        printf("program terminated");
        break;
    }
    printf ("Enter \n\n\t1 for addition \n\n\t2 for subtraction\n\n\t3 for multiplication\n\n\t4 for division\n\n\t5 for ( number1 + number2)^2 \n\n\t6 for (number1 - number2)^2 \n\n\t7 for (number1)^2 +(number2)^2 \n\n\t8 for (number1)^2-(number2)^2 \n\n\t");

   scanf("%d",&n);
    if (n==1)
    {
       result=add(number1,number2);

   }
   else if (n==2)
    {
        result=sub(number1,number2);

   }
    else if (n==3)
    {
        result=mul(number1,number2);
    }
    else if (n==4)
    {
        if(number2 ==0 )
        {
            printf("Can not divide by zero");
            continue;
        }
        result =div(number1,number2);

   }
   else if (n==5)
    {
        result=sumsqr(number1,number2);
    }
    else if(n==6)
    {
        result=subsqr(number1,number2);
    }
    else if (n==7)
    {
        result=suminsqr(number1,number2);
    }
else if (n==8)
{
    result=subinsqr(number1,number2);
}
    else
        {
        printf("unknown operator \n");
    continue;
}
printf("result is : \t %d \n\n \t\t *****YOUR MATH IS SOLVED*****\n>>>>> Again: \n \n \n",result);
}
return 0;
}
