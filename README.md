0x1B. C - Sorting algorithms & Big O
C - Algorithm & Data structure
General objectives
To know at least four different sorting algorithms
To know what the Big O notation is, and how to evaluate the time complexity of an algorithm
To know how to select the best sorting algorithm for a given input
To know what stable sorting algorithm is
Resources
Sorting algorithm || Big O notation|| Sorting algorithms animations || 15 sorting algorithms in 6 minutes
General Requirements
Allowed editors: vi, vim, emacs
All files was compiled on Ubuntu 20.04 LTS using gcc, using the options -Wall -Werror -Wextra -pedantic -std=gnu89
All files end with a new line
There is a README.md file at the root of the folder of the project
The codes used the Betty style, and were checked using betty-style.pl and betty-doc.pl
Global variables were not allowed
No more than 5 functions per file
The prototypes of all functions used are included in the header file called sort.h
All header files are include guarded
A list/array does not need to be sorted if its size is less than 2. GitHub
More Info/lnstructions
Data Structure and Functions

For this project you are given the following print_array, and print_list functions:
#include <stdlib.h>
#include <stdio.h>

/**
 * print_array - Prints an array of integers
 *
 * @array: The array to be printed
 * @size: Number of elements in @array
 */
void print_array(const int *array, size_t size)
{
    size_t i;

    i = 0;
    while (array && i < size)
    {
        if (i > 0)
            printf(", ");
        printf("%d", array[i]);
        ++i;
    }
    printf("\n");
}
#include <stdio.h>
#include "sort.h"

/**
 * print_list - Prints a list of integers
 *
 * @list: The list to be printed
 */
void print_list(const listint_t *list)
{
    int i;

    i = 0;
    while (list)
    {
        if (i > 0)
            printf(", ");
        printf("%d", list->n);
        ++i;
        list = list->next;
    }
    printf("\n");
}
Our files print_array.c and print_list.c (containing the print_array and print_list functions) will be compiled with your functions during the correction.
Please declare the prototype of the functions print_array and print_list in your sort.h header file
Please use the following data structure for doubly linked list:
/**
 * struct listint_s - Doubly linked list node
 *
 * @n: Integer stored in the node
 * @prev: Pointer to the previous element of the list
 * @next: Pointer to the next element of the list
 */
typedef struct listint_s
{
    const int n;
    struct listint_s *prev;
    struct listint_s *next;
} listint_t;
Please, note this format is used for Quiz and Task questions.

O(1)
O(n)
O(n!)
n square -> O(n^2)
log(n) -> O(log(n))
n + k -> O(n+k)
… Please use the “short” notation (don’t use constants). Example: O(nk) or O(wn) should be written O(n). If an answer is required within a file, all your answers files must have a newline at the end.
Tests
Here is a quick tip to help you test your sorting algorithms with big sets of random integers: Random.org

Files & Description
S/N	Files	Description
1.	0-bubble_sort.c,
0-O	A function that sorts an array of integers in ascending order using the Bubble sort algorithm
2.	1-insertion_sort_list.c,
1-O	A function that sorts a doubly linked list of integers in ascending order using the Insertion sort algorithm
3.	2-selection_sort.c,
2-O	A function that sorts an array of integers in ascending order using the Selection sort algorithm
4.	3-quick_sort.c,
3-O	A function that sorts an array of integers in ascending order using the Quick sort algorithm
5.	100-shell_sort.c	A function that sorts an array of integers in ascending order using the Shell sort algorithm, using the Knuth sequence
6.	101-cocktail_sort_list.c,
101-O	A function that sorts a doubly linked list of integers in ascending order using the Cocktail shaker sort algorithm
7.	102-counting_sort.c,
102-O	A function that sorts an array of integers in ascending order using the Counting sort algorithm
8.	103-merge_sort.c,
103-O	A function that sorts an array of integers in ascending order using the Merge sort algorithm
9.	104-heap_sort.c,
104-O	A function that sorts an array of integers in ascending order using the Heap sort algorithm
10.	105-radix_sort.c	A function that sorts an array of integers in ascending order using the Radix sort algorithm
11.	106-bitonic_sort.c,
106-O	A function that sorts an array of integers in ascending order using the Bitonic sort algorithm
12.	107-quick_sort_hoare.c,
107-O	A function that sorts an array of integers in ascending order using the Quick sort algorithm
Folder	tests	Contains the main.c files command argv used to test run the codes
