

---

# Search-Algorithms-in-Cpp

## **Aim**

To study different searching techniques in C++ and implement programs to search for elements in an array.

## **Tools**

* GNU g++ compiler for local compilation
* Any online C++ compiler

---

## **Theory**

Searching is the process of finding a specific element in a data structure.
Two of the most commonly used searching techniques are **Linear Search** and **Binary Search**.

### **Linear Search**

* A simple method where each element of the array is checked sequentially until the desired element is found or the end of the array is reached.
* It does **not** require the array to be sorted.

### **Binary Search**

* An efficient search technique applicable only on **sorted arrays**.
* The array is repeatedly divided into two halves, and the search continues in the half that may contain the element.
* Significantly reduces the number of comparisons compared to linear search.

### **Important Points**

* Linear Search → **O(n)** time complexity
* Binary Search → **O(log n)** time complexity
* Binary Search requires a **sorted** array
* Linear Search works on both **sorted** and **unsorted** arrays

---

## **Program 1: Linear Search**

### **Logic**

A function is created to search for the element in the array.
The function iterates over all elements sequentially and returns the index if the element is found, otherwise returns `-1`.

### **Algorithm**

1. Start
2. Input the size of the array
3. Input the array elements
4. Input the element to be searched
5. Iterate through the array:

   * If element matches, return its index
   * Else continue
6. If not found, return `-1`
7. End

---

## **Program 2: Sequential Search [Linear in main()]**

### **Logic**

The search is performed directly inside the `main()` function using a loop.
A boolean flag keeps track of whether the element is found.
If found, the index is printed; otherwise, a “not found” message is displayed.

### **Algorithm**

1. Start
2. Input the number of elements
3. Input the array elements
4. Input the element to be searched
5. Initialize a flag as `false`
6. Iterate through the array:

   * If element matches, print index and set flag `true`
   * Break the loop
7. If flag remains `false`, print “Element not found”
8. End

---

## **Program 3: Binary Search**

### **Logic**

The array must be **sorted**.
Two pointers (`left` and `right`) are used to track the current search interval.
The middle element is compared with the target element, and depending on comparison, the search continues in the left or right half.

### **Algorithm**

1. Start
2. Input the number of elements
3. Input the sorted array elements
4. Input the element to be searched
5. Initialize `left = 0` and `right = size - 1`
6. While `left <= right`:

   * Calculate `mid = (left + right) / 2`
   * If `arr[mid]` matches, return index
   * If `arr[mid] < element`, search in right half (`left = mid + 1`)
   * Else search in left half (`right = mid - 1`)
7. If element not found, return `-1`
8. End

---

## **Conclusion**

**Linear** and **Binary Search** are fundamental searching techniques.

* Linear Search is simple and works on any array.
* Binary Search is more efficient for **sorted arrays**.

Understanding these methods is essential for designing efficient algorithms for data retrieval.
