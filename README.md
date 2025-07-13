# Prime Number Checker

A simple C library for working with prime numbers.

## Functions

### `is_prime(int x)`
Checks if a number is prime.
- **Returns:** 
  - `1` if the number is prime
  - `0` if the number is not prime
  - `-1` if the number is less than 2

### `next_prime(int x)`
Finds the next prime number starting from the given number.
- **Returns:** The next prime number greater than or equal to `x`

## Files

- `prime.h` - Header file with function declarations
- `prime.c` - Implementation of prime number functions

## Usage

Include the header file in your C program:

```c
#include "prime.h"

int main() {
    int num = 10;
    
    if (is_prime(num) == 1) {
        printf("%d is prime\n", num);
    } else {
        printf("%d is not prime\n", num);
    }
    
    printf("Next prime after %d is %d\n", num, next_prime(num));
    
    return 0;
}
```

## Compilation

Compile your program with:
```bash
gcc -o program main.c prime.c -lm
```

Note: The `-lm` flag is needed to link the math library for the `sqrt()` function.
