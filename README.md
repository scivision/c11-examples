# C11 standard Examples

![Actions Status](https://github.com/scivision/c11-examples/workflows/ci/badge.svg)

A few examples of C11 standard to check compilers and build systems.

## Static assert

[C11 static_assert](https://en.cppreference.com/w/c/language/_Static_assert)
issues compile-time errors if the assertion is false.
This can be useful particularly for IoT and embedded systems where integer types may
[not behave the same](https://blog.feabhas.com/2014/10/vulnerabilities-in-c-when-integers-go-bad/)
as the developer's laptop or other systems.
For legacy code, putting a couple `static_assert` can flag the engineer right away if `int` or `long` aren't the expected bit width.

## Variable length array

C11 introduced variable length arrays.
C11 standard says VLA length cannot be 0.
Some compilers allow this anyway so to be portable, don't have 0 length VLA.
