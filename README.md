# finalexam
기말고사 보너스 과제입니다. 
#include <stdio.h>



void setarray(int*, int);



int main() {

    int alphabet[26] = { 0 };

    void* p = &alphabet;



    setarray(alphabet, sizeof(alphabet) / sizeof(alphabet[0]));



    for (int i = 0; i < 26; i++) {

        printf("%c ", *(char*)p); p = (int*)p + 1;

    }



    return 0;

}



void setarray(int* a, int size) {

    for (int i = 0; i < size; i++) a[i] = 65 + i;

}
