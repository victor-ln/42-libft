# 42-Libft

![libftm](https://user-images.githubusercontent.com/81260589/182065710-0140075f-fbb2-4802-9ab9-fb19172c6a24.png)

## Table of contents

- [Introduction](#Introduction)
- [How to run](#How-to-run)
- [Usage](#Usage)
- [Reference tables](#Reference-table)

## Introduction

This project is my first project as a student at school 42 São Paulo.
I've recoded a few functions of the C standard library (libc) as well as some other useful functions.

## How to run

- Clone the repository:
`git clone https://github.com/victor-ln/42-Libft.git`
- Access the cloned folder:
`cd 42-Libft`
- Run the Makefile:
`make`
- To clean objects files execute:
`make clean`
- To clean libft.a:
`make fclean`
- Recompile:
`make re`

## Usage

- Add `#include "libft.h"` in your source code or header file.
- Compile it with __libft.a__: ``gcc main.c libft.a``

## Reference tables

### Functions from `<ctype.h>`

These functions `is*` checks c and returns nonzero if the character c falls into the tested class, or zero if not.

| Functions | Description |
| --- | --- |
| [ft_isalpha](42-Libft/ft_isalpha.c) | Checks for an alphabetic character. |
| [ft_isdigit](42-Libft/ft_isdigit.c) | Checks for a digit (0 through 9). |
| [ft_isalnum](42-Libft/ft_isalnum.c) | Checks for an alphanumeric character. |
| [ft_isascii](42-Libft/ft_isascii.c) | Checks whether c fits into the ASCII character set. |
| [ft_isprint](42-Libft/ft_isprint.c) | Checks for any printable character. |
| [ft_toupper](42-Libft/ft_toupper.c) | Converts char to uppercase. |
| [ft_tolower](42-Libft/ft_tolower.c) | Converts char to lowercase. |

### Functions from `<string.h>`

| Functions | Description |
| --- | --- |
| [ft_strlen](42-Libft/ft_strlen.c) | Returns how many characters are in the given string excluding the '\0'. |
| [ft_memset](42-Libft/ft_memset.c) | Fills the first n bytes of the memory area pointed by s with the constant byte c. |
| [ft_bzero](42-Libft/ft_bzero.c) | Erases the data in the n bytes of the memory starting at the location pointed by s, by writing zeros (bytes containing '\0') to that area. |
| [ft_memcpy](42-Libft/ft_memcpy.c) | Copies n bytes from memory area src to memory area dest. The memory areas must not overlap. |
| [ft_memccpy](42-Libft/ft_memccpy.c) | Copies no more than n bytes from memory area src to memory area dest, stopping when the character c is found. |
| [ft_memmove](42-Libft/ft_memmove.c) | Copies n bytes from memory area src to memory area dest. |
| [ft_strlcpy](42-Libft/ft_strlcpy.c) | Copies up to size - 1 characters from the NUL-terminated string src to dst, NUL-terminating the result. |
| [ft_strlcat](42-Libft/ft_strlcat.c) | Appends the NUL-terminated string src to the end of dst. It will append at most size - strlen(dst) - 1 bytes, NUL-terminating the result. Returns the initial length of dst plus the length of src |
| [ft_strchr](42-Libft/ft_strchr.c) | Returns a pointer to the first occurrence of the character c in the string src or NULL if the character is not found. |
| [ft_strrchr](42-Libft/ft_strrchr.c) | Returns a pointer to the last occurrence of the character c in the string s. |
| [ft_strcmp](42-Libft/ft_strcmp.c) | Compares both strings s1 and s2 and returns the difference between them or zero if they're equal. |
| [ft_strcat](42-Libft/ft_strcat.c) | Returns an array of strings obtained by splitting ’s’ using the character ’c’ as a delimiter. The array is ended by a NULL pointer. |
| [ft_strncmp](42-Libft/ft_strncmp.c) | It is similar to strcmp() function, except it only compares the first (at most) n bytes of s1 and s2. |
| [ft_memchr](42-Libft/ft_memchr.c) | Scans the initial n bytes of the memory area pointed by s for the first instance of c. Both c and the bytes of the memory area pointed by s are interpreted as unsigned char. |
| [ft_memcmp](42-Libft/ft_memcmp.c) | 	Compares the first n bytes (each interpreted as unsigned char) of the memory areas s1 and s2. |
| [ft_strnstr](42-Libft/ft_strnstr.c) | Locates the first occurrence of the null-terminated string little in the string big, where not more than len characters are searched. Characters that appear after a '\0' character are not searched. If little is an empty string, big is returned; if little occurs nowhere in big, NULL is returned; otherwise a pointer to the first character of the first occurrence of little is returned. |
| [ft_strdup](42-Libft/ft_strdup.c) | 	Returns a pointer to a new string which is a duplicate of the string s. |

### Functions from `<stdlib.h>`

| Functions | Description |
| --- | --- |
| [ft_atoi](42-Libft/ft_atoi.c) | Converts the initial portion of the string pointed by nptr to int. |
| [ft_atol](42-Libft/ft_atol.c) | The same as atoi, except that it converts to long. |
| [ft_calloc](42-Libft/ft_calloc.c) | Allocates memory for an array of nmemb elements of size bytes each and returns a pointer to the allocated memory. The memory is set to zero. If nmemb or size is 0, then returns NULL. |

### Non-standard functions

| Functions | Description |
| --- | --- |
| [ft_substr](42-Libft/ft_substr.c) | Allocates with malloc() and returns a substring from the string ’s’. The substring begins at index ’start’ and is of maximum size ’len’. |
| [ft_strjoin](42-Libft/ft_strjoin.c) | Allocates with malloc() and returns a new string, which is the result of the concatenation of ’s1’ and ’s2’. |
| [ft_strtrim](42-Libft/ft_strtrim.c) | Allocates with malloc() and returns a copy of ’s1’ with the characters specified in ’set’ removed from the beginning and the end of the string. |
| [ft_split](42-Libft/ft_split.c) | Returns an array of strings obtained by splitting ’s’ using the character ’c’ as a delimiter. The array is ended by a NULL pointer. |
| [ft_itoa](42-Libft/ft_itoa.c) | Returns a string representing the integer received as an argument. |
| [ft_utoa](42-Libft/ft_utoa.c) | Returns a string representing the unsigned integer received as an argument. |
| [ft_strmapi](42-Libft/ft_strmapi.c) | Applies the function ’f’ to each character of the string ’s’ to create a new string with malloc() resulting from successive applications of ’f’. Returns the string created from the successive applications of ’f’ or NULL if the allocation fails |
| [ft_striteri](42-Libft/ft_striteri.c) | Applies the function f to each character of the string passed as argument, and passing its index as first argument. Each character is passed by address to f to be modified if necessary. |
| [ft_putchar_fd](42-Libft/ft_putchar_fd.c) | Outputs the character ’c’ to the given file descriptor. |
| [ft_putstr_fd](42-Libft/ft_putstr_fd.c) | Outputs the string ’s’ to the given file descriptor. |
| [ft_putendl_fd](42-Libft/ft_putendl_fd.c) | Outputs the string ’s’ to the given file descriptor, followed by a newline. |
| [ft_putnbr_fd](42-Libft/ft_putnbr_fd.c) | Outputs the integer ’n’ to the given file descriptor. |

### Linked list functions

| Functions | Description |
| --- | --- |
| [ft_lstnew](42-Libft/ft_lstnew.c) | Returns a new element. The variable ’content’ is initialized with the value of the parameter ’content’. The variable ’next’ is initialized to NULL. |
| [ft_lstmap](42-Libft/ft_lstmap.c) | Iterates the list ’lst’ and applies the function ’f’ to the content of each element. Creates a new list resulting of the successive applications of the function ’f’. The ’del’ function is used to delete the content of an element if needed. |
| [ft_lstadd_front](42-Libft/ft_lstadd_front.c) | Adds the element ’new’ at the beginning of the list. |
| [ft_lstadd_back](42-Libft/ft_lstadd_back.c) | Adds the element ’new’ at the end of the list. |
| [ft_lstsize](42-Libft/ft_lstsize.c) | Counts the number of elements in a list. |
| [ft_lstlast](42-Libft/ft_lstlast.c) | Returns the last element of the list. |
| [ft_lstiter](42-Libft/ft_lstiter.c) | Iterates the list ’lst’ and applies the function ’f’ to the content of each element. |
| [ft_lstclear](42-Libft/ft_lstclear.c) | Deletes and frees the given element and every successor of that element, using the function ’del’ and free(). Finally, the pointer to the list is set to NULL. |
| [ft_lstdelone](42-Libft/ft_lstdelone.c) | Takes as a parameter an element and frees the memory of the element’s content using the function ’del’ given as a parameter and free the element. The memory of ’next’ is not freed. |
