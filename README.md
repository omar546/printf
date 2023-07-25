# 0x11. C - printf

This project implements a simplified version of the `printf` function in the C programming language. The `_printf` function allows for formatted output to the standard output stream, supporting conversion specifiers for characters, strings, and integers. The implementation adheres to the requirements and constraints specified in the project prompt.

## Table of Contents
- [Introduction](#introduction)
- [File Descriptions](#file-descriptions)
- [Usage](#usage)
- [Supported Conversion Specifiers](#supported-conversion-specifiers)
- [Compilation](#compilation)
- [Example](#example)

## Introduction

The `printf` function in the C Standard Library is used to print formatted output to the standard output stream. It takes a format string containing directives, conversion specifiers, and plain characters. In this project, we provide our own implementation of the `_printf` function that handles specific conversion specifiers.

## File Descriptions

The project includes the following files:

- `main.c`: Contains the main function used for testing the `_printf` function.
- `main.h`: Header file containing function prototypes and necessary includes.
- `print_functions.c`: Contains the implementation of the `_printf` function and related helper functions.
- `print_helpers.c`: Contains helper functions to print characters, strings, and integers.

## Usage

To use the `_printf` function, include the `main.h` header file in your C code. Then, call the function with a format string and any required arguments. The function returns the number of characters printed.

```c
#include "main.h"

int main(void)
{
    _printf("Hello, %s!\n", "world");
    return (0);
}
```

## Supported Conversion Specifiers

The `_printf` function supports the following conversion specifiers:

- `%c`: Character
- `%s`: String
- `%%`: Percent sign (literal `%`)
- `%d`: Signed decimal integer
- `%i`: Signed decimal integer

The function does not support flag characters, field width, precision, or length modifiers, as specified in the project requirements.

## Compilation

To compile the program, use the following command:

```
gcc -Wall -Werror -Wextra -pedantic -std=gnu89 *.c -o printf
```

## Example

```c
#include <stdio.h>
#include "main.h"

int main(void)
{
    int len;

    len = _printf("Hello, %s!\n", "world");
    _printf("Number: %d\n", 12345);
    _printf("Character: %c\n", 'A');
    _printf("Percent: %%\n");
    _printf("Unknown: %r\n");
    _printf("Length: %i\n", len);
    return (0);
}
```

Output:
```
Hello, world!
Number: 12345
Character: A
Percent: %
Unknown: %r
Length: 18
```

This example demonstrates the usage of different conversion specifiers with the `_printf` function. Unsupported specifiers are handled gracefully, and the function returns the correct length of characters printed.
