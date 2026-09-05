# LeetCode 103 - Binary Tree Zigzag Level Order Traversal

## Problem

Given the root of a binary tree, return the **zigzag level order traversal** of its nodes' values.

In normal level order traversal, nodes are visited from **left to right** at every level. In zigzag traversal, the direction changes after every level:

* First level → Left to Right
* Second level → Right to Left
* Third level → Left to Right
* And so on.

## Example 1

### Input

```text
root = [3,9,20,null,null,15,7]
```

### Output

```text
[[3],[20,9],[15,7]]
```

### Explanation

The tree is:

```text
        3
       / \
      9   20
         /  \
        15   7
```

The traversal is:

```text
Level 1: 3
Level 2: 20, 9
Level 3: 15, 7
```

Therefore, the answer is:

```text
[[3],[20,9],[15,7]]
```

## Approach

This problem can be solved using **Breadth-First Search (BFS)** with a queue.

We process the tree one level at a time. A boolean variable is used to keep track of the direction of traversal.

For every level:

1. Store all nodes of the current level.
2. If the direction is left to right, add values normally.
3. If the direction is right to left, reverse the values.
4. Add the current level to the result.
5. Change the direction for the next level.

## Algorithm

1. If the root is `None`, return an empty list.
2. Create a queue and add the root.
3. Set a flag to indicate left-to-right traversal.
4. While the queue is not empty:

   * Process all nodes in the current level.
   * Store their values.
   * Add their children to the queue.
   * Reverse the current level when required.
5. Change the traversal direction.
6. Return the result.

## Complexity

* **Time Complexity:** `O(n)`
* **Space Complexity:** `O(n)`

Each node is visited once, and the queue stores nodes that are waiting to be processed.

## LeetCode Details

**Problem Number:** 103
**Problem Name:** Binary Tree Zigzag Level Order Traversal
**Difficulty:** Medium
**Topics:** Binary Tree, Breadth-First Search, Queue

## Language

Python 3

## Author

T.Nandhini
