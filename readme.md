Here are my notes for the C language, that I've made for a quick reference in the future. It something like a cheatsheet, but very personal.

```c
int a[4] = {1,2,3,4};
int a[] = {1,2,3,4};
int a[] = {0};
int *pa;
int **pb;
```

take third element of an array

`a[3] == *(a + 3) == 3[a] == *(&a[0] + 3)` - basically array variable is a pointer on a first element of array

```c
if (a[3] == *(a + 3) &&
  a[3] == 3[a] &&
  a[3] == *(&a[0] + 3)) {
  printf("yey");
}
```

`*pa` - get value

`pa` - get or set memory location

`pa = a`

`pa = &a[0]` - the same as above

`*a` - get first element of array

`int &b` - reference, cannot be NULL or uninitialized

`pa = &b` - get address of variable and assign it to pointer

`**pb = &pa` - reference on reference

### Function pointer (similar to C++ templates)

```c
#include <stdio.h>

int referenced(int val) {
  return 2 * val;
}

void execute(int (*ptr)(int)) {
  printf("%d\n", ptr(3));
}

int main() {
  int (*ptr_func)(int) = &referenced;

  execute(ptr_func);

  return 1;
}
```

## References

* http://en.cppreference.com/w/
