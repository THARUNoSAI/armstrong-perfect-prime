//checking of the number is armstrong or perfect or prime
#include<stdio.h>
#include<math.h>
void prime(int n){
  int m=0;
  for (int x=1;x<=n;x++){
    if(n%x==0){
      m++;
    }
  }
  if(m==2){printf("%d is prime",n);}
  else{printf("\n%d is composite",n);}
}
void armstrong(int n){
  int a=n,power=0;
  while (a>=1){
    int b=a%10;
    a=a-b;
    a=a/10;
    power+=1;
  }
  int sum1=0,f=n,d=0;
  while (f>=1){
    int b=f%10;
    f=f-b;
    f=f/10;
    int po=pow(b,power);
    sum1=sum1+po;
  }
  if (sum1==n){printf("\n%d is an armstrong number",n);}
  else{printf("\n%d is not an armstrong number",n);}
}
void perfect(int n){
  int g=0;
  for(int x=1;x<n;x++){
    if (n%x==0){g+=x;}
  }
  if(g==n){printf("\n%d is a perfect number",n);}
  else{printf("\n%d is not a perfect number",n);}
}
int main(){
  int n;
  scanf("%d",&n);
  prime(n);
  armstrong(n);
  perfect(n);
}
