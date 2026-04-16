# 2D Array Access in C++ (Pointer vs Indexing)

## Overview

This program demonstrates two ways of accessing elements in a 2D array in C++:

* **Pointer notation**: `*(*(arr + i) + j)`
* **Array indexing**: `arr[i][j]`

Both approaches produce the same result, showing how arrays and pointers are closely related in memory.

---

##  Concepts Covered

* 2D arrays in C++
* Pointer arithmetic
* Nested loops
* Memory access techniques

---

##  Code Explanation

### Array Initialization

```cpp
const int ROW = 3;
const int COL = 4;

int arr[ROW][COL] = {
    {1, 2, 3, 4},
    {5, 6, 7, 8},
    {9, 10, 11, 12}
};
```

This creates a **3 × 4 matrix** stored in contiguous memory.

---

###  Method 1: Pointer Notation

```cpp
*(*(arr + i) + j)
```

Step-by-step:

* `arr + i` → moves to the i-th row
* `*(arr + i)` → accesses that row
* `*( *(arr + i) + j )` → accesses the j-th element in the row

---

###  Method 2: Array Indexing

```cpp
arr[i][j]
```

This is the standard and most readable way to access elements.

---

##  How to Compile and Run

### Using g++:

```bash
g++ program.cpp -o program
./program


##  Expected Output

 *( *(arr+i)+j ) 
   1   2   3   4
   5   6   7   8
   9  10  11  12

 arr[i][j] 
   1   2   3   4
   5   6   7   8
   9  10  11  12

