# MyProGRamS
Solved problems 

//PATTERN PRINTING
/*
h
pa
*yp
*/
#include<stdio.h>

int main() 
{
    char arr[100];
    int n,k=0;
    scanf("%s%n",arr,&n);
    int x,y=2,z=1,sum=0;
    while(z<=15)
    {
        sum +=z;
        if(sum>=n)
            break;
        z++;
    }
    for(int i=0;i<z;i++)
    {
        int j=0;
        x = k;
        while(j<=i)
        {
            if(x==n)
            {
                printf("$");
                x--;
            }
            else if(x<n)
            {
                printf("%c",arr[x]);
                x--;
            }
            else
            {
                printf("$");
                x--;
            }
            j++;
        }
        k+=y;
        y++;
        printf("\n");
    }
}
