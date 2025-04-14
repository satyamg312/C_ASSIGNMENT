# C_ASSIGNMENT
// armstrong.h
#ifndef ARMSTRONG_H
#define ARMSTRONG_H

// Function prototype
int isArmstrong(int num);

// Function definition
int isArmstrong(int num) {
    int original = num, result = 0, remainder;

    while (num != 0) {
        remainder = num % 10;
        result += remainder * remainder * remainder;
        num /= 10;
    }

    return (result == original);
}
// main.c
#include <stdio.h>
#include "armstrong_func.h"

int main() {
    int number;

    printf("Enter a number: ");
    scanf("%d", &number);

    if (isArmstrong(number))
        printf("%d is an Armstrong number.\n", number);
    else
        printf("%d is not an Armstrong number.\n", number);

    return 0;
}
// prime.h

int isPrime(int num) {
    if (num <= 1)
        return 0;
    for (int i = 2; i * i <= num; i++) {
        if (num % i == 0)
            return 0;
    }
    return 1;
}
// main.c

#include <stdio.h>
#include "prime_func.h"

int main() {
    int number;

    printf("Enter a number: ");
    scanf("%d", &number);

    if (isPrime(number))
        printf("%d is a Prime number.\n", number);
    else
        printf("%d is NOT a Prime number.\n", number);

    return 0;
    
}
// odd_even.h
#include <stdio.h>

// Simple function to check odd or even
void checkOddEven(int num) {
    if (num % 2 == 0) {
        printf("%d is Even.\n", num);
    } else {
        printf("%d is Odd.\n", num);
    }
}
// main.c
#include <stdio.h>
#include"odd.h"  // Including our custom header file

int main() {
    int number;

    printf("Enter an integer: ");
    scanf("%d", &number);

    checkOddEven(number);  // Calling the function

    return 0;
}
