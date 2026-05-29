#include <stdio.h>

int prime(int n);

int main()
{
    int num, flag = 0;

    printf("Enter a number: ");
    scanf("%d", &num);

    // 1. Assign the returned value to flag
    flag = prime(num);

    // 2. Print the result based on the flag value
    if (flag == 0)
    {
        printf("%d is a prime number.\n", num);
    }
    else
    {
        printf("%d is not a prime number.\n", num);
    }

    return 0;
}

int prime(int n)
{
    // 3. Handle numbers less than or equal to 1
    if (n <= 1)
    {
        return 1;
    }

    int flag = 0;
    for (int i = 2; i <= n / 2; i++)
    {
       if (n % i == 0)
       {
           flag = 1;
           break;
       }
    }

    return flag;
}
