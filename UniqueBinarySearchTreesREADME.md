# leet-day22

# Readme: Count Unique Binary Search Trees

## Problem Description

Given an integer `n`, you are required to find the number of structurally unique Binary Search Trees (BSTs) that have exactly `n` nodes with unique values from 1 to `n`.

A Binary Search Tree (BST) is a binary tree where each node has a unique value, and for every node:

- All values in the left subtree are less than the node's value.
- All values in the right subtree are greater than the node's value.

## Example

### Input
```
n = 3
```

### Output
```
5
```

## Constraints

- 1 <= n <= 19

## Approach and Complexity

The problem can be solved using the concept of Catalan numbers. The `n-th` Catalan number represents the number of structurally unique BSTs with `n` nodes. The formula for calculating the `n-th` Catalan number is:

```
C(n) = (2n)! / ((n+1)! * n!)
```

To calculate this efficiently, we can use the formula to compute the `n-th` Catalan number in linear time, i.e., O(n).

### Algorithm

1. Initialize a variable `catalan` to 1.
2. Iterate from 0 to `n-1`, and in each iteration, update `catalan` as follows:
   ```
   catalan = catalan * (2 * (2 * i + 1)) / (i + 2)
   ```
3. Return the final value of `catalan`.

### Complexity Analysis

The time complexity of this approach is O(n) since it iterates from 0 to `n-1` and performs a constant number of operations in each iteration. The space complexity is O(1) as it only uses a constant amount of extra space.

## Summary

The given problem can be efficiently solved by calculating the `n-th` Catalan number using the formula, which allows us to find the number of structurally unique BSTs with `n` nodes. The solution has a time complexity of O(n) and a space complexity of O(1), making it an optimal solution for the given constraints.
