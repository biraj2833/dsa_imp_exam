# Dsa_imp_exam

### 1️⃣ WHAT IS DSA AND WHY DO WE NEED DSA? (5 MARKS)

## 🔹 Concept

Data Structures and Algorithms (DSA) is a discipline that focuses on organizing data efficiently and solving problems using well-defined step-by-step procedures.

## 🔹 Key Points

• Data Structures define how data is stored

• Algorithms define how problems are solved

• Together they improve efficiency

## 🔹 Need of DSA

• Efficient data handling

• Better time and space utilization

• Handling large datasets

• Building optimized software systems

---
## Types of Data Structures and Basic Operations Performed on Data Structures

![Image](https://i.pinimg.com/736x/74/8b/ad/748bade7cc70b81894dbb8b65257742b.jpg)

![Image](https://www.scaler.com/topics/images/data-structure-operations-thumbnail.webp)

![Image](https://miro.medium.com/1%2AUdSKw8FJazsFcGaeo5hxgA%402x.jpeg)

### 🔹 What is a Data Structure?

A **Data Structure (DS)** is a way of **organizing, storing, and managing data** in memory so that it can be accessed and modified efficiently.

---

## 🔹 Types of Data Structures

Data structures are mainly classified into **two types**:

---

### 1️⃣ Linear Data Structures

In linear data structures, data elements are arranged **sequentially** (one after another).

**Examples:**

* Array
* Stack
* Queue
* Linked List

**Characteristics:**

* Single level structure
* Easy to traverse
* Memory is accessed sequentially

---

### 2️⃣ Non-Linear Data Structures

In non-linear data structures, data elements are arranged in a **hierarchical or network form**.

**Examples:**

* Tree
* Graph

**Characteristics:**

* Multi-level structure
* Complex relationships
* Faster searching in many cases

---

### 🔹 Classification Summary

| Type       | Examples                         |
| ---------- | -------------------------------- |
| Linear     | Array, Stack, Queue, Linked List |
| Non-Linear | Tree, Graph                      |

---

## 🔹 Basic Operations Performed on Data Structures

The following are the **basic operations** commonly performed on any data structure:

---

### 1️⃣ Insertion

* Adding a new element into the data structure
* Can be done at beginning, end, or any position

**Example:**
Inserting an element into an array or linked list

---

### 2️⃣ Deletion

* Removing an element from the data structure
* Requires shifting or relinking elements

**Example:**
Deleting an element from stack (POP)

---

### 3️⃣ Traversal

* Visiting each element of the data structure **exactly once**

**Example:**
Traversing an array or tree traversal (inorder, preorder)

---

### 4️⃣ Searching

* Finding the location of a particular element

**Example:**
Linear search, Binary search

---

### 5️⃣ Sorting

* Arranging data elements in **ascending or descending order**

**Example:**
Bubble sort, Insertion sort

---

### 6️⃣ Merging

* Combining two similar data structures into one

**Example:**
Merging two arrays

---

## 🔹 Importance of Data Structures

* Efficient data management
* Faster processing
* Optimized memory usage
* Essential for large-scale applications

---

## 🔹 Conclusion (Exam-Ready)

Data structures are classified into **linear and non-linear types**, each serving different purposes. Basic operations like **insertion, deletion, traversal, searching, sorting, and merging** are essential for manipulating data efficiently in any data structure.
---

2️⃣ WHAT IS AN ARRAY? EXPLAIN ITS TYPES (5 MARKS)

### 🔹 Concept

An array is a linear data structure used to store multiple elements of the same data type in contiguous memory locations.

### 🔹 Types of Array

• One Dimensional Array.

• Two Dimensional Array.

• Multi Dimensional Array.

### 🔹 Use Case

• Storing lists of values

• Matrix representation

• Used in sorting and searching

---

3️⃣ APPLICATIONS OF ARRAY (5 MARKS)

<img width="1478" height="694" alt="image" src="https://github.com/user-attachments/assets/6b1719f1-816f-4b4e-8e83-c6e49ae3c20d" />

### 🔹 Applications

• Used to store large amounts of data

• Used in image and signal processing

• Used for implementing other data structures

• Used in numerical computations

• Used in database indexing

## SPARSE MATRIX & SPARSE MATRIX REPRESENTATION


## 🔹 What is a Sparse Matrix?

A **Sparse Matrix** is a matrix in which the **number of zero elements is much greater than the number of non-zero elements**.

In general, a matrix is considered **sparse** if:

• Number of zero elements > Number of non-zero elements


### 📌 Example of Sparse Matrix

Matrix A (4 × 4):
```c
0  0  5  0
0  0  0  0
0  8  0  0
0  0  0  6
```

Here, most elements are **0**, so this is a **sparse matrix**.


## 🔹 Why Sparse Matrix is Needed?

Storing all elements of a sparse matrix using a normal 2D array is **inefficient**.

Problems with normal storage:
• Wastes memory storing zeros
• Slower processing
• Inefficient for large matrices

Solution:
➡️ Store **only non-zero elements** using **Sparse Matrix Representation**

## 🔹 Sparse Matrix Representation

Sparse matrix representation stores **only meaningful (non-zero) values** along with their **row and column indices**.


## 🔹 Common Sparse Matrix Representations

## 1️⃣ Triplet Representation (Most Important for Exams)

This is the **most commonly used and exam-oriented method**.

### Structure of Triplet Representation

Each row stores:
• Row index
• Column index
• Value

First row stores:
• Total number of rows
• Total number of columns
• Total number of non-zero elements

### 📌 Example

Original Matrix (4 × 4):
```c
0  0  5  0
0  0  0  0
0  8  0  0
0  0  0  6
```
Non-zero elements:
• 5 at (0,2)
• 8 at (2,1)
• 6 at (3,3)

### Triplet Form

| Row | Column | Value |
| --- | ------ | ----- |
| 4   | 4      | 3     |
| 0   | 2      | 5     |
| 2   | 1      | 8     |
| 3   | 3      | 6     |

Explanation:
• First row → Matrix size and non-zero count
• Remaining rows → Actual data

## 🔹 Advantages of Triplet Representation

• Saves memory
• Easy to implement
• Efficient for sparse data
• Reduces storage from O(m×n) to O(k), where k = non-zero elements

## 🔹 Disadvantages of Triplet Representation

• Slower access compared to array
• Searching an element takes more time
• Not suitable for frequent random access

## 2️⃣ Linked List Representation (Brief)

• Each non-zero element is stored as a node
• Node contains:
– Row index
– Column index
– Value
– Link to next node

Used when:
• Dynamic insertion/deletion is required

## 🔹 Comparison: Normal Matrix vs Sparse Matrix

| Feature    | Normal Matrix              | Sparse Matrix                 |
| ---------- | -------------------------- | ----------------------------- |
| Storage    | Stores all elements        | Stores only non-zero elements |
| Memory     | High                       | Low                           |
| Efficiency | Poor for large sparse data | High                          |
| Use case   | Dense matrices             | Large sparse matrices         |


## 🔹 Applications of Sparse Matrix

• Graph representation (Adjacency Matrix)
• Scientific computing
• Image processing
• Machine learning
• Network routing
• Big data applications

---

## 🔹 One-Line Exam Answer (Very Important)

> A sparse matrix is a matrix with a large number of zero elements, and it is efficiently represented by storing only non-zero elements using methods like triplet representation.

---

4️⃣ STACK – PUSH & POP OPERATIONS (10 MARKS)
## STACK – PUSH & POP OPERATIONS (Algorithms)

![Image](https://www.tutorialspoint.com/data_structures_algorithms/images/stack_representation.jpg)

![Image](https://homework.study.com/cimages/multimages/16/stack_push_operation2294814496370743228.jpg)

![Image](https://study.com/cimages/videopreview/videopreview-full/l656peepfd.jpg)

A **stack** is a **linear data structure** that follows the principle **LIFO (Last In, First Out)**.
Two fundamental operations are **PUSH** (insert) and **POP** (delete).


## 🔹 PUSH Operation (Insert an Element)

### **Algorithm: PUSH(STACK, TOP, MAX, ITEM)**

**Step 1:** If `TOP == MAX − 1`
→ Display **“Stack Overflow”** and **STOP**

**Step 2:** `TOP = TOP + 1`

**Step 3:** `STACK[TOP] = ITEM`

**Step 4:** **STOP**


## 🔹 POP Operation (Delete an Element)

### **Algorithm: POP(STACK, TOP)**

**Step 1:** If `TOP == −1`
→ Display **“Stack Underflow”** and **STOP**

**Step 2:** `ITEM = STACK[TOP]`

**Step 3:** `TOP = TOP − 1`

**Step 4:** Return `ITEM`

**Step 5:** **STOP**

---

## 🔹 Initialization

```text
TOP = -1
```

## 🔹 Conditions Summary

| Condition        | Meaning        |
| ---------------- | -------------- |
| `TOP == -1`      | Stack is EMPTY |
| `TOP == MAX - 1` | Stack is FULL  |


## 🔹 Example

### PUSH 10, 20, 30

```
TOP → 2
Stack: [10, 20, 30]
```

### POP

```
Removed Element: 30
TOP → 1
Stack: [10, 20]
```


## 🔹 Key Points

* PUSH adds an element at the **top**
* POP removes the **topmost** element
* Both operations take **O(1)** time complexity

---

5️⃣ QUEUE – ENQUEUE & DEQUEUE OPERATIONS (10 MARKS)

## INSERTION IN DOUBLE ENDED QUEUE (DEQUE) – ALGORITHM

![Image](https://miro.medium.com/v2/resize%3Afit%3A1400/1%2AQyQG0uBovPZH9xzYEx_bMQ.png)

![Image](https://miro.medium.com/1%2AtuT-pn42vOOU2uNbyGiqzg.png)

![Image](https://cdn.programiz.com/sites/tutorial2program/files/deque-insert-front-2.png)

A **Double Ended Queue (DEQUE)** is a linear data structure in which **insertion and deletion can be performed at both ends** (front and rear).

There are **two insertion operations**:

* **Insert at Front**
* **Insert at Rear**


## 🔹 Initial Conditions

```text
FRONT = -1
REAR  = -1
```



## 🔹 Algorithm 1: INSERT_AT_FRONT(DEQUE, FRONT, REAR, MAX, ITEM)

**Step 1:** If `FRONT == 0`
→ Display **“Overflow at Front”** and **STOP**

**Step 2:** If `FRONT == -1`

* Set `FRONT = 0`
* Set `REAR = 0`

**Step 3:** Else

* `FRONT = FRONT − 1`

**Step 4:** `DEQUE[FRONT] = ITEM`

**Step 5:** **STOP**



## 🔹 Algorithm 2: INSERT_AT_REAR(DEQUE, FRONT, REAR, MAX, ITEM)

**Step 1:** If `REAR == MAX − 1`
→ Display **“Overflow at Rear”** and **STOP**

**Step 2:** If `FRONT == -1`

* Set `FRONT = 0`
* Set `REAR = 0`

**Step 3:** Else

* `REAR = REAR + 1`

**Step 4:** `DEQUE[REAR] = ITEM`

**Step 5:** **STOP**



## 🔹 Conditions Summary

| Condition         | Meaning                      |
| ----------------- | ---------------------------- |
| `FRONT == -1`     | DEQUE is EMPTY               |
| `FRONT == 0`      | Front insertion not possible |
| `REAR == MAX - 1` | Rear insertion not possible  |


## 🔹 Example

### Insert at Rear: 10, 20

```text
DEQUE: [10, 20]
FRONT → 0
REAR  → 1
```

### Insert at Front: 5

```text
DEQUE: [5, 10, 20]
FRONT → 0
REAR  → 2
```

## 🔹 Time Complexity

* **O(1)** for both front and rear insertion

---

## DELETE SECOND LAST ELEMENT FROM A QUEUE (Algorithm)

![Image](https://www.tutorialride.com/images/data-structures/queue-array.jpeg)

![Image](https://he-s3.s3.amazonaws.com/media/uploads/cf1e1c1.png)

![Image](https://jenkov.com/images/java-collections/java-queue.png)

In a **queue (FIFO)**, deletion is normally done only from the **front**.
To delete the **second last element**, we must **traverse the queue** and adjust elements manually.

Assume the queue is implemented using an **array**.

---

## 🔹 Given

* Queue `Q[ ]`
* `FRONT`, `REAR`
* Second last element is at index `REAR − 1`

---

## 🔹 Algorithm: DELETE_SECOND_LAST(Q, FRONT, REAR)

### **Step 1:**

If `FRONT == -1` OR `FRONT == REAR`
→ Display **“Deletion not possible”** (queue empty or only one element)
→ **STOP**

---

### **Step 2:**

If `(REAR - FRONT + 1) < 2`
→ Display **“Second last element does not exist”**
→ **STOP**

---

### **Step 3:**

Set `POS = REAR − 1`   *(index of second last element)*

---

### **Step 4:**

For `i = POS` to `REAR − 1`
→ `Q[i] = Q[i + 1]`

---

### **Step 5:**

`REAR = REAR − 1`

---

### **Step 6:**

**STOP**

---

## 🔹 Example

### Initial Queue

```text
FRONT → 0
REAR  → 4
Queue: [10, 20, 30, 40, 50]
```

### Delete Second Last Element (`40`)

```text
Queue: [10, 20, 30, 50]
FRONT → 0
REAR  → 3
```


### ✔️ One-line Exam Answer

> To delete the second last element from a queue, shift elements after index `REAR−1` to the left and decrement `REAR` by one.

---

If you want:

* **C program**
* **Linked-list queue version**
* **Diagram-only explanation**
* **Circular queue version**

Just tell me 👍


---

6️⃣ SINGLY LINKED LIST – INSERT AT ANY POSITION (10 MARKS)

## SINGLY LINKED LIST – INSERT AT ANY POSITION (Algorithm)

![Image](https://image.slidesharecdn.com/insertioninsinglylinkedlist-170509164604/75/Insertion-in-singly-linked-list-1-2048.jpg)

![Image](https://www.alphacodingskills.com/imgfiles/linked-list-insertat.PNG)

![Image](https://favtutor.com/resources/images/uploads/Linked_list_data_structure_nodes.jpg)

![Image](https://miro.medium.com/0%2AchiZd2LxZXoXWL52.jpg)

A **singly linked list** consists of nodes where each node contains:

* **DATA**
* **LINK** (address of next node)

Insertion at **any position** means inserting a new node:

* At the **beginning**
* At the **end**
* Or at a **given position (middle)**


## 🔹 Algorithm: INSERT_AT_POSITION(START, ITEM, POS)

### **Step 1:** Create a new node `NEW`

### **Step 2:** Set

`NEW → DATA = ITEM`

### **Step 3:** If `POS == 1`

* `NEW → LINK = START`
* `START = NEW`
* **STOP**


### **Step 4:** Set

`PTR = START`
`COUNT = 1`

### **Step 5:** While `COUNT < POS − 1` AND `PTR != NULL`

* `PTR = PTR → LINK`
* `COUNT = COUNT + 1`


### **Step 6:** If `PTR == NULL`

→ Display **“Invalid Position”** and **STOP**


### **Step 7:**

`NEW → LINK = PTR → LINK`
`PTR → LINK = NEW`


### **Step 8:** **STOP**

## 🔹 Example

### Initial List

```text
10 → 20 → 40 → NULL
```

### Insert `30` at position `3`

```text
10 → 20 → 30 → 40 → NULL
```

## 🔹 Key Points

* Position starts from **1**
* Traversal is required to reach `(POS − 1)` node
* Time Complexity:

  * **O(1)** → insertion at beginning
  * **O(n)** → insertion at any position


---


7️⃣ BINARY SEARCH TREE – INSERT OPERATION (10 MARKS)

## BINARY SEARCH TREE – INSERT OPERATION (Algorithm)

![Image](https://courses.grainger.illinois.edu/cs225/sp2019/assets/notes/bst/insert.png)

![Image](https://www.log2base2.com/images/ds/bst-insert-demo.svg)

A **Binary Search Tree (BST)** is a binary tree in which, for every node:

* Left subtree contains values **less than** the node
* Right subtree contains values **greater than** the node
  *(No duplicate keys, in standard BST)*



## 🔹 Algorithm: BST_INSERT(ROOT, ITEM)

### **Step 1:** Create a new node `NEW`

### **Step 2:**

`NEW → DATA = ITEM`
`NEW → LEFT = NULL`
`NEW → RIGHT = NULL`



### **Step 3:** If `ROOT == NULL`

* `ROOT = NEW`
* **STOP**

### **Step 4:** Set

`PTR = ROOT`
`PARENT = NULL`


### **Step 5:** While `PTR != NULL`

* Set `PARENT = PTR`

* If `ITEM < PTR → DATA`
  → `PTR = PTR → LEFT`

* Else if `ITEM > PTR → DATA`
  → `PTR = PTR → RIGHT`

* Else
  → Display **“Duplicate value not allowed”** and **STOP**



### **Step 6:** If `ITEM < PARENT → DATA`

→ `PARENT → LEFT = NEW`
Else
→ `PARENT → RIGHT = NEW`


### **Step 7:** **STOP**

## 🔹 Example

### Insert: `50, 30, 70, 20, 40, 60`

```text id="8e2zv7"
        50
       /  \
     30    70
    / \    /
  20  40  60
```
---
## BINARY SEARCH TREE – DELETE OPERATION (Algorithm)

![Image](https://baoqger.github.io/images/twochildren-delete-after.png)

![Image](https://courses.grainger.illinois.edu/cs225/sp2019/assets/notes/bst/remove2child.png)

![Image](https://tutorialhorizon.com/static/media/algorithms/2014/12/Inorder-Predecessor-and-Successor-in-Binary-Search-Tree.jpg)

![Image](https://scaler.com/topics/images/bst-gif.gif)

Deletion in a **Binary Search Tree (BST)** means **removing a node** while **maintaining the BST property**:

* Left subtree < Root
* Right subtree > Root

---

## 🔹 Cases of Deletion in BST

Deletion depends on the **number of children** of the node to be deleted.

### **Case 1: Node with NO child (Leaf Node)**

* Simply remove the node
* Set parent link to `NULL`

---

### **Case 2: Node with ONE child**

* Replace the node with its child
* Link parent directly to the child

---

### **Case 3: Node with TWO children**

* Find **Inorder Successor** (smallest element in right subtree)
  **OR**
* Find **Inorder Predecessor** (largest element in left subtree)
* Replace node’s data with successor/predecessor
* Delete the successor/predecessor node

---

## 🔹 Algorithm: BST_DELETE(ROOT, ITEM)

### **Step 1:** If `ROOT == NULL`

→ Display **“Tree is empty”** and **STOP**

---

### **Step 2:** If `ITEM < ROOT → DATA`

→ `ROOT → LEFT = BST_DELETE(ROOT → LEFT, ITEM)`

---

### **Step 3:** Else if `ITEM > ROOT → DATA`

→ `ROOT → RIGHT = BST_DELETE(ROOT → RIGHT, ITEM)`

---

### **Step 4:** Else

(Node to be deleted found)

#### a) If `ROOT → LEFT == NULL` AND `ROOT → RIGHT == NULL`

* `free(ROOT)`
* Return `NULL`

#### b) If `ROOT → LEFT == NULL`

* `TEMP = ROOT → RIGHT`
* `free(ROOT)`
* Return `TEMP`

#### c) If `ROOT → RIGHT == NULL`

* `TEMP = ROOT → LEFT`
* `free(ROOT)`
* Return `TEMP`

#### d) If `ROOT` has TWO children

* Find **Inorder Successor**
* Copy successor value to `ROOT`
* Delete successor recursively

---

### **Step 5:** Return `ROOT`

---

## 🔹 Example

### Initial BST

```text
        50
       /  \
     30    70
    / \    /
  20  40  60
```

### Delete Node `30`

```text
        50
       /  \
     40    70
    /      /
  20      60
```

---

## 🔹 Time Complexity

| Case         | Complexity   |
| ------------ | ------------ |
| Balanced BST | **O(log n)** |
| Skewed BST   | **O(n)**     |

---

8️⃣ BINARY TREE TRAVERSALS (INORDER, PREORDER, POSTORDER) (10 MARKS)

## BINARY TREE TRAVERSALS

### (INORDER, PREORDER, POSTORDER)

![Image](https://miro.medium.com/1%2AcxXPgxw5imaniGnNScef5g.jpeg)

![Image](https://raw.githubusercontent.com/Codecademy/docs/main/media/binary-tree-labeled.png)

![Image](https://iq.opengenus.org/content/images/2019/07/treetraversal-1.png)

![Image](https://cs-people.bu.edu/tvashwin/cs112_spring09/lab06_files/tree_example.png)

**Tree traversal** is the process of visiting **each node exactly once** in a binary tree in a specific order.



## 🔹 Types of Binary Tree Traversals

| Traversal | Order               | Short Form |
| --------- | ------------------- | ---------- |
| Inorder   | Left → Root → Right | **LNR**    |
| Preorder  | Root → Left → Right | **NLR**    |
| Postorder | Left → Right → Root | **LRN**    |


## 🔹 Example Binary Tree

```text id="trvex1"
        A
       / \
      B   C
     / \   \
    D   E   F
```



## 🔹 INORDER Traversal (LNR)

### **Algorithm: INORDER(TREE)**

1. If `TREE != NULL`
2. INORDER(`TREE → LEFT`)
3. Visit `TREE → DATA`
4. INORDER(`TREE → RIGHT`)

### **Output**

```text id="inord1"
D  B  E  A  C  F
```

### **Use**

* Produces **sorted order** in a BST


## 🔹 PREORDER Traversal (NLR)

### **Algorithm: PREORDER(TREE)**

1. If `TREE != NULL`
2. Visit `TREE → DATA`
3. PREORDER(`TREE → LEFT`)
4. PREORDER(`TREE → RIGHT`)

### **Output**

```text id="preord1"
A  B  D  E  C  F
```

### **Use**

* Used to **copy a tree**
* Used in **prefix expressions**



## 🔹 POSTORDER Traversal (LRN)

### **Algorithm: POSTORDER(TREE)**

1. If `TREE != NULL`
2. POSTORDER(`TREE → LEFT`)
3. POSTORDER(`TREE → RIGHT`)
4. Visit `TREE → DATA`

### **Output**

```text id="postord1"
D  E  B  F  C  A
```

### **Use**

* Used to **delete a tree**
* Used in **postfix expressions**


## 🔹 Time & Space Complexity

| Traversal | Time     | Space (Recursion) |
| --------- | -------- | ----------------- |
| All       | **O(n)** | **O(h)**          |

`n` = number of nodes
`h` = height of tree

---

9️⃣ INSERTION SORT (10 MARKS)

## INSERTION SORT (Algorithm)

![Image](https://miro.medium.com/1%2A_NOe6jL9veyR4yAyf85dzA.png)

![Image](https://images.openai.com/static-rsc-3/RYIhNF6QS1qWDCecTjbPT76Jurhp35r0IiSadx44fNfnHsg4ppSC3sBbUydZUTTXOLnkStt9PajQ-bPb9cMIrX7D5ogiByVfZnVQn3qwg4U?purpose=fullsize\&v=1)

![Image](https://he-s3.s3.amazonaws.com/media/uploads/46bfac9.png)

![Image](https://www.opentechguides.com/images/howto/howto_5001.png)

**Insertion Sort** is a **comparison-based sorting algorithm** that works the way we sort **playing cards in hand**—one element at a time, inserting each into its correct position in the already sorted part.


## 🔹 Algorithm: INSERTION_SORT(A, N)

**Step 1:** For `i = 1` to `N − 1`

**Step 2:**
`KEY = A[i]`
`j = i − 1`

**Step 3:** While `j ≥ 0` AND `A[j] > KEY`

* `A[j + 1] = A[j]`
* `j = j − 1`

**Step 4:**
`A[j + 1] = KEY`

**Step 5:** Repeat until array is sorted

**Step 6:** **STOP**


## 🔹 Example

### Initial Array

```text id="ins1"
8   3   5   2
```

### Pass-wise Sorting

```text id="ins2"
Pass 1: 3   8   5   2
Pass 2: 3   5   8   2
Pass 3: 2   3   5   8
```



## 🔹 Key Characteristics

| Property     | Value            |
| ------------ | ---------------- |
| Sorting Type | Comparison-based |
| Technique    | Insertion        |
| Stable       | ✅ Yes            |
| In-place     | ✅ Yes            |
| Adaptive     | ✅ Yes            |



## 🔹 Time Complexity

| Case                   | Complexity |
| ---------------------- | ---------- |
| Best (Already sorted)  | **O(n)**   |
| Average                | **O(n²)**  |
| Worst (Reverse sorted) | **O(n²)**  |



## 🔹 Space Complexity

* **O(1)** (No extra memory used)



## 🔹 Advantages

* Simple and easy to implement
* Efficient for **small datasets**
* Works well for **nearly sorted arrays**


## 🔹 Disadvantages

* Slow for large datasets
* Not suitable for large-scale applications

---
 
🔟 QUICK SORT (10 MARKS)

## QUICK SORT (Algorithm)

![Image](https://miro.medium.com/1%2ADtH6fEdBhoUGnjBWudJ8pA.png)

![Image](https://runestone.academy/ns/books/published/pythonds/_images/partitionA.png)

![Image](https://s3.amazonaws.com/hr-challenge-images/quick-sort/RecursionTree.png)

![Image](https://cdn-images-1.medium.com/max/1080/1%2A-Ew3z7-bu0gjNXKL6plLzA.jpeg)

**Quick Sort** is a **divide-and-conquer sorting algorithm**. It selects a **pivot** element and partitions the array such that:

* Elements **smaller than pivot** are on the left
* Elements **greater than pivot** are on the right
  The process is then recursively applied to the subarrays.



## 🔹 Algorithm: QUICK_SORT(A, LOW, HIGH)

### **Step 1:** If `LOW < HIGH`

### **Step 2:**

`P = PARTITION(A, LOW, HIGH)`

### **Step 3:**

`QUICK_SORT(A, LOW, P − 1)`
`QUICK_SORT(A, P + 1, HIGH)`

### **Step 4:** **STOP**



## 🔹 Algorithm: PARTITION(A, LOW, HIGH)

*(Using last element as Pivot)*

**Step 1:**
`PIVOT = A[HIGH]`
`i = LOW − 1`

**Step 2:** For `j = LOW` to `HIGH − 1`

* If `A[j] < PIVOT`

  * `i = i + 1`
  * Swap `A[i]` and `A[j]`

**Step 3:**
Swap `A[i + 1]` and `A[HIGH]`

**Step 4:**
Return `i + 1`



## 🔹 Example

### Initial Array

```text id="qs1"
10   7   8   9   1   5
```

### Pivot = 5

```text id="qs2"
After partition → 1   5   8   9   10   7
Pivot index = 1
```

### Final Sorted Array

```text id="qs3"
1   5   7   8   9   10
```


## 🔹 Time Complexity

| Case    | Complexity     |
| ------- | -------------- |
| Best    | **O(n log n)** |
| Average | **O(n log n)** |
| Worst   | **O(n²)**      |


## 🔹 Space Complexity

* **O(log n)** (recursive stack, average case)


## 🔹 Key Characteristics

| Property         | Value            |
| ---------------- | ---------------- |
| Technique        | Divide & Conquer |
| In-place         | ✅ Yes            |
| Stable           | ❌ No             |
| Fast in practice | ✅ Yes            |



## 🔹 Advantages

* Very fast for large datasets
* Cache-efficient
* Widely used in real systems



## 🔹 Disadvantages

* Worst-case **O(n²)** if pivot is poorly chosen
* Recursive overhead

---




1️⃣1️⃣ MERGE SORT (10 MARKS)

## MERGE SORT (Algorithm)

![Image](https://www.w3schools.com/dsa/img_mergesort_long.png)

![Image](https://static.afteracademy.com/images/merge-sort-example-explanation-2620b7697eb6af7e.png)

![Image](https://www.programiz.com/sites/tutorial2program/files/merge-sort-example_0.png)

![Image](https://miro.medium.com/v2/resize%3Afit%3A1400/1%2AEcYxs6OdHZjtUpCkqOJANg.png)

**Merge Sort** is a **divide-and-conquer** sorting algorithm that:

1. **Divides** the array into two halves
2. **Recursively sorts** each half
3. **Merges** the sorted halves to produce the final sorted array


## 🔹 Algorithm: MERGE_SORT(A, LOW, HIGH)

**Step 1:** If `LOW < HIGH`

**Step 2:**
`MID = (LOW + HIGH) / 2`

**Step 3:**
`MERGE_SORT(A, LOW, MID)`
`MERGE_SORT(A, MID + 1, HIGH)`

**Step 4:**
`MERGE(A, LOW, MID, HIGH)`

**Step 5:** **STOP**



## 🔹 Algorithm: MERGE(A, LOW, MID, HIGH)

**Step 1:**
`i = LOW`, `j = MID + 1`, `k = LOW`

**Step 2:** While `i ≤ MID` AND `j ≤ HIGH`

* If `A[i] ≤ A[j]`
  → `TEMP[k] = A[i]`, `i++`
* Else
  → `TEMP[k] = A[j]`, `j++`
* `k++`

**Step 3:** Copy remaining elements of left subarray (if any)

**Step 4:** Copy remaining elements of right subarray (if any)

**Step 5:** Copy `TEMP[LOW..HIGH]` back to `A[LOW..HIGH]`


## 🔹 Example

### Initial Array

```text id="ms1"
38   27   43   3   9   82   10
```

### Final Sorted Array

```text id="ms2"
3   9   10   27   38   43   82
```


## 🔹 Time Complexity

| Case    | Complexity     |
| ------- | -------------- |
| Best    | **O(n log n)** |
| Average | **O(n log n)** |
| Worst   | **O(n log n)** |



## 🔹 Space Complexity

* **O(n)** (extra temporary array)


## 🔹 Key Characteristics

| Property                | Value            |
| ----------------------- | ---------------- |
| Technique               | Divide & Conquer |
| Stable                  | ✅ Yes            |
| In-place                | ❌ No             |
| Predictable performance | ✅ Yes            |



## 🔹 Advantages

* Guaranteed **O(n log n)** time
* Stable sorting algorithm
* Suitable for **large datasets**
* Works well with **linked lists**


## 🔹 Disadvantages

* Requires extra memory
* Slower than Quick Sort in practice for small arrays

---


1️⃣2️⃣ HASHING (5 MARKS)

### 🔹 Concept

Hashing maps data to a fixed size table using hash function.

### 🔹 Steps

1. Apply hash function
2. Store element in hash table
3. Retrieve element using key

### 🔹 Application

• Database indexing
• Password storage

---

1️⃣3️⃣ COLLISION HANDLING (10 MARKS)

## COLLISION HANDLING (in Hashing)

![Image](https://i.sstatic.net/diHhF.png)

![Image](https://miro.medium.com/1%2ANKChpBn2gp1mweG9IAurBA.png)

![Image](https://i.sstatic.net/RT51v.png)

![Image](https://fiveable.me/_next/image?q=75\&url=https%3A%2F%2Fstorage.googleapis.com%2Fstatic.prod.fiveable.me%2Fsearch-images%252F%2522Collision_resolution_techniques_in_hash_tables%253A_open_addressing_vs_chaining_efficiency_and_memory_utilization%2522-1000px-Hash_table_5_0_1_1_1_1_0_LL.svg.png\&w=3840)

**Collision handling** refers to the techniques used in a **hash table** when **two or more keys map to the same hash index**.



## 🔹 Why Collisions Occur

* Limited hash table size
* Poor hash function
* Large number of keys



## 🔹 Major Collision Handling Techniques

### 1️⃣ **Chaining (Open Hashing)**

* Each table index stores a **linked list** of elements.
* All keys with the same hash value are chained together.

**Algorithm (Insert):**

1. Compute `index = hash(key)`
2. Insert key at the linked list of `table[index]`

**Advantages**

* Simple to implement
* No table overflow (as long as memory exists)

**Disadvantages**

* Extra memory for pointers
* Performance degrades if chains grow long

**Time Complexity**

* Average: **O(1)**
* Worst: **O(n)**



### 2️⃣ **Open Addressing (Closed Hashing)**

* All elements are stored **inside the hash table**
* On collision, search for another empty slot

#### a) **Linear Probing**

```text
index = (hash(key) + i) % table_size
```

* Checks next slot sequentially

**Pros:** Simple
**Cons:** Primary clustering


#### b) **Quadratic Probing**

```text
index = (hash(key) + i²) % table_size
```

* Reduces clustering compared to linear probing

**Cons:** Secondary clustering still exists



#### c) **Double Hashing**

```text
index = (h1(key) + i * h2(key)) % table_size
```

* Uses a second hash function

**Pros:** Best distribution
**Cons:** More complex



## 🔹 Comparison Table

| Technique         | Extra Space | Clustering | Performance |
| ----------------- | ----------- | ---------- | ----------- |
| Chaining          | ✅ Yes       | ❌ No       | Good        |
| Linear Probing    | ❌ No        | ✅ High     | Fair        |
| Quadratic Probing | ❌ No        | ⚠️ Medium  | Better      |
| Double Hashing    | ❌ No        | ❌ Low      | Best        |

---

1️⃣4️⃣ AVL TREE (10 MARKS)

## AVL TREE

![Image](https://pages.cs.wisc.edu/~wangy/AVLTree.png)

![Image](https://i.sstatic.net/AP14x.png)

![Image](https://www.cs.emory.edu/~cheung/Courses/253/Syllabus/Trees/FIGS/AVL/x-avl14b.gif)

![Image](https://i.sstatic.net/n6KwW.png)

An **AVL Tree** is a **self-balancing Binary Search Tree (BST)** in which the **height difference** (balance factor) between the left and right subtrees of **every node** is at most **1**.



## 🔹 Balance Factor (BF)

```text
BF(node) = Height(Left Subtree) − Height(Right Subtree)
```

**Valid values:** `-1, 0, +1`
If `|BF| > 1`, the tree becomes **unbalanced** and must be **rotated**.



## 🔹 Why AVL Trees?

* Prevents BST from becoming **skewed**
* Guarantees **O(log n)** time for search, insert, delete



## 🔹 Rotations in AVL Tree

When imbalance occurs after insertion or deletion, rotations restore balance.

### 1️⃣ **LL Rotation (Left–Left)**

* Insertion in **left subtree of left child**

**Fix:** Single **Right Rotation**


### 2️⃣ **RR Rotation (Right–Right)**

* Insertion in **right subtree of right child**

**Fix:** Single **Left Rotation**


### 3️⃣ **LR Rotation (Left–Right)**

* Insertion in **right subtree of left child**

**Fix:**
Left Rotation on left child → Right Rotation on node

---

### 4️⃣ **RL Rotation (Right–Left)**

* Insertion in **left subtree of right child**

**Fix:**
Right Rotation on right child → Left Rotation on node


## 🔹 Example (Insertion Causing Imbalance)

### Insert: `30, 20, 10`

```text
Before balancing (LL case):

    30
   /
  20
 /
10
```

### After Right Rotation

```text
    20
   /  \
 10   30
```


## 🔹 AVL Tree Insertion (High-Level Steps)

1. Insert node like **BST**
2. Update **height** of ancestors
3. Calculate **balance factor**
4. Apply appropriate **rotation**


## 🔹 Time Complexity

| Operation | Complexity   |
| --------- | ------------ |
| Search    | **O(log n)** |
| Insert    | **O(log n)** |
| Delete    | **O(log n)** |


## 🔹 Advantages

* Always balanced
* Faster search than normal BST
* Guaranteed performance


## 🔹 Disadvantages

* Extra memory for height storage
* Rotations make insertion/deletion more complex

---

## 🔹 Comparison: BST vs AVL Tree

| Feature           | BST    | AVL      |
| ----------------- | ------ | -------- |
| Balance           | ❌ No   | ✅ Yes    |
| Worst-case height | O(n)   | O(log n) |
| Search speed      | Slower | Faster   |
| Complexity        | Simple | Complex  |

---

## 🔹 DFS vs BFS

| DFS                    | BFS                        |
| ---------------------- | -------------------------- |
| Uses Stack / Recursion | Uses Queue                 |
| Goes deep first        | Goes level-wise            |
| Lower memory (usually) | Higher memory              |
| Not shortest path      | Shortest path (unweighted) |

---

1️⃣7️⃣ BFS VS DFS (5 MARKS)

• BFS uses queue
• DFS uses stack
• BFS finds shortest path
• DFS uses less memory

---

1️⃣8️⃣ MINIMUM SPANNING TREE – PRIM’S ALGORITHM (10 MARKS)

## MINIMUM SPANNING TREE – PRIM’S ALGORITHM

![Image](https://cp-algorithms.com/graph/MST_before.png)

![Image](https://images.tpointtech.com/core/images/prims-algorithm-java.png)

![Image](https://tutorialhorizon.com/static/media/algorithms/2015/06/PQ-9-15.png)

![Image](https://prepbytes-misc-images.s3.ap-south-1.amazonaws.com/assets/1661859676290-Image-05.png)

A **Minimum Spanning Tree (MST)** of a connected, weighted, undirected graph is a subgraph that:

* Connects **all vertices**
* Has **no cycles**
* Has **minimum possible total edge weight**

**Prim’s Algorithm** is a **greedy algorithm** that builds the MST by **growing one vertex at a time**, always choosing the **minimum-weight edge** that connects a visited vertex to an unvisited vertex.

---

## 🔹 Key Idea

> Start from any vertex and repeatedly add the **cheapest edge** that expands the tree.

---

## 🔹 Algorithm: PRIM(G, START)

**Input:**

* Graph `G(V, E)` with weights
* Starting vertex `START`

**Step 1:** Initialize

* `visited[v] = false` for all vertices
* `key[v] = ∞` (minimum edge weight to connect `v`)
* `parent[v] = -1`

**Step 2:** Set

* `key[START] = 0`

**Step 3:** Repeat for `(V − 1)` times

1. Select the **unvisited vertex `u` with minimum key value**
2. Mark `u` as **visited**
3. For each adjacent vertex `v` of `u`

   * If `v` is not visited **and** `weight(u, v) < key[v]`

     * `key[v] = weight(u, v)`
     * `parent[v] = u`

**Step 4:** The edges `(parent[v], v)` form the **MST**

**Step 5:** **STOP**

## 🔹 Characteristics of Prim’s Algorithm

| Feature            | Description          |
| ------------------ | -------------------- |
| Algorithm Type     | Greedy               |
| Graph Type         | Weighted, Undirected |
| Disconnected Graph | ❌ Not applicable     |
| Cycle Formation    | ❌ No cycles          |


## 🔹 Prim vs Kruskal (Quick Comparison)

| Prim’s                  | Kruskal’s                |
| ----------------------- | ------------------------ |
| Vertex-based            | Edge-based               |
| Grows one tree          | Builds forest            |
| Better for dense graphs | Better for sparse graphs |

---

2️⃣0️⃣ FILE STRUCTURE IN C (10 MARKS)

## FILE STRUCTURE IN C

![Image](https://deen3evddmddt.cloudfront.net/uploads/content-images/file-handling-in-c.webp)

![Image](https://www.dremendo.com/c-programming-tutorial/images/c-program-structure.png)

![Image](https://www.go4expert.com/proxy.php?hash=436af6a502c13c6d0b3a765550002b23\&image=https%3A%2F%2Fd1cakvb8tfmuws.cloudfront.net%2Ffile-descriptor-file-pointer%2FKernelFilePointers.jpg)

![Image](https://ars.els-cdn.com/content/image/3-s2.0-B9780340700143500542-u09-10-9780340700143.jpg)

In **C programming**, a **file** is a collection of data stored permanently on secondary storage (hard disk).
**File structure** in C refers to **how files are organized, accessed, and manipulated** using standard library functions.


## 🔹 Why File Handling is Needed

* Data is **lost** when program terminates (variables are temporary)
* Files provide **permanent storage**
* Useful for **large data**, reports, logs, databases



## 🔹 Types of Files in C

### 1️⃣ **Text Files**

* Data stored as **characters**
* Human-readable
* Examples: `.txt`, `.c`

**Functions used**

* `fprintf()`
* `fscanf()`
* `fgets()`
* `fputs()`



### 2️⃣ **Binary Files**

* Data stored in **binary format**
* Faster and more compact
* Not human-readable
* Examples: `.dat`, `.bin`

**Functions used**

* `fread()`
* `fwrite()`



## 🔹 File Pointer

```c
FILE *fp;
```

* `FILE` is a structure defined in `<stdio.h>`
* File pointer connects **program ↔ file**



## 🔹 Basic File Operations in C

### 1️⃣ Create / Open a File

```c
fp = fopen("data.txt", "r");
```

### 2️⃣ Read from File

```c
fscanf(fp, "%d", &x);
```

### 3️⃣ Write to File

```c
fprintf(fp, "%d", x);
```

### 4️⃣ Close the File

```c
fclose(fp);
```


## 🔹 File Opening Modes

| Mode             | Meaning                       |
| ---------------- | ----------------------------- |
| `r`              | Read only                     |
| `w`              | Write only (creates new file) |
| `a`              | Append                        |
| `r+`             | Read & write                  |
| `w+`             | Read & write (overwrite)      |
| `a+`             | Read & append                 |
| `rb`, `wb`, `ab` | Binary modes                  |


## 🔹 Structure of a File Program in C

```text
START
  ↓
Declare FILE pointer
  ↓
Open file using fopen()
  ↓
Perform read/write operations
  ↓
Close file using fclose()
  ↓
END
```


## 🔹 Random Access Functions

| Function   | Use               |
| ---------- | ----------------- |
| `fseek()`  | Move file pointer |
| `ftell()`  | Current position  |
| `rewind()` | Move to beginning |



## 🔹 Advantages of File Structure

* Permanent data storage
* Easy data retrieval
* Efficient for large datasets
* Supports data sharing


## 🔹 Disadvantages

* Slower than memory access
* Needs careful error handling

---

2️⃣1️⃣ BINARY VS TEXT FILE (5 MARKS)

## Binary File vs Text File (5 Marks)

![Image](https://www.scaler.com/topics/images/difference-between-text-file-and-binary-file-thumbnail.webp)

![Image](https://webapi.cihancopur.com/upload/Image/1000/fd452b55a3ca451d87381a036e2f83a3.gif)

![Image](https://control.com/uploads/articles/machine-readable-vs-human-readable-data-fig1.jpg)

![Image](https://control.com/uploads/articles/machine-readable-vs-human-readable-data-fig2.jpg)

In **C programming**, files are broadly classified into **text files** and **binary files** based on how data is stored and accessed.

A **text file** stores data in the form of **characters** (ASCII/Unicode). All data is converted into readable text before being written to the file. Text files are **human-readable** and can be easily opened and edited using a text editor like Notepad. Common examples include `.txt`, `.c`, and `.csv` files. However, text files require **more storage space** and are **slower** because data conversion takes place during input and output operations.

A **binary file**, on the other hand, stores data in **binary (0s and 1s) format**, exactly as it is present in the computer’s memory. Binary files are **not human-readable** and cannot be understood using a normal text editor. Examples include `.dat`, `.bin`, and `.exe` files. Binary files are **faster**, **more secure**, and **occupy less space** compared to text files, making them suitable for storing large volumes of data.

### Comparison Table

| Feature      | Text File          | Binary File        |
| ------------ | ------------------ | ------------------ |
| Data format  | Characters (ASCII) | Binary (0s and 1s) |
| Readability  | Human-readable     | Not human-readable |
| Storage size | Larger             | Smaller            |
| Speed        | Slower             | Faster             |
| Examples     | `.txt`, `.c`       | `.dat`, `.bin`     |

**Conclusion:**
Text files are preferred when data needs to be read or edited by humans, whereas binary files are preferred for **efficient storage and faster processing**.

---

2️⃣2️⃣ TIME COMPLEXITY (5 MARKS)

## TIME COMPLEXITY (5 Marks)

![Image](https://miro.medium.com/1%2AdWet_YU-5072Kcko7LzsuQ.jpeg)

![Image](https://paper-attachments.dropbox.com/s_2D428973624E7FC84C7D69D11421DE762BEA6B6F3361231FCDCAE0425D14526F_1664885448372_Untitled.drawio%2B17.png)

![Image](https://media2.dev.to/dynamic/image/width%3D800%2Cheight%3D%2Cfit%3Dscale-down%2Cgravity%3Dauto%2Cformat%3Dauto/https%3A%2F%2Fdev-to-uploads.s3.amazonaws.com%2Fuploads%2Farticles%2Fi4uqif112vvw150wphsw.jpg)

![Image](https://i.sstatic.net/ceoAc.png)

**Time Complexity** is a measure of the **amount of time an algorithm takes to execute** as a function of the **input size (n)**. It helps in analyzing and comparing algorithms **independent of hardware, compiler, or programming language**. Instead of calculating exact execution time, time complexity focuses on how the running time **grows with input size**.

Time complexity is expressed using **asymptotic notations**, which describe the performance of an algorithm for **large values of n**.



### Types of Time Complexity (Asymptotic Notations)

1. **Big-O Notation – O(f(n))**
   Represents the **worst-case time complexity**.
   It gives the **upper bound** on execution time.
   Example: Linear search → **O(n)**

2. **Big-Ω Notation – Ω(f(n))**
   Represents the **best-case time complexity**.
   It gives the **lower bound** on execution time.
   Example: Best case of linear search → **Ω(1)**

3. **Big-Θ Notation – Θ(f(n))**
   Represents the **average-case time complexity**.
   It gives a **tight bound** on execution time.


### Common Time Complexities

| Complexity | Example                 |
| ---------- | ----------------------- |
| O(1)       | Accessing array element |
| O(log n)   | Binary search           |
| O(n)       | Linear search           |
| O(n²)      | Bubble sort             |
| O(n log n) | Merge sort              |


### Importance of Time Complexity

* Helps select **efficient algorithms**
* Predicts performance for **large inputs**
* Saves **execution time and resources**

**Conclusion:**
Time complexity is a crucial concept in data structures and algorithms, as it allows programmers to design and choose algorithms that perform efficiently as input size increases.

---

2️⃣3️⃣ SPACE COMPLEXITY (5 MARKS)

## SPACE COMPLEXITY (5 Marks)

![Image](https://storage.googleapis.com/algodailyrandomassets/curriculum/fundamentals/space1.png)

![Image](https://i.sstatic.net/YNnOq.png)

![Image](https://cdn.botpenguin.com/assets/website/Space_Complexity_155761920b.webp)

![Image](https://storage.googleapis.com/algodailyrandomassets/curriculum/fundamentals/space2.png)

**Space Complexity** refers to the **amount of memory space required by an algorithm** to execute as a function of the **input size (n)**. It includes all the memory needed for **variables, data structures, function calls, and auxiliary storage** during program execution.

Space complexity is important because memory is a **limited resource**, and efficient algorithms should use **minimum possible space** while solving a problem.



### Components of Space Complexity

1. **Fixed Space**

   * Space required for constants, variables, and program instructions
   * Independent of input size

2. **Variable Space**

   * Space required for dynamic memory allocation
   * Depends on input size (arrays, linked lists, recursion stack)



### Types of Space Complexity

* **Auxiliary Space**: Extra space used by an algorithm (excluding input data)
* **Total Space**: Input space + Auxiliary space



### Common Space Complexities

| Space Complexity | Example                 |
| ---------------- | ----------------------- |
| O(1)             | Iterative algorithms    |
| O(n)             | Merge sort              |
| O(log n)         | Recursive binary search |
| O(n²)            | 2D matrix storage       |


### Importance of Space Complexity

* Helps in designing **memory-efficient algorithms**
* Important in **embedded systems** and **large data applications**
* Prevents memory overflow issues


**Conclusion:**
Space complexity measures how efficiently an algorithm uses memory. Along with time complexity, it plays a vital role in evaluating the overall performance of an algorithm.

---

2️⃣4️⃣ ORDERS OF COMPLEXITY (10 MARKS)
## ORDERS OF COMPLEXITY (10 Marks)

![Image](https://miro.medium.com/1%2AdWet_YU-5072Kcko7LzsuQ.jpeg)

![Image](https://miro.medium.com/1%2AP62yJveT5IuMOGizuIrX_w.png)

![Image](https://images.squarespace-cdn.com/content/v1/5acbdd3a25bf024c12f4c8b4/1599000012698-NJEGM0BCGG5ZKGIWC1GU/Big%2BO%2BNotation%2BSummary%2B%281%29.jpg)

**Orders of Complexity** describe how the **time or space requirement of an algorithm grows** as the size of input (**n**) increases. They help us **compare algorithms** and determine which one is more efficient for large inputs. Orders of complexity are expressed using **asymptotic notations**, mainly **Big-O notation**.

As input size increases, algorithms with lower orders of complexity perform better and scale efficiently.


## 🔹 Common Orders of Time Complexity

### 1️⃣ **Constant Time – O(1)**

* Execution time is **independent of input size**
* Always takes the same amount of time

**Example:**
Accessing an array element

```c
x = a[5];
```


### 2️⃣ **Logarithmic Time – O(log n)**

* Input size is **reduced at each step**
* Very efficient for large inputs

**Example:**
Binary Search


### 3️⃣ **Linear Time – O(n)**

* Execution time grows **proportionally with input size**

**Example:**
Linear Search, array traversal


### 4️⃣ **Linearithmic Time – O(n log n)**

* Combination of linear and logarithmic growth
* Common in efficient sorting algorithms

**Example:**
Merge Sort, Quick Sort (average case)


### 5️⃣ **Quadratic Time – O(n²)**

* Time increases as the **square of input size**
* Usually involves **nested loops**

**Example:**
Bubble Sort, Selection Sort


### 6️⃣ **Cubic Time – O(n³)**

* Time increases as **cube of input size**
* Inefficient for large inputs

**Example:**
Matrix multiplication (basic method)


### 7️⃣ **Exponential Time – O(2ⁿ)**

* Time doubles with every increase in input
* Extremely slow for large inputs

**Example:**
Recursive Fibonacci


### 8️⃣ **Factorial Time – O(n!)**

* Worst possible growth rate
* Used in permutation-based problems

**Example:**
Travelling Salesman Problem (brute force)


## 🔹 Comparison of Orders of Complexity

| Order      | Name         | Efficiency |
| ---------- | ------------ | ---------- |
| O(1)       | Constant     | Best       |
| O(log n)   | Logarithmic  | Very Good  |
| O(n)       | Linear       | Good       |
| O(n log n) | Linearithmic | Efficient  |
| O(n²)      | Quadratic    | Poor       |
| O(n³)      | Cubic        | Very Poor  |
| O(2ⁿ)      | Exponential  | Worst      |
| O(n!)      | Factorial    | Worst      |


## 🔹 Importance of Orders of Complexity

* Helps in **selecting the best algorithm**
* Predicts **performance for large inputs**
* Essential for **competitive programming and system design**
* Saves **time and memory resources**


### **Conclusion**

Orders of complexity provide a systematic way to analyze and compare algorithms based on their performance as input size grows. Algorithms with **lower order of complexity are always preferred**, especially for large-scale and real-time applications.

---
## What is Recursion? Advantages, Disadvantages & Comparison with Iteration

---
2️⃣5️⃣
## 🔹 What is Recursion?

**Recursion** is a programming technique in which a **function calls itself** to solve a problem by breaking it into **smaller sub-problems**.
A recursive solution must have:

1. **Base Case** – condition to stop recursion
2. **Recursive Case** – function calling itself

### Example (C):

```c
int fact(int n) {
    if (n == 0)        // Base case
        return 1;
    return n * fact(n - 1);   // Recursive call
}
```

---

## 🔹 Advantages of Recursion

* Simple and **easy to understand**
* Reduces code length
* Best suited for **divide-and-conquer** problems
* Natural fit for **tree and graph traversals**
* Improves readability for complex problems

---

## 🔹 Disadvantages of Recursion

* Uses extra memory due to **function call stack**
* Slower than iteration (function call overhead)
* Risk of **stack overflow** for deep recursion
* Difficult to debug and trace
* Not suitable for all problems

---

## 🔹 Recursion vs Iteration

| Feature      | Recursion                | Iteration                   |
| ------------ | ------------------------ | --------------------------- |
| Definition   | Function calls itself    | Uses loops (`for`, `while`) |
| Termination  | Base condition           | Loop condition              |
| Memory usage | High (stack memory)      | Low                         |
| Speed        | Slower                   | Faster                      |
| Code length  | Shorter                  | Longer                      |
| Readability  | Better for complex logic | Better for simple tasks     |
| Risk         | Stack overflow           | Infinite loop               |

---

## 🔹 Example Comparison (Factorial)

### Recursive

```c
int fact(int n) {
    if (n == 0)
        return 1;
    return n * fact(n - 1);
}
```

### Iterative

```c
int fact(int n) {
    int f = 1;
    for (int i = 1; i <= n; i++)
        f = f * i;
    return f;
}
```

---

## 🔹 When to Use Recursion?

* Tree traversals (BST, AVL)
* Divide & Conquer algorithms (Merge Sort, Quick Sort)
* Problems with natural recursive structure

---

## 🔹 Exam Tip (5–10 Marks)

* Write **definition**
* Mention **base case**
* List **advantages & disadvantages**
* Add **comparison table**
* Write **one example**

---

2️⃣6️⃣
### Dynamic Memory Allocation (5 Marks)

**Dynamic Memory Allocation (DMA)** is the process of allocating memory **at runtime** from the **heap memory** instead of allocating it at compile time. It is used when the size of data is **not known in advance** and memory needs to be managed efficiently during program execution.

In C programming, dynamic memory allocation is done using functions provided in the `<stdlib.h>` header file. The main functions are **`malloc()`**, **`calloc()`**, **`realloc()`**, and **`free()`**. The `malloc()` function allocates a block of memory without initialization, while `calloc()` allocates memory and initializes it to zero. The `realloc()` function is used to change the size of an already allocated memory block, and `free()` releases the allocated memory back to the system.

Dynamic memory allocation provides **flexibility and efficient memory utilization**, but it also has some drawbacks. It is slower than static memory allocation and may lead to problems like **memory leaks** and **dangling pointers** if memory is not properly freed.

**Conclusion:**
Dynamic memory allocation allows programs to manage memory efficiently at runtime, especially when handling large or variable-sized data.

---
### 2️⃣7️⃣Prority Queue-
    
A priority queue is an abstract data type similar to a regular queue, but with elements ordered by priority rather than insertion order. Each element has an associated priority, and the element with the highest priority is served first. If elements have equal priority, they are served based on their order in the queue. 
---

### 2️⃣8️⃣## Linked List – Definition, Types (with Diagrams), Applications & Need of Circular Linked List

![Image](https://miro.medium.com/v2/resize%3Afit%3A1050/1%2AMPEJnhLiRJ5vB3-Fp-Yjow.jpeg)

![Image](https://www.scaler.com/topics/images/different-types-of-linked-lists-in-the-data-structure.webp)

![Image](https://deen3evddmddt.cloudfront.net/uploads/content-images/circular-doubly-linked-list.webp)

![Image](https://ds1-iiith.vlabs.ac.in/exp/linked-list/circular-linked-list/images/circularly_linked_lists.png)


## 🔹 What is a Linked List?

A **Linked List** is a **dynamic linear data structure** in which elements (called **nodes**) are stored **non-contiguously** in memory.
Each node contains two parts:

* **DATA** – value stored
* **LINK** – address of the next node

The first node is pointed to by a pointer called **HEAD / START**.


## 🔹 Types of Linked List


### 1️⃣ Singly Linked List (SLL)

Each node has:

* Data
* Link to the **next node**

**Diagram:**

```text
10 → 20 → 30 → 40 → NULL
```

**Features:**

* Traversal in **one direction**
* Less memory usage
* Simple implementation


### 2️⃣ Doubly Linked List (DLL)

Each node has:

* Data
* Link to **previous node**
* Link to **next node**

**Diagram:**

```text
NULL ← 10 ⇄ 20 ⇄ 30 ⇄ 40 → NULL
```

**Features:**

* Traversal in **both directions**
* Faster deletion
* Uses more memory (extra pointer)


### 3️⃣ Circular Linked List (CLL)

Last node points back to the **first node** instead of `NULL`.

**Diagram:**

```text
10 → 20 → 30 → 40
 ↑________________↓
```

**Features:**

* No `NULL` pointer
* Traversal starts from any node
* Useful for cyclic operations



## 🔹 Applications of Linked List

* Dynamic memory management
* Implementation of **stack, queue, deque**
* Polynomial manipulation
* Sparse matrix representation
* Graph adjacency list
* Undo/Redo operations
* Music playlists & image viewers


## 🔹 Why Do We Need Circular Linked List?

### Problems with Linear Linked List

* Traversal always starts from **first node**
* Extra condition checking for `NULL`
* Inefficient for cyclic processes

### Advantages of Circular Linked List

* No `NULL` pointer → continuous traversal
* Any node can be a **starting point**
* Efficient for **round-robin scheduling**
* Used in **CPU scheduling**
* Used in **circular queues**
* Suitable for **repeating processes**



## 🔹 Real-Life Example of Circular Linked List

* CPU task scheduling
* Multiplayer games (turn-based)
* Traffic light control system
* Music player loop mode



## 🔹 Comparison (Quick View)

| Feature      | Singly | Doubly | Circular  |
| ------------ | ------ | ------ | --------- |
| Direction    | One    | Two    | One / Two |
| Extra Memory | Low    | High   | Low       |
| NULL Pointer | Yes    | Yes    | No        |
| Cyclic Use   | ❌      | ❌      | ✅         |



## 🔹 Conclusion (Exam-Ready)

A linked list is a dynamic data structure that allows efficient insertion and deletion. It is classified into singly, doubly, and circular linked lists. Circular linked lists are especially useful for applications requiring continuous or cyclic traversal.

---
### 2️⃣9️⃣TREE – Definition, Basic Elements, Representations & Types

![Image](https://images.openai.com/static-rsc-3/Qcosb1hJMUK3EA0a8AKLKQL-Xyh_PRHVcdngiqb4ZB2P8XKmDyCIV-UdDFdsipflIcF4RI_cuhlw79zEkcXm-T-bIDdzH5SmsDqhJoRc3vs?purpose=fullsize\&v=1)

![Image](https://www.nku.edu/~longa/classes/mat115/days/resources/graphs/Tree-Basic-Terminology.png)

![Image](https://miro.medium.com/1%2ACMGFtehu01ZEBgzHG71sMg.png)

![Image](https://www.theknowledgeacademy.com/_files/images/Types_of_Binary_Trees.png)


## 🔹 What is a Tree?

A **Tree** is a **non-linear hierarchical data structure** that consists of **nodes** connected by **edges**.
It is used to represent data having a **parent–child relationship**.

* The topmost node is called the **root**
* Every tree has **one root**
* There is **no cycle** in a tree



## 🔹 Basic Elements of a Tree

### 1️⃣ Node

* A basic unit that stores **data**
* Each node may have zero or more children

### 2️⃣ Root

* The **topmost node** of the tree
* Has **no parent**

### 3️⃣ Edge

* A connection between two nodes (parent → child)

### 4️⃣ Parent

* A node that has one or more children

### 5️⃣ Child

* A node that descends from a parent

### 6️⃣ Leaf (External Node)

* A node with **no children**

### 7️⃣ Internal Node

* A node with **at least one child**

### 8️⃣ Level

* Position of a node in the tree (root is at level 0 or 1)

### 9️⃣ Height

* Maximum number of levels in a tree



### 📌 Example Tree

```text
        A
      /   \
     B     C
    / \     \
   D   E     F
```



## 🔹 Different Ways to Represent a Tree



### 1️⃣ Array Representation

* Tree nodes are stored in an **array**
* Mostly used for **complete binary trees**

**Index rule (Binary Tree):**

* Left child → `2i`
* Right child → `2i + 1`
* Parent → `i / 2`

**Advantages**

* Simple representation
* Fast access

**Disadvantages**

* Wastes memory for sparse trees



### 2️⃣ Linked List Representation

* Each node contains:

  * Data
  * Pointer to left child
  * Pointer to right child

```text
struct node {
   int data;
   struct node *left;
   struct node *right;
};
```

**Advantages**

* Dynamic memory usage
* No memory wastage

**Disadvantages**

* Extra memory for pointers



## 🔹 Types of Trees



### 1️⃣ General Tree

* A node can have **any number of children**



### 2️⃣ Binary Tree

* Each node has **at most two children**
* Left child and right child



### 3️⃣ Binary Search Tree (BST)

* Left subtree < Root
* Right subtree > Root
* Enables fast searching



### 4️⃣ Complete Binary Tree

* All levels filled except possibly the last
* Nodes filled from **left to right**



### 5️⃣ Full Binary Tree

* Each node has **0 or 2 children**



### 6️⃣ AVL Tree

* A **self-balancing BST**
* Height difference ≤ 1



### 7️⃣ Heap

* A complete binary tree
* Used in **priority queues**
* Types: Min-Heap, Max-Heap



## 🔹 Applications of Trees

* File system hierarchy
* Database indexing
* Expression evaluation
* XML/HTML parsing
* Artificial Intelligence
* Operating systems

---

### 📚 DSA Important Exam Questions – To-Do List

---

## ✅ 5 MARKS QUESTIONS

* [x]  What is DSA and why do we need DSA?
* [x]  Types of Data Structures and Basic Operations Performed on Data Structures
* [x] What is an Array? Explain its types.
* [x] Applications of Array.
* [x] Hashing.
* [x] Binary vs Text File.
* [x] Time Complexity.
* [x] Space Complexity.
* [x] BFS vs DFS.
* [x] Dynamic memory allocation
* [x] explain priority queue?
---

## ✅ 10 MARKS QUESTIONS

* [x] Stack – PUSH & POP Operations.
* [x] Queue – ENQUEUE & DEQUEUE Operations.
* [x] Singly Linked List – Insert at Any Position.
* [x] Binary Search Tree – Insert Operation, Delete Operations
* [x] Binary Tree Traversals (Inorder, Preorder, Postorder).
* [x] Insertion Sort.
* [x] Quick Sort.
* [x] Merge Sort.
* [x] Collision Handling in Hashing.
* [x] AVL Tree.
* [x] Minimum Spanning Tree – Prim’s Algorithm.
* [x] File Structure in C.
* [x] Orders of Complexity.
* [x] What is reccursion? advantages and disadvantages ? compare recurssion and itterative?
* [x] What is linked list? explain types with diagrams ? Application of linked list? why we need circular linked list?
* [x] What is tree? Explain their basic element ? explain different way to represent a tree? explain type of tree?
---
