# interview-prep

Absolutely — here's a **crash course tailored for algorithms and data structures interviews in Python**, designed to prep you efficiently for a company like Aviator (a startup = fast-paced interviews, likely to value clean code, fast thinking, and strong fundamentals).

---

## 📘 **Core Topics You MUST Know**

Here's a breakdown by category, with Python-specific syntax and practice concepts.

---

### ✅ **1. Python Essentials for Interviews**

* **Data Structures**: `list`, `set`, `dict`, `tuple`
* **Built-ins**:

  * `sorted()`, `reversed()`
  * `heapq` for heaps
  * `collections` (`defaultdict`, `Counter`, `deque`)
  * `itertools` (`combinations`, `permutations`, `product`)
* **Idioms**:

  * List comprehensions
  * One-liners for max/min
  * Lambda functions, `key=` usage
  * Unpacking: `a, b = b, a`

---

### 🧠 **2. Big-O Complexity (Must Know)**

* **Time complexity** of common operations:

  * List indexing: `O(1)`
  * List insert/pop at end: `O(1)`
  * List insert/pop at start: `O(n)`
  * Set/Dict lookup: `O(1)` average
  * Heap push/pop: `O(log n)`
* **Know how to analyze your code** and simplify nested loops.

---

### 📚 **3. Data Structures**

#### 🔹 Arrays/Lists

* Sliding Window
* Two Pointers
* Prefix Sums

#### 🔹 Strings

* Hashing (e.g., anagrams)
* Palindromes
* String matching (KMP not often needed; know `in`, slicing tricks)

#### 🔹 Hash Maps and Sets

* Use `Counter`, `defaultdict`
* For frequency, deduplication, O(1) lookups

#### 🔹 Stack / Queue

* `stack`: use Python list
* `queue`: use `collections.deque`
* Classic problems: valid parentheses, evaluate expressions, monotonic stack

#### 🔹 Heap / Priority Queue

* Min heap: `heapq` (default)
* Max heap: push negative values or use `heapq._heapify_max()`

#### 🔹 Linked Lists

* Reverse a list
* Detect cycle (Floyd’s Tortoise and Hare)
* Merge sorted lists

#### 🔹 Trees

* Traversals: Inorder, Preorder, Postorder (recursively and iteratively)
* Binary Search Tree properties
* LCA (Lowest Common Ancestor)
* Depth, Height, Diameter
* Serialization/Deserialization

#### 🔹 Graphs

* Represent with adj list/dict
* Traversals: BFS, DFS (iterative/recursive)
* Topological sort
* Union-Find (Disjoint Set)

---

### 🔢 **4. Algorithms**

#### 🔹 Binary Search

* Standard and on rotated arrays
* Binary search on answers (e.g., min/max feasible)

#### 🔹 Sorting

* Know built-in `sorted()`
* Custom sort with `key=lambda`
* Count sort / bucket sort for frequency-based problems

#### 🔹 Recursion & Backtracking

* Classic: subsets, permutations, N-Queens
* Understand base/recursive case

#### 🔹 Dynamic Programming (DP)

* Memoization (`lru_cache`)
* Tabulation (bottom-up arrays)
* Subsets, Knapsack, LCS, LIS, House Robber, Coin Change

#### 🔹 Greedy

* Activity selection
* Scheduling
* Minimize/maximize resources

#### 🔹 Bit Manipulation

* XOR tricks (e.g., find unique)
* Masking
* `n & (n - 1)` to check/set bits

---

### ⚙️ **5. Problem-Solving Patterns**

* Two Pointers (slow/fast)
* Sliding Window
* BFS/DFS Templates
* Binary Search on Range
* Backtracking Template
* DP Table/Memo Template

---

## 🧪 Practice Strategy

* **Easy/Medium LeetCode**: 70% medium, 30% easy
* Focus areas: Arrays, Strings, Hashing, Trees, Graphs, DP
* Mock interview prep: do problems on [https://leetcode.com](https://leetcode.com), [https://binarysearch.com](https://binarysearch.com), or [https://exercism.org](https://exercism.org)

---

## 📂 Python Templates (Memorize These!)

```python
# BFS Template
from collections import deque
def bfs(start):
    queue = deque([start])
    visited = set([start])
    while queue:
        node = queue.popleft()
        for neighbor in graph[node]:
            if neighbor not in visited:
                visited.add(neighbor)
                queue.append(neighbor)

# DFS Template (recursive)
def dfs(node, visited):
    if node in visited:
        return
    visited.add(node)
    for neighbor in graph[node]:
        dfs(neighbor, visited)

# Binary Search Template
def binary_search(nums, target):
    left, right = 0, len(nums) - 1
    while left <= right:
        mid = (left + right) // 2
        if nums[mid] == target:
            return mid
        elif nums[mid] < target:
            left = mid + 1
        else:
            right = mid - 1
    return -1

# DP Memo Template
from functools import lru_cache
@lru_cache(None)
def dp(i):
    # base case
    # recurrence relation
    return result
```

---

Would you like a **cheat sheet PDF**, **custom mock interview questions**, or **sample coding rounds similar to Aviator's format**?
