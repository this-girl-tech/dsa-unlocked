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

ComplexityMeaningExamples**O(1)**ConstantArray index, Hash lookup**O(log n)**Shrinks input each stepBinary search**O(n)**Linear scanSingle loop**O(n log n)**Efficient scalingMerge sort**O(n²)**Double loopsMatrix problems**O(2ⁿ)**All subsetsBacktracking**O(n!)**All permutationsPermutation problems

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

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   for (let i = 0; i < n; i++) {}  // O(n)   `

### **Nested Loops**

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   for (let i = 0; i < n; i++)    for (let j = 0; j < n; j++) {}  // O(n²)   `

### **Shrinking Input**

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   while (n > 1) n /= 2;  // O(log n)   `

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

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   n → n/2 → n/4 → n/8 → ... → 1    Total steps = log₂(n)   `

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

OperationSpaceSwap variables**O(1)**Extra array or DP table**O(n)**HashMap / Set**O(n)**Recursion depth**O(h)**Merge Sort**O(n)**

**Example**
-----------

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   function fact(n) {    if (n === 0) return 1;    return n * fact(n - 1);  }  // SC = O(n) because recursion uses stack memory   `

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

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   for(...)            → O(n)  for inside for      → O(n²)  while(n /= 2)       → O(log n)   `

**Recursion Patterns**
----------------------

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   Divide & Conquer    → O(n log n)  Subsets             → O(2ⁿ)  Permutations        → O(n!)  Tree DFS            → O(n)   `

**Hashing**
-----------

Plain textANTLR4BashCC#CSSCoffeeScriptCMakeDartDjangoDockerEJSErlangGitGoGraphQLGroovyHTMLJavaJavaScriptJSONJSXKotlinLaTeXLessLuaMakefileMarkdownMATLABMarkupObjective-CPerlPHPPowerShell.propertiesProtocol BuffersPythonRRubySass (Sass)Sass (Scss)SchemeSQLShellSwiftSVGTSXTypeScriptWebAssemblyYAMLXML`   Insert   → O(1)  Search   → O(1)  Delete   → O(1)   `

⭐ 9. Sorting Algorithms Overview
================================

AlgorithmTimeSpaceNotesBubble SortO(n²)O(1)Very slowSelection SortO(n²)O(1)Always n²Insertion SortO(n²)O(1)Best case O(n)Merge SortO(n log n)O(n)StableQuick SortO(n log n)O(log n)Fast averageHeap SortO(n log n)O(1)Space-efficient

⭐ 10. Quick Judge Guide
=======================

**If your input size is:**

*   n ≤ 10³ → O(n²) acceptable
    
*   n ≤ 10⁵ → O(n log n) required
    
*   n ≤ 10⁶ → O(n) required
    
*   n ≥ 10⁷ → O(log n) or O(1) only
    

⭐ 11. Master Heuristics (Remember These)
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
