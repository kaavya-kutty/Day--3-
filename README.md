# Day--3-
#include <stdio.h>

int isPrime(int n)
{
    int i;

   if (n <= 1)
        return 0;

  for (i = 2; i <= n / 2; i++)
    {
        if (n % i == 0)
            return 0;
    }

   return 1;
}

int main()
{
    int n;

  printf("Enter a positive integer: ");
    scanf("%d", &n);

   if (isPrime(n))
        printf("%d is a prime number", n);
    else
        printf("%d is not a prime number", n);

  return 0;
}
#include <stdio.h>

int countDigit(int n, int digit)
{
    if (n == 0)
        return 0;

  if (n % 10 == digit)
        return 1 + countDigit(n / 10, digit);
    else
        return countDigit(n / 10, digit);
}

int main()
{
    int n, digit, count;

  printf("Enter a positive integer: ");
    scanf("%d", &n);

  printf("Enter the digit to count: ");
    scanf("%d", &digit);

   count = countDigit(n, digit);

   printf("The digit %d occurs %d times", digit, count);

  return 0;
}
#include <stdio.h>

void reverseNumber(int n)
{
    if (n == 0)
        return;

   printf("%d", n % 10);
    reverseNumber(n / 10);
}

int main()
{
    int n;

  printf("Enter a positive integer: ");
    scanf("%d", &n);

   printf("Reversed number: ");
    reverseNumber(n);

  return 0;
}
