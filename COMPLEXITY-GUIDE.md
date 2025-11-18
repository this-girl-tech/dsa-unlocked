🧠 Time & Space Complexity (The Smart Way to Understand Algorithms)
===================================================================

Complexity helps you understand how an algorithm behaves as input size grows.Once you master this, solving DSA problems becomes faster, easier, and far more predictable.

This guide covers the **most important complexity concepts** you must know — with clear rules, examples, and patterns.

⭐ 1. Big-O Notation
===================

**What Big-O tells you**
------------------------

*   How **fast** your code runs
    
*   How **much memory** it uses
    
*   Whether your approach will **scale**
    

**Common Big-O Complexities**
-----------------------------


| Complexity           | Meaning                        | Examples                |
|----------------------|--------------------------------|-------------------------|
| O(1)                 | Constant                       |Array index, Hash lookup |
| O(log n)             | Shrinks input each step        | Binary search           |
| O(n)                 | Linear scan                    |  Single loop            |
| O(n log n)           | Efficient scaling              |   Merge sort            |
| O(n²)                | Double loops                   |   Matrix problems       |
| O(2ⁿ)                | All subsets                    |   Backtracking          |
| O(n!)                | All permutations               |    Permutation problems |


⭐ 2. How to Calculate Time Complexity
=====================================

**Rules**
---------

*   Ignore constants → O(2n + 10) → **O(n)**
    
*   Keep highest term → O(n² + n) → **O(n²)**
    
*   Loops define complexity
    

**Examples**
------------

### **Single Loop**

`   for (let i = 0; i < n; i++) {}  // O(n)   `

### **Nested Loops**

`   for (let i = 0; i < n; i++)    for (let j = 0; j < n; j++) {}  // O(n²)   `

### **Shrinking Input**

`   while (n > 1) n /= 2;  // O(log n)   `

⭐ 3. Understanding O(log n)
===========================

**When it appears**
-------------------

*   Binary search
    
*   Heaps
    
*   Balanced BSTs
    
*   Divide & Conquer algorithms
    

**Why it’s extremely fast**
---------------------------

`   n → n/2 → n/4 → n/8 → ... → 1    Total steps = log₂(n)   `

Even for 1,000,000, only ~20 steps.

⭐ 4. Practical Complexity Examples
==================================

**Best Possible Complexities**

*   Search in sorted array → **O(log n)**
    
*   Find max/min → **O(n)**
    
*   Sorting → **O(n log n)**
    
*   BFS/DFS → **O(V + E)**
    
*   Sliding window → **O(n)**
    
*   Subsets → **O(2ⁿ)**
    
*   Permutations → **O(n!)**
    

⭐ 5. Space Complexity
=====================

**What it measures**
--------------------

How much **extra memory** your algorithm uses.

**Common Space Costs**
----------------------

| Space                | Operation                      |           
|----------------------|--------------------------------|
| O(1)                 | Swap variables                 |
| O(n)                 | Extra array or DP table        | 
| O(n)                 | HashMap / Set                  |  
| O(h)                 | Recursion depth                |   
| O(n)                 | Merge Sort                     |   


**Example**
-----------

`   function fact(n) {    if (n === 0) return 1;    return n * fact(n - 1);  }  // SC = O(n) because recursion uses stack memory   `

⭐ 6. Time–Space Trade-Off
=========================

**Common Scenarios**
--------------------

*   Hashing → faster lookups, uses more memory
    
*   Prefix sum → O(1) queries, O(n) space
    
*   Memoization → reduces time, increases space
    

⭐ 7. Common Mistakes
====================

*   **O(n + n) = O(n²)** — Incorrect. Correct → **O(n)**
    
*   **Ignoring worst case** (e.g., QuickSort worst → O(n²))
    
*   **Forgetting recursion uses memory** — each call adds stack frame
    
*   **Counting operations instead of patterns** — analyze growth, not exact steps
    

⭐ 8. Complexity Patterns (Quick Cheatsheet)
===========================================

**Loop Patterns**
-----------------

`   for(...)            → O(n)  for inside for      → O(n²)  while(n /= 2)       → O(log n)   `

**Recursion Patterns**
----------------------

`   Divide & Conquer    → O(n log n)  Subsets             → O(2ⁿ)  Permutations        → O(n!)  Tree DFS            → O(n)   `

**Hashing**
-----------

`   Insert   → O(1)  Search   → O(1)  Delete   → O(1)   `


⭐ 9. Quick Judge Guide
=======================

**If your input size is:**

*   n ≤ 10³ → O(n²) acceptable
    
*   n ≤ 10⁵ → O(n log n) required
    
*   n ≤ 10⁶ → O(n) required
    
*   n ≥ 10⁷ → O(log n) or O(1) only
    

⭐ 10. Master Heuristics (Remember These)
========================================

*   Shrinking input → **O(log n)**
    
*   Scan all elements → **O(n)**
    
*   Sort + scan → **O(n log n)**
    
*   Two nested loops → **O(n²)**
    
*   All subsets → **O(2ⁿ)**
    
*   All permutations → **O(n!)**
    

These shortcuts help you estimate complexity instantly.

🌸 Final Note
=============

Complexity isn’t about mathematics —it’s about recognizing **how your algorithm grows** as the input becomes bigger.

Once these patterns click, evaluating efficiency becomes effortless.

Keep practicing. You’re leveling up every day. 🚀
