
# Libft
*Your very first own library*

### Table of Contents
* **About the project**
* * [Introduction](#introduction)
* * [Function Overview](#function-overview)
* * [Bonus](#bonus)
* **Usage**
* * [Requirements](#requirements)
* * [Instructions](#instructions)
* [**Goals**](#goals)
* [**Skills**](#skills)


## About the project

### Introduction

In this project we'll be implementing our home-made functions from libc, which will be very useful to get familiar with memory allocation, and to think of creative ways to code these functions.

### Function Overview

| Function 		| Description 												| Prototype |
| -- 			| -- 													| -- |
| `ft_atoi` 		| Reads a String, and, after ignoring spaces with  `ft_isspace`, saves the string into an integer	| `int	ft_atoi(const char *nptr);`
| `ft_bzero` 		| Writes  `n`  zeroes to the string  `s` 								| `void	ft_bzero(void *s, size_t n);`
| `ft_calloc` 		| Reserves  `x`  blocks of  `y`  bits of memory 							| `void	*ft_calloc(size_t nmemb, size_t size);`
| `ft_isalnum` 		| Returns  `1`  if the input is a number or a letter in the  `ASCII`  table 				| `int	ft_isalnum(int c);`
| `ft_isalpha` 		| Returns  `1`  if the input is a letter in the  `ASCII`  table 					| `int	ft_isalpha(int c);`
| `ft_isascii` 		| Returns whether or not a value belongs to the  `ASCII`  table 					| `int	ft_isascii(int c);`
| `ft_isdigit` 		| Returns  `1`  if the input is a number in the  `ASCII`  table 					| `int	ft_isdigit(int c);`
| `ft_isprint` 		| Returns whether a character is printable 								| `int	ft_isprint(int c);`
| `ft_itoa` 		| Saves the given number as a string (char array)							| `int	ft_get_len_int(unsigned long n);`
| `ft_memchr` 		| Looks for a matching character inside a part of the memory						| `void	*ft_memchr(const void *s, int c, size_t n);`
| `ft_memcmp` 		| Compares two parts of memory, returning  `0`  if they're the  same, or else a nonzero value		| `int	ft_memcmp(const void *s1, const void *s2, size_t n);`
| `ft_memcpy` 		| Copies from one part of memory to another, ignoring possible overlaps					| `void	*ft_memcpy(void *dest, const void *src, size_t n);`
| `ft_memmove` 		| Copies from one part of memory to another, preventing possible overlaps				| `void	*ft_memmove(void *dest, const void *src, size_t n);`
| `ft_memset` 		| Assigns a character  `n`  times to a part of the memory						| `void	*ft_memset(void *ptr, int c, size_t n);`
| `ft_putchar_fd` 	| Prints a character to the given file descriptor							| `void	ft_putchar_fd(char c, int fd);`
| `ft_putendl_fd` 	| Prints a string followed by a new line  `\n`  to a given file descriptor				| `void	ft_putendl_fd(char *s, int fd);`
| `ft_putnbr_fd` 	| Prints number to the given file descriptor								| `void	ft_putnbr_fd(int n, int fd);`
| `ft_putstr_fd` 	| Prints string to the given file descriptor								| `void	ft_putstr_fd(char *s, int fd);`
| `ft_split` 		| Splits a string according to a given separator character						| `char	**ft_split(char const *s, char c);`
| `ft_strchr` 		| Looks for a specific character inside a given string							| `char	*ft_strchr(const char *s, int c);`
| `ft_strdup` 		| Saves enoug space and duplicates a string								| `char	*ft_strdup(const char *s);`
| `ft_striteri`		| Applies the 'f' function to every element in a string							| `void	ft_striteri(char *s, void (*f)(unsigned int, char*));`
| `ft_strjoin` 		| Concatenates two strings allocating enough space first						| `char	*ft_strjoin(char const *s1, char const *s2);`
| `ft_strlcat` 		| Concatenates two strings ensuring it ends with  `\0`							| `size_t	ft_strlcat(char *dst, const char *src, size_t size);`
| `ft_strlcpy` 		| Copies  `n - 1`  bytes from a source string to a destination string					| `size_t	ft_strlcpy(char *dst, const char *src, size_t size);`
|`ft_strlen` 		| Returns length of a string										| `size_t	ft_strlen(const char *tab);`
| `ft_strmapi`		| Applies a function (mapping) to every element in a string						| `char	*ft_strmapi(char const *s, char (*f)(unsigned int, char));`
| `ft_strncmp` 		| Compares two strings up to the n-th character 							| `int	ft_strncmp(const char *s1, const char *s2, size_t n);`
| `ft_strnstr`		| Tries to find a substring (`needle`) in a second string (`haystack`) before the n-th char is reached 	| `char	*ft_strnstr(const char	*big, const char *little, size_t n);`
| `ft_strrchr` 		| Looks for a given character in a string, reading it from back to front 				| `char	*ft_strrchr(const char *s, int c);`
| `ft_strtrim`		| Removes occurrences of characters in a string from the start and end of another one 			| `char	*ft_strtrim(char const *s1, char const *set);`
| `ft_substr`		| Copies from the n-th char of a string 								| `char	*ft_substr(char const *s, unsigned int start, size_t len);`
| `ft_tolower`		| Makes every uppercase character in a string lowercase 						| `int	ft_tolower(int c);`
| `ft_toupper` 		| Makes every lowercase character in a string uppercase 						| `int	ft_toupper(int c);`

### Bonus

For this part we implemented a struct defining the well-known linked lists
```c
typedef	struct	s_list
{
	void		*content;
	struct	s_list	*next;
}			t_list; 
```

Bonus functions to implement

| Bonus Function 	|  Description 								| Prototype |
| -- 			| -- 									| -- |
| `ft_lstnew` 		|Creates new node allocating with  `malloc` 				| `t_list	*ft_lstnew(void *content);`
| `ft_lstadd_front` 	| Adds new node at the beginning of the linked list 			| `void	ft_lstadd_front(t_list **alst, t_list *new);`
| `ft_lstsize` 		| Returns number of elements of linked list 				| `int	ft_lstsize(t_list *lst);`
| `ft_lstlast` 		| Retrieves last node of the list 					| `t_list	*ft_lstlast(t_list *lst);`
| `ft_lstadd_back` 	| Adds new node at the end of the linked list 				| `void	ft_lstadd_back(t_list **alst, t_list *new);`
| `ft_lstdelone` 	| Deletes, frees, and applies function del to content of a given node 	| `void	ft_lstdelone(t_list *lst, void (*del)(void *));`
| `ft_lstclear` 	| Deletes a given element and every element after that 			| `void	ft_lstclear(t_list **lst, void (*del)(void *));`
| `ft_lstiter` 		| Applies a function to the content of every node of the linked list 	| `void	ft_lstiter(t_list *lst, void (*f)(void *));`
| `ft_lstmap` 		| Applies function to a copy of the list, freeing when necessary 	| `t_list	*ft_lstmap(t_list *lst, void *(*f)(void *), void (*del)(void *));`

## Usage

### Requirements

The function is written in C language and thus needs the  **`gcc`  compiler**  and some standard  **C libraries**  to run.

### Instructions

**Cloning the repositories**

```shell
git clone https://github.com/Neress-dono/Tronc-Commun_42.git 
cd Tronc-Commun_42/libft
```

**2. Compiling the library**

- to compile without bonus functions.
```shell
$ make
```  
- to compile with bonuses.
```shell
$ make bonus
```


## Goals:

-   C basics
-   Standard C library
-   Generation of a static library
-	Unix logic

## Skills:

-   Imperative programming  
-   Rigor  
-   Algorithms & AI

### [Go back](https://github.com/Neress-dono/common-core_42)
