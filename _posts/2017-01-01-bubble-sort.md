---
layout: post
title: Bubble Sort
tags: [sorting]
---

<h3> Approach </h3>
<p> We compare every number with every other number, swapping the numbers with respect to our sort order. If we wish to sort in ascending order, when comparing we swap the left and right numbers when the left number is greater than the right number. In this fashion, the largest numbers bubble up to top. </p>


<h3> Python </h3>
```python
def bubbleSort(nums):
  for i in range(0, len(nums)):
    for j in range(i, len(nums)):
      if nums[i] > nums[j]:
        nums[i], nums[j] = nums[j], nums[i]

  return nums
```

<h3> Time Complexity </h3>
Polynomial - O(n^2)

<h3> Space Complexity </h3>
Constant - O(n)

<h3> Sample </h3>
<p> Input: [5, 7, 3, 2, 4, 6, 1] </p>
<p> Output: [1, 2, 3, 4, 5, 6, 7] </p>

|  i  |  j  |           nums          |
|:---:|:---:|:-----------------------:|
|  0  |  0  |  [5, 7, 3, 2, 4, 6, 1]  |
|  0  |  1  |  [5, 7, 3, 2, 4, 6, 1]  |
|  0  |  2  |  [3, 7, 5, 2, 4, 6, 1]  |
|  0  |  3  |  [2, 7, 5, 3, 4, 6, 1]  |
|  0  |  4  |  [2, 7, 5, 3, 4, 6, 1]  |
|  0  |  5  |  [2, 7, 5, 3, 4, 6, 1]  |
|  0  |  6  |  [1, 7, 5, 3, 4, 6, 2]  |
|  1  |  1  |  [1, 7, 5, 3, 4, 6, 2]  |
|  1  |  2  |  [1, 5, 7, 3, 4, 6, 2]  |
|  1  |  3  |  [1, 3, 7, 5, 4, 6, 2]  |
|  1  |  4  |  [1, 3, 7, 5, 4, 6, 2]  |
|  1  |  5  |  [1, 3, 7, 5, 4, 6, 2]  |
|  1  |  6  |  [1, 2, 7, 5, 4, 6, 3]  |
|  2  |  2  |  [1, 2, 7, 5, 4, 6, 3]  |
|  2  |  3  |  [1, 2, 5, 7, 4, 6, 3]  |
|  2  |  4  |  [1, 2, 4, 7, 5, 6, 3]  |
|  2  |  5  |  [1, 2, 4, 7, 5, 6, 3]  |
|  2  |  6  |  [1, 2, 3, 7, 5, 6, 4]  |
|  3  |  3  |  [1, 2, 3, 7, 5, 6, 4]  |
|  3  |  4  |  [1, 2, 3, 5, 7, 6, 4]  |
|  3  |  5  |  [1, 2, 3, 5, 7, 6, 4]  |
|  3  |  6  |  [1, 2, 3, 4, 7, 6, 5]  |
|  4  |  4  |  [1, 2, 3, 4, 7, 6, 5]  |
|  4  |  5  |  [1, 2, 3, 4, 6, 7, 5]  |
|  4  |  6  |  [1, 2, 3, 4, 5, 7, 6]  |
|  5  |  5  |  [1, 2, 3, 4, 5, 7, 6]  |
|  5  |  6  |  [1, 2, 3, 4, 5, 6, 7]  |
|  6  |  6  |  [1, 2, 3, 4, 5, 6, 7]  |