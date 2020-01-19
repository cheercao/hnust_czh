#include <stdio.h>
#include<stdlib.h>
#include<math.h>
int main()
{
    int n,m,t,z,h,p,i,count,x;
    while(scanf("%d %d",&n,&p)!=EOF){
    count=0;
    for(i=n;i<=p;i++)
    if(i<99)count++;
    else {
        x=i;
    m=x%10;
    x=x/10;h=m-x%10;
    while(x!=0)
    {
        t=x%10;
        z=m-t;
        if(z!=h)break;
        m=t;
        x/=10;
    }
    if(x==0)
        count++;
    }
    printf("%d\n",count);
    }
    return 0;
}
ADA IV型数的定义如下: 把一个正整数的各个位上的数字依次组成一个数列,如果该数列是等差数列,则该数为ADA IV型数.如13579和2468都是ADA IV型数, 153和246810都不是ADA IV型数.为了避免不必要的麻烦,规定区间[1,99]的数均为ADA IV型数.
有没有更快更简便的方法？？
