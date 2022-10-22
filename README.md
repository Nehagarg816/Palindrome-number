# Palindrome-number
This is a program to determine whether a number is palindrome or not.


#include <stdio.h>
int Palindrome(int a)
{
    int rev = 0;
    int num = a;
    while (a != 0)
    {
        rev = rev * 10 + a % 10;
        a = a / 10;
    }
    printf("Reversed number is %d\n", rev);
    if (num == rev)
    {
        return 1;
    }
    else
    {
        return 0;
    }
}

int main()
{
    int n;
    printf("Enter one number: ");
    scanf("%d", &n);
    if (Palindrome(n))
    {
        printf("This number is a Palindrome");
    }
    else
    {
        printf("This number is not a Palindrome");
    }
    return 0;
}
