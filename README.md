# ECE-220-Assignment-1-a-2
#include <stdio.h>

int main() {
    int num1;
    int num2;
    int num3;
    int max;
    int mid;
    int min;
    printf("Please enter 3 numbers please.\n");
    scanf("%d %d %d",&num1, &num2, &num3);

    if ((num1 > num2) && (num1 > num3)){
        if (num2 > num3) {
            max = num1;
            mid = num2;
            min = num3;
        }
        if (num3 > num2){
            max = num1;
            mid = num3;
            min = num2;
        }
    }
    if  ((num2 > num1) && (num2 > num3)){
        if(num1 > num3){
            max = num2;
            mid = num1;
            min = num3;
        }
        if(num1 <num3) {
            max = num2;
            mid = num3;
            min = num1;
        }
    }
    if ((num3 > num1) && (num3 > num2)){
        if(num1 > num2){
            max = num3;
            mid = num1;
            min = num2;
        }
        if(num1 < num2) {
            max = num3;
            mid = num2;
            min = num1;
        }
    }
    printf("Min:%d\n",min);
    printf("Middle:%d\n",mid);
    printf("Max:%d\n",max);

    printf("***The odd numbers are:\n");
    if (min %2 != 0){
        while (min < mid){
            printf("value:%d\n",min);
            min += 2;
        }

    }
    else{
        ++min;
        while (min < mid){
            printf("value:%d\n",min);
            min += 2;
        }
    }

    printf("***The even nunbers are:\n");
    if (mid %2 == 0){
        while (mid < max){
            printf("value:%d\n",mid);
            mid += 2;
        }

    }
    else{
        ++mid;
        while (mid < max){
            printf("value:%d\n",mid);
            mid += 2;
        }
    }
}
