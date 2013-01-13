Here are my notes for the C language, that I've made for a quick reference in the future. It something like a cheatsheet, but very personal.

```c
int a[4] = {1,2,3,4};
int a[] = {1,2,3,4};
int a[] = {0};
int *pa;
int **pb;
```

take third element of an array

```
a[3] == *(a + 3) == 3[a] == *(&a[0] + 3)
```

basically array variable is a pointer on a first element of array

`*pa` - get value

`pa` - get or set memory location

`pa = a`

`pa = &a[0]` - the same as above

`*a` - get first element of array

`int &b` - reference, cannot be NULL or uninitialized

`pa = &b` - get address of variable and assign it to pointer

`**pb = &pa` - reference on reference
