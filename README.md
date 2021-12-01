/*# 2021.12.1--
计算打车费用*/

#include <stdio.h>
 
float taxifee(int clock,int miles)
{
    float money;
    if(miles<=3)
    {
        money=14;
        printf("费用为14\n");
    }
    else
    {
        if(clock>=23 || clock<5)
        {
            money=13+1+2.3*(miles-3)*1.2;
            printf("夜间车费为：%f\n",money);
        }
        else
        {
            money=13+1+2.3*(miles-3);
            printf("日间车费为：%f\n",money);
        }
    }
    
    return money;    
}
int main()
{
    printf("打的总费用：%.1f\n",taxifee(9,12)+taxifee(18,12));
    return 0;
}
