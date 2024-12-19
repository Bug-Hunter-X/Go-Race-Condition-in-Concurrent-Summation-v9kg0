# Go Race Condition Example
This repository demonstrates a common race condition bug in Go, where multiple goroutines concurrently access and modify a shared variable without proper synchronization.  The result is an incorrect calculation of the sum of integers.  The `bug.go` file contains the buggy code, and `bugSolution.go` provides a corrected version.

## Bug Description
The program calculates the sum of numbers from 0 to 999 using 1000 goroutines.  The race condition arises because multiple goroutines attempt to update the shared `count` variable concurrently without using appropriate locking mechanisms. This can lead to unpredictable and incorrect results, as the final sum is inconsistent across runs.