#include<stdio.h>
#include<conio.h>
int menu();
void sum();
void palidrome(int);
int armstrong();
int square(int);
void main()
{
      int a,b,c;
      char yn;
      clrscr();
      do
      {
	    c=menu();
	    switch(c)
	    {
		  case 1:
			 sum();
			 break;
		  case 2:
			 printf("enter value for checking palidrome or not:");
			 scanf("%d",&c);
			 palidrome(c);
			 break;
		  case 3:
			 c=armstrong();
			 if(c==1)
			      printf("armstrong number");
			 else
			      printf("not armstrong number");
			      break;
		  case 4:
			 printf("enter any number to print square series:");
			 scanf("%d",&a);
			 c=square(a);
			 break;
		  case 5:
			 exit(0);
		  default:
			 printf("invalid choice");
	    }
	    printf("\nYou want to continue? if yes(Y/y) else no(N/n):");
	    flushall();
	    scanf("%c",&yn);
      }while(yn=='y'||yn=='Y');
      getch();
}
int menu()
{
       int choice;
       printf("\n\n\tMenu\n");
       printf("\n\t1\tSum of digit:\n");
       printf("\n\t2\tPalidrome number:\n");
       printf("\n\t3\tArmstrong number:\n");
       printf("\n\t4\tSquare series:\n");
       printf("\n\t5\tExit\n");
       printf("\nEnter your choice:");
       scanf("%d",&choice);
       return choice;
}
void sum()
{
       int n,i,s=0;
       printf("Enter any number:");
       scanf("%d",&n);
       while(n>0)
       {
	     i=n%10;
	     s=s+i;
	     n=n/10;
       }
       printf("sum of digit is :%d",s);
}
void palidrome(int n)
{
		    int i,s=0,t=n;
		    while(n>0)
		    {
			i=n%10;
			s=(s*10)+i;
			n=n/10;
		    }
		    if(t==s)
			  printf("number is palidrome");
		    else
			  printf("number is not palidrome");
}
int armstrong()
{
       int n,i,s=0,t;
       printf("enter any number:");
       scanf("%d",&n);
       n=t;
       while(n>0)
       {
	    i=n%10;
	    s=s+(i*i*i);
	    n=n/10;
       }
       if(t==s)
	    return 1;
       else
	    return 0;
}
int square(int a)
{
	int i;
	printf("\n\n");
	for(i=1;i<=a;i++)
	    printf("%d",i*i);
	return 0;
}
