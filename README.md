 C Program: Bubble Sort Implementation

This project demonstrates how to implement the *Bubble Sort* algorithm in the C programming language.

 Description

The program:

* Declares and initializes an integer array
* Calculates the array size using sizeof
* Sorts the array in ascending order using the *Bubble Sort algorithm*
* Prints the sorted array

This example is ideal for beginners learning sorting algorithms in C.

---

 Source Code

c

#include <stdio.h>

int main() {
    
    int arr[] = {5, 2, 9, 1, 5, 6};
    int n = sizeof(arr) / sizeof(arr[0]);
    int i, j, temp;

    // Bubble Sort
    for(i = 0; i < n - 1; i++) {
        for(j = 0; j < n - i - 1; j++) {
            if(arr[j] > arr[j + 1]) {
                temp = arr[j];
                arr[j] = arr[j + 1];
                arr[j + 1] = temp;
            }
        }
    }

    // Print sorted array
    printf("Sorted array: ");
    for(i = 0; i < n; i++) {
        printf("%d ", arr[i]);
    }

    return 0;
}


---

 How to Compile and Run

 Using GCC

1. Save the file as bubble_sort.c
2. Open terminal or command prompt
3. Compile the program:


gcc bubble_sort.c -o bubble_sort


4. Run the executable:


./bubble_sort


(On Windows, use bubble_sort.exe)

---

 Sample Output


Sorted array: 1 2 5 5 6 9


---

 Concepts Covered

* Arrays in C
* Nested for loops
* Swapping values using a temporary variable
* Sorting algorithms (Bubble Sort)
* Using sizeof to calculate array length

---

 How Bubble Sort Works

1. Compare adjacent elements
2. Swap them if they are in the wrong order
3. Repeat the process for all elements
4. After each pass, the largest unsorted element moves to its correct position
5. Continue until the array is fully sorted

---

 Time Complexity

* *Best Case:* O(n) (when already sorted with optimization)
* *Average Case:* O(n²)
* *Worst Case:* O(n²)

---
