## AIM : 
To implement Pseudorandom Number Generation using Standard Library.
## ALGORITHM : 

Step 1: Get the number of random numbers to generate from the user.<br>

Step 2: Read the minimum and maximum values for the random number range.<br>

Step 3: Initialize the random seed using the current time.<br>

Step 4: Generate a random number by calculating the remainder of division with the range
(max - min + 1) and adding the minimum value.<br>

Step 5: Repeat the random number generation for the specified count.<br>

Step 6: Print each generated random number.<br>

Step 7: End the program.<br>

## PROGRAM:
```c
#include <stdio.h>

#define A 1664525
#define C 1013904223
#define M 4294967296 

unsigned int lcg(unsigned int seed) {
    return (A * seed + C) % M;
}

int main() {
    unsigned int seed;
    int n, i;
    printf("\n\n\n\n    *****Pseudorandom number generator*****\n\n\n\n");
    printf("Enter the seed value: ");
    scanf("%u", &seed);
    printf("Enter how many random numbers to generate: ");
    scanf("%d", &n);
    printf("Random numbers:\n");
    for (i = 0; i < n; i++) {
        seed = lcg(seed);
        printf("%u\n", seed);
    }
    return 0;
}
```
## RESULT:
![Screenshot 2024-10-10 085049](https://github.com/user-attachments/assets/70842e06-211f-4eac-ac95-9b0f814e0f1a)



