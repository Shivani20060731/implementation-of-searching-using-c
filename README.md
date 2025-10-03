# implementation-of-searching-using-c
Implementation of Searching in C++

Aim

To explore and implement searching algorithms in C++ and understand their working principles, efficiency, and use cases.

Software Used

MinGW C/C++ Compiler

Visual Studio Code (VS Code)

Online C++ Compiler

Theory of Searching

Searching is the process of finding the location of a target element within a collection of data. Efficient searching is crucial for quick data retrieval in real-world applications such as databases, file systems, and information retrieval.

There are two fundamental searching approaches:

1. Linear Search (Sequential Search) – checks every element one by one.


2. Binary Search (Divide and Conquer Search) – repeatedly halves the search range in a sorted dataset.

Both methods have their advantages and trade-offs, making them suitable for different scenarios.

1. Binary Search

Explanation of Code

Binary Search is a divide-and-conquer algorithm that works only on sorted arrays.

The search range is repeatedly halved by comparing the middle element with the target.

If the middle element is equal to the target → search is successful.

If the target is smaller → continue search in the left half.

If the target is larger → continue search in the right half.

Process repeats until the element is found or the search range becomes empty.


Advantages

Extremely efficient for large datasets.

Logarithmic complexity.


Limitations

Requires sorted data.

Not suitable for unsorted datasets without preprocessing.


Complexity

Time Complexity: O(log n)

Space Complexity: O(1) (iterative)

Deterministic: Always finds element if present.


Algorithm (Iterative Binary Search)

1. Start.


2. Input number of elements and store in an array/vector.


3. Sort the array in ascending order.


4. Input the target element.


5. Initialize:

start = 0

end = n-1



6. While start ≤ end:

Compute mid = (start + end) / 2.

If arr[mid] == target, return index.

Else if arr[mid] > target, set end = mid - 1.

Else set start = mid + 1.



7. If loop ends without match → element not found.


8. Stop.

2. Linear Search

Explanation of Code

Linear Search checks each element sequentially until a match is found or the list ends.

Works on both sorted and unsorted datasets.

If match found → return index.

If end reached with no match → return -1.


Advantages

Simple and easy to implement.

Works without sorting.


Limitations

Inefficient for large datasets.

Requires O(n) comparisons in the worst case.


Complexity

Time Complexity:

Best case → O(1) (element found at start).

Average/Worst case → O(n).


Space Complexity: O(1).

Stable: Preserves order of elements.


Algorithm (Linear Search)

1. Start.


2. Input array elements.


3. Input target element.


4. For each element from index i = 0 to n-1:

If arr[i] == target, return index.
5. If no match found, return -1.
6. Stop.

Comparison of Binary and Linear Search

Feature	Linear Search	Binary Search

Dataset	Works on unsorted/sorted	Works only on sorted data
Time Complexity	O(n)	O(log n)
Best Case	O(1)	O(1)
Worst Case	O(n)	O(log n)
Implementation	Simple	Slightly more complex
Efficiency	Poor for large datasets	Very efficient for large datasets

Conclusion

This experiment demonstrated two fundamental searching algorithms:

1. Binary Search

Very efficient with logarithmic complexity.

Ideal for large, sorted datasets.

Faster but requires preprocessing (sorting).

2. Linear Search

Simple, requires no sorting.

Suitable for small or unsorted datasets.

Slower for large datasets.
