#include<stdio.h>

int main()
{
    int a, b;
    int i = 0;
    int j = 0;
    scanf_s("%d%d", &a, &b);
    while (a != 0 || b != 0)
    {
        for (a; a <= b; a++)
        {
            int arr = a;
            while (a != 0)
            {
                if ((a % 10) == 4)
                {
                    i++;
                    break;
                }
                else if ((a % 100) == 38)
                {
                    i++;
                    break;
                }
                else
                {
                    a /= 10;
                }
            }
            a = arr;
        }
        printf("%d\n", i);
        i = 0;
        scanf_s("%d%d", &a, &b);
    }
    return 0;
}
