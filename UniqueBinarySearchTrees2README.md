# leet-day22

# Unique Binary Search Trees II

## Problem Description

Given an integer `n`, you need to generate all the structurally unique Binary Search Trees (BSTs) that contain exactly `n` nodes with unique values from 1 to `n`. Return the answer in any order.

## Examples

Input: `n = 3`
Output:
```
[
  [1, null, 2, null, 3],
  [1, null, 3, 2],
  [2, 1, 3],
  [3, 1, null, null, 2],
  [3, 2, null, 1]
]
```

Input: `n = 1`
Output:
```
[
  [1]
]
```

## Approach

To generate all structurally unique BSTs, we can use a recursive approach. For each number `i` from `1` to `n`, we can choose it as the root of the BST and then recursively generate the left and right subtrees using the numbers before and after `i`, respectively. By combining the left and right subtrees with the root `i`, we can form the final BST.

To implement this, we create a recursive function `generate` that takes the range of numbers `[start, end]` and returns a vector of all possible BSTs that can be formed using the numbers in this range.

## Complexity Analysis

The time complexity for this approach is exponential, as there can be multiple BSTs for each number `i`, and the total number of BSTs for `n` numbers can grow exponentially with `n`.

The space complexity is also exponential, as we need to store all the possible BSTs in the result vector. The maximum number of BSTs that can be formed is related to the Catalan numbers and is also exponential.
