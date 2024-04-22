
#include <stdio.h>

int main() {
   float a,b;
   int result;
    sub_result://label for goto
   printf("enter your 1st number =   ");
   scanf("%f",&a);
   printf("enter your 2nd number =  ");
   scanf("%f",&b);
   printf("which do you want ? \n 1= sum \n 2= subtraction \n 3= multiplication \n 4= divisn \n  = ");
   scanf("%d",&result);
   float sum = a+b;
   float subtraction= a-b;
   float multiplication= a*b;
   float division = a/b;
  
   switch(result){
       case 1: printf(" your  result is = %.1f \n",sum);
       break;
        case 2: printf(" your  result is = %.1f \n ",subtraction);
       break;
        case 3: printf(" your  result is = %.1f \n ",multiplication);
       break;
        case 4: printf(" your  result is = %.1f \n ",division);
       break;
       
        default:
       printf("Error.try again\n");
       break;
       
   }
   if(result>4){
       goto sub_result;
   }
   int again;
    again:
   printf("Do you want more ? \n 1= yes or 2= no ");
   printf("\n  = ");
   scanf("%d",&again);
   if(again==1){
       goto sub_result;
   }
   else{
       printf("exit successfully");
   }
    return 0;
