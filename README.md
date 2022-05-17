#include <stdio.h>

int main()
{
  int date,days,year,month,res1,res2,res3,pday,fday,res4,res5,res6,res7,res8,res9,res10;
printf("enter the date: ");
scanf("%d",&date);
printf("enter the month: ");
scanf("%d",&month);
if(month-1==0)
{
  days=date;
}
if(month-1==1)
{
  days=31;
}
if(month-1==2)
{
  days=59+date;
}
if(month-1==3)
{
  days=90+date;
}
if(month-1==4)
{
  days=120+date;
}
if(month-1==5)
{
  days=151+date;
}
if(month-1==6)
{
  days=181+date;
}
if(month-1==7)
{
  days=212+date;
}
if(month-1==8)
{
  days=243+date;
}
if(month-1==9)
{
  days=273+date;
}
if(month-1==10)
{
  days=304+date;
}
if(month-1==11)
{
  days=334+date;
}

res1=days%7;
if(res1>0)
{
pday=res1-1;
}
else{
  pday=7;
}
printf("enter the required year: ");
scanf("%d",&year);
if(year==2022)
{
  if(pday==0 || pday==7)
  {
    res9=7;
  }
  if(pday==1)
  {
    res9=1;
  }
  if(pday==2)
  {
    res9=2;
  }
  if(pday==3)
  {
    res9=3;
  }
  if(pday==4)
  {
    res9=4;
  }
  if(pday==5)
  {
    res9=5;
  }
  if(pday==6)
  {
    res9=6;
  }
}
else
{if(year<2022)
{
  if(year%4==3)
  {
    res3=2022-year;
  res4=res3/4;
  res5=res3%4;
  res6=res4*5+res5+2;
  res7=res6-pday;
  res8=res7%7;
  res9=8-res8;
  }
  else{
res3=2022-year;
  res4=res3/4;
  res5=res3%4;
  res6=res4*5+res5+1;
  res7=res6-pday;
  res8=res7%7;
  res9=8-res8;
  }
  
}
else{
  if(year%4==3)
  {
res3=year-2022;
  res4=res3/4;
  res5=res3%4;
  res6=res4*5+res5+2;
  res7=7-pday;
  res8=res6-res7;
  if(res8<8)
  {
    res9=res8;
  }
  else{
    res10=res8%7;
    res9=8-res10;
  }
  }
  else{
res3=year-2022;
  res4=res3/4;
  res5=res3%4;
  res6=res4*5+res5+1;
  res7=7-pday;
  res8=res6-res7;
  if(res8<8)
  {
    res9=res8;
  }
  else{
    res10=res8%7;
    res9=8-res10;
  }
  }
  
  
}}
if(res9==1 || res9==8)
{
  printf("%d month,%dth-%d is sunday",month,date,year);
}
if(res9==2)
{
  printf("%d month,%dth-%d is monday",month,date,year);
}
if(res9==3)
{
  printf("%d month,%dth-%d is tuesday",month,date,year);
}
if(res9==4)
{
  printf("%d month,%dth-%d is wednesday",month,date,year);
}
if(res9==5)
{
  printf("%d month,%dth-%d is thursday",month,date,year);
}
if(res9==6)
{
  printf("%d month,%dth-%d is friday",month,date,year);
}
if(res9==7)
{
  printf("%d month,%dth-%d is saturday",month,date,year);
}
return 0;
}

