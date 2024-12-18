# Assembly Memory Access Violation

This repository demonstrates a common error in assembly programming: accessing memory outside the allocated space. The bug is caused by an unexpectedly large value in the `ecx` register when calculating a memory address using array indexing.

## Bug Description

The `bug.asm` file contains assembly code that attempts to access an element in an array. However, if the index stored in `ecx` exceeds the array bounds, it will cause a memory access violation.  This can lead to program crashes or unpredictable behavior.

## Solution

The `bugSolution.asm` file provides a corrected version of the code.  It includes bounds checking to ensure that the index `ecx` is within the valid range before accessing the array element.