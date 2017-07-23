# reverse

#include <stdlib.h>
#include <stdio.h>
#include <string.h>

char* reverseString(char* s) {
    
    int length = 0, i = 0;
    length = strlen(s);
    char temp[1];
    
    for(i = 0; i < length/2; i++)
    {
        *temp = s[i];
        s[i] = s[length-i-1];
        s[length-i-1] = *temp;
    }
    return s;
}

int main(void) {
    
    char *str = malloc(sizeof(char *) * 250); //arbitrary memory allocation
    scanf("%s", str); //get input from user
    reverseString(str);
    printf("%s\n", str);
    
    free(str); //free memory
    return 0;
}
