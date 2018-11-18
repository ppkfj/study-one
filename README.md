# study-one
#include <stdio.h>
#include <string.h>
int main()
{
    char a[100];
    int i,j,k,t,m;
    while(1)
    {
        printf("输入字符:");
        gets(a);
        printf("输入移位数（1-25）:");
        scanf("%d%*c",&m);
        for(i=0; i<sizeof(a); i++)
        {
            if(a[i] >= 'A' && a[i] <= 'Z')
            {
                a[i] = ((a[i]-'A')+m)%26+'A';
            }
            else if(a[i] >= 'a' && a[i] <= 'z')
            {
                a[i] = ((a[i]-'a')+m)%26+'a';
            }
        }
        printf("%s",a);
        printf("\n");
    }
    return 0;
}
