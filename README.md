# Off-by-One Error in C++ Vector Iteration

This repository demonstrates a common off-by-one error in C++ when iterating over a `std::vector`.  The code attempts to access an element beyond the valid range of the vector, leading to undefined behavior.

The `bug.cpp` file contains the erroneous code, while `bugSolution.cpp` provides a corrected version.

**The Problem:**
The original code uses `i <= vec.size()` as the loop condition.  However, vector indices are zero-based, so the valid indices range from 0 to `vec.size() - 1`. Accessing `vec[vec.size()]` results in accessing memory outside the vector's allocated space.

**The Solution:**
The corrected code uses `i < vec.size()` as the loop condition, ensuring that the loop terminates before accessing any invalid memory locations.