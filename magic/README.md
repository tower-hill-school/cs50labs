# Magic Numbers

In this lab you will learn:

- Why do we use magic numbers
- How to use magic numbers

## What are Magic Numbers?

The variable lab, we replaced a "hard-coded" number representing age with a variable. This was a far better design than having to change the program each time you run it to hard-code another value.

There were still other hard-coded numbers though remaining even after replacing 17 with the variable `age`. We still have a 1, 10 and 50. What do these numbers represent? While this is a simple program and it may be easy to understand what each calculation is doing, in more complex programs, the meaning of hard-coded numbers may not be as obvious.

These numbers are called "Magic Numbers".

{% next %}

## Using Constants Instead!

When we have a need to use a number in a program whose value is never going to change, it's considered good design to use a constant. 

What if we wrote a program that does calculations that happen to use the number 3.14159265. Some people might recognize this as PI, but others may not be sure what our program is doing.

Since this number is never going to change value, we may want to define this as a constant. A program with PI defined as a constant could look like this:

```c
#include <cs50.h>
#include <stdio.h>

#define PI 3.14159265

int main(void)
{
  float radius = get_float("Radius in inches: ");
  float area = PI * radius * radius;
  printf("Your area is %.1f square inches.\n", area);
}
```

Notice the syntax for creating the consant PI, is the keyword `#define` then the **name** of the constant, `PI`, followed by the **replacement** value, 3.14159265. The general form of this is:

```
define NAME REPLACEMENT
```

{% next %}

## Your Turn

Modify the program on the right (the same program as in the variables lab) and change each of the **magic numbers** to **constants**. The first of these is already done for you.