# Sum-of-all-prime-in-range
Sum of all prime number in a given range in c language

**INPUT 1 : 12  24
**OUTPUT: 72

```

#include <stdio.h>

int main()
{
    int i, j, end, isPrime, sum=0;

    int l;
    scanf("%d",&l);
    scanf("%d", &end);

    for(i=l; i<=end; i++)
    {

        isPrime = 1;
        for(j=2; j<=i/2 ;j++)
        {
            if(i%j==0)
            {
              
                isPrime = 0;
                break;
            }
        }

        if(isPrime==1)
        {
            sum += i;
        }
    }

    printf("%d",sum);

    return 0;
}


