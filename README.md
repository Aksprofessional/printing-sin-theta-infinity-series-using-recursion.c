# printing-sin-theta-infinity-series-using-recursion.c
// C program for sin theta infinite series #include &lt;stdio.h>}
// C program for sin theta infinite series
#include <stdio.h>
#include <math.h>
double exmp(int,int,int);
long fact(int);
int main() {
    int n,x,s=1;
    double e;
    puts("enter x and n");
    scanf("%d%d",&x,&n);
    e=exmp(x,n,s);
    printf("%.2lf",e);
    return 0;
}

double exmp(int x,int n,int s)
{
    if(n==1)
    return x;
    return s*(pow(x,n)/fact(n))+exmp(x,n-2,-s);
}
long fact(int n)
{
    if(n==0)
    return 1;
    return n*fact(n-1);
}
