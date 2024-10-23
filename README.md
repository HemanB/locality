#  Locality

## Objectives

This lab focuses on locality of reference for array accesses.   It follows Section 11.3.1 of DIS.

* Understand array layout and how array access patterns affect spatial locality of reference.
* Use the `time` command to measure performance of different access patterns.
* See how improving locality reduces program runtime.
* Modify array accesses to optimize locality.

## Part 1: Timings

This lab includes two progrrams that sum a matrix:

- `sumarrayrows` accesses the columns of each row.
- `sumarraycols` accesses the rows of each column.

Build the programs using the Makefile. 
Use the linux `time` command to see how long each program takes to execute:
```bash
time ./sumarrayrows
time ./sumarraycols
```
Take note of the execution time for each program. Focus on the time labeled "user".

What explains the differences in runtime?

## Part 2: Improving locality

Now consider `sumarray3d.c`.   It sums the elements of a 3D array.

Consider how to change the loop order to reorder the accesses to speed up this program.
The source file `sumarray3dnew.c` is a copy of `sumarray3d`.c.   Modify `sumarray3dnew.c` to speed it up
without changing its function.   Build it and time the two programs to validate your solution:

```bash
time ./sumarray3d
time ./sumarray3dnew
```

## Submit

As usual, use git to fork and clone, then add, commit, and push your modified `sumarray3dnew.c`.

Answer the questions on gradescope about these programs.
