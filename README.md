# DS

1.Stack in Python

    A stack is a linear data structure that stores items in a Last-In/First-Out (LIFO) or First-In/Last-Out (FILO) manner. In stack, a new element is added at one end and an element is removed from that end only. The insert and delete operations are often called push and pop.
    
    Stack in python
    
    The functions associated with stack are:
    
    empty() – Returns whether the stack is empty – Time Complexity : O(1)
    size() – Returns the size of the stack – Time Complexity : O(1)
    top() – Returns a reference to the top most element of the stack – Time Complexity : O(1)
    push(g) – Adds the element ‘g’ at the top of the stack – Time Complexity : O(1)
    pop() – Deletes the top most element of the stack – Time Complexity : O(1)
    Implementation
    There are various ways from which a stack can be implemented in Python. This article covers the implementation of stack using data structures and modules from Python library.
    
    Stack in Python can be implemented using following ways:
    
        list
        collections.deque
        queue.LifoQueue



2.Queue in Python
    Like stack, queue is a linear data structure that stores items in First In First Out (FIFO) manner. With a queue the least recently added item is removed first. A good example of queue is any queue of consumers for a resource where the consumer that came first is served first.
    
    Queue in Python
    
    Operations associated with queue are:
    
    Enqueue: Adds an item to the queue. If the queue is full, then it is said to be an Overflow condition – Time Complexity : O(1)
    Dequeue: Removes an item from the queue. The items are popped in the same order in which they are pushed. If the queue is empty, then it is said to be an Underflow condition – Time Complexity : O(1)
    Front: Get the front item from queue – Time Complexity : O(1)
    Rear: Get the last item from queue – Time Complexity : O(1)
    Implementation
    There are various ways to implement a queue in Python. This article covers the implementation of queue using data structures and modules from Python library.
    
    Queue in Python can be implemented by the following ways:
    
        list
        collections.deque
        queue.Queue

3.LinkedList

    Like arrays, Linked List is a linear data structure. Unlike arrays, linked list elements are not stored at a contiguous location; the elements are linked using pointers.
    linkedlist
    
    Why Linked List?
    Arrays can be used to store linear data of similar types, but arrays have the following limitations.
    1) The size of the arrays is fixed: So we must know the upper limit on the number of elements in advance. Also, generally, the allocated memory is equal to the upper limit irrespective of the usage.
    2) Inserting a new element in an array of elements is expensive because the room has to be created for the new elements and to create room existing elements have to be shifted.
    
    For example, in a system, if we maintain a sorted list of IDs in an array id[].
    
    id[] = [1000, 1010, 1050, 2000, 2040].
    
    
    
    
    And if we want to insert a new ID 1005, then to maintain the sorted order, we have to move all the elements after 1000 (excluding 1000).
    Deletion is also expensive with arrays until unless some special techniques are used. For example, to delete 1010 in id[], everything after 1010 has to be moved.
    
    Advantages over arrays
    1) Dynamic size
    2) Ease of insertion/deletion
    
    Drawbacks:
    1) Random access is not allowed. We have to access elements sequentially starting from the first node. So we cannot do binary search with linked lists efficiently with its default implementation. Read about it here.
    2) Extra memory space for a pointer is required with each element of the list.
    3) Not cache friendly. Since array elements are contiguous locations, there is locality of reference which is not there in case of linked lists.
    
    Representation:
    A linked list is represented by a pointer to the first node of the linked list. The first node is called the head. If the linked list is empty, then the value of the head is NULL.
    Each node in a list consists of at least two parts:
    1) data
    2) Pointer (Or Reference) to the next node

4.Binary Tree

    A tree whose elements have at most 2 children is called a binary tree. Since each element in a binary tree can have only 2 children, we typically name them the left and right child.
    
    
    
    A Binary Tree node contains following parts.
    
    Data
    Pointer to left child
    Pointer to right child
    
  Tree Traversals
    Unlike linear data structures (Array, Linked List, Queues, Stacks, etc) which have only one logical way to traverse them, trees can be traversed in different ways. Following are the generally used ways for traversing trees.
    
 
    Depth First Traversals:
    (a) Inorder (Left, Root, Right) : 4 2 5 1 3
    (b) Preorder (Root, Left, Right) : 1 2 4 5 3
    (c) Postorder (Left, Right, Root) : 4 5 2 3 1
    
    Breadth First or Level Order Traversal : 1 2 3 4 5
    
    Inorder Traversal :
    
    Algorithm Inorder(tree)
       1. Traverse the left subtree, i.e., call Inorder(left-subtree)
       2. Visit the root.
       3. Traverse the right subtree, i.e., call Inorder(right-subtree)
    Uses of Inorder
    In case of binary search trees (BST), Inorder traversal gives nodes in non-decreasing order. To get nodes of BST in non-increasing order, a variation of Inorder traversal where Inorder traversal s reversed can be used.
    Example: Inorder traversal for the above-given figure is 4 2 5 1 3.
 
    Preorder Traversal :
    
    Algorithm Preorder(tree)
       1. Visit the root.
       2. Traverse the left subtree, i.e., call Preorder(left-subtree)
       3. Traverse the right subtree, i.e., call Preorder(right-subtree) 
    Uses of Preorder
    Preorder traversal is used to create a copy of the tree. Preorder traversal is also used to get prefix expression on of an expression tree. Please see http://en.wikipedia.org/wiki/Polish_notation to know why prefix expressions are useful.
    Example: Preorder traversal for the above given figure is 1 2 4 5 3.
    
    
    Postorder Traversal
    
    Algorithm Postorder(tree)
       1. Traverse the left subtree, i.e., call Postorder(left-subtree)
       2. Traverse the right subtree, i.e., call Postorder(right-subtree)
       3. Visit the root.
    Uses of Postorder
    Postorder traversal is used to delete the tree. Please see the question for deletion of tree for details. Postorder traversal is also useful to get the postfix expression of an expression tree. Please see http://en.wikipedia.org/wiki/Reverse_Polish_notation to for the usage of postfix expression.
    
    Example: Postorder traversal for the above given figure is 4 5 2 3 1.

  Binary Heap
  
    A Binary Heap is a Binary Tree with following properties.
    1) It’s a complete tree (All levels are completely filled except possibly the last level and the last level has all keys as left as possible). This property of Binary Heap makes them suitable to be stored in an array.
    
    2) A Binary Heap is either Min Heap or Max Heap. In a Min Binary Heap, the key at root must be minimum among all keys present in Binary Heap. The same property must be recursively true for all nodes in Binary Tree. Max Binary Heap is similar to MinHeap.
    
    Examples of Min Heap:
    
                10                      10
             /      \               /       \  
           20        100          15         30  
          /                      /  \        /  \
        30                     40    50    100   40
    How is Binary Heap represented?
    A Binary Heap is a Complete Binary Tree. A binary heap is typically represented as an array.
    
    The root element will be at Arr[0].
    Below table shows indexes of other nodes for the ith node, i.e., Arr[i]:
    Arr[(i-1)/2]	Returns the parent node
    Arr[(2*i)+1]	Returns the left child node
    Arr[(2*i)+2]	Returns the right child node
    The traversal method use to achieve Array representation is Level Order
    
    
    
    
    
    Please refer Array Representation Of Binary Heap for details.
    
    
    
    Applications of Heaps:
    1) Heap Sort: Heap Sort uses Binary Heap to sort an array in O(nLogn) time.
    
    2) Priority Queue: Priority queues can be efficiently implemented using Binary Heap because it supports insert(), delete() and extractmax(), decreaseKey() operations in O(logn) time. Binomoial Heap and Fibonacci Heap are variations of Binary Heap. These variations perform union also efficiently.
    
    3) Graph Algorithms: The priority queues are especially used in Graph Algorithms like Dijkstra’s Shortest Path and Prim’s Minimum Spanning Tree.
    
    4) Many problems can be efficiently solved using Heaps. See following for example.
    a) K’th Largest Element in an array.
    b) Sort an almost sorted array/
    c) Merge K Sorted Arrays.
    
    Operations on Min Heap:
    1) getMini(): It returns the root element of Min Heap. Time Complexity of this operation is O(1).
    
    2) extractMin(): Removes the minimum element from MinHeap. Time Complexity of this Operation is O(Logn) as this operation needs to maintain the heap property (by calling heapify()) after removing root.
    
    3) decreaseKey(): Decreases value of key. The time complexity of this operation is O(Logn). If the decreases key value of a node is greater than the parent of the node, then we don’t need to do anything. Otherwise, we need to traverse up to fix the violated heap property.
    
    
    
    
    4) insert(): Inserting a new key takes O(Logn) time. We add a new key at the end of the tree. IF new key is greater than its parent, then we don’t need to do anything. Otherwise, we need to traverse up to fix the violated heap property.
    
    5) delete(): Deleting a key also takes O(Logn) time. We replace the key to be deleted with minum infinite by calling decreaseKey(). After decreaseKey(), the minus infinite value must reach root, so we call extractMin() to remove the key.

5.Graph

    A Graph is a non-linear data structure consisting of nodes and edges. The nodes are sometimes also referred to as vertices and the edges are lines or arcs that connect any two nodes in the graph. More formally a Graph can be defined as,
    
    A Graph consists of a finite set of vertices(or nodes) and set of Edges which connect a pair of nodes.
    
    
    
    In the above Graph, the set of vertices V = {0,1,2,3,4} and the set of edges E = {01, 12, 23, 34, 04, 14, 13}.
    
    Graphs are used to solve many real-life problems. Graphs are used to represent networks. The networks may include paths in a city or telephone network or circuit network. Graphs are also used in social networks like linkedIn, Facebook. For example, in Facebook, each person is represented with a vertex(or node). Each node is a structure and contains information like person id, name, gender, locale etc.
    
   Graph representation
 
     A graph is a data structure that consists of the following two components:
    1. A finite set of vertices also called as nodes.
    2. A finite set of ordered pair of the form (u, v) called as edge. The pair is ordered because (u, v) is not the same as (v, u) in case of a directed graph(di-graph). The pair of the form (u, v) indicates that there is an edge from vertex u to vertex v. The edges may contain weight/value/cost.
    
    Graphs are used to represent many real-life applications: Graphs are used to represent networks. The networks may include paths in a city or telephone network or circuit network. Graphs are also used in social networks like linkedIn, Facebook. For example, in Facebook, each person is represented with a vertex(or node). Each node is a structure and contains information like person id, name, gender, and locale. See this for more applications of graph.
    
    Following is an example of an undirected graph with 5 vertices.
    
    
    The following two are the most commonly used representations of a graph.
    1. Adjacency Matrix
    2. Adjacency List
    There are other representations also like, Incidence Matrix and Incidence List. The choice of graph representation is situation-specific. It totally depends on the type of operations to be performed and ease of use.
    
    Adjacency Matrix:
    Adjacency Matrix is a 2D array of size V x V where V is the number of vertices in a graph. Let the 2D array be adj[][], a slot adj[i][j] = 1 indicates that there is an edge from vertex i to vertex j. Adjacency matrix for undirected graph is always symmetric. Adjacency Matrix is also used to represent weighted graphs. If adj[i][j] = w, then there is an edge from vertex i to vertex j with weight w.
    
    
    
    
    
    
    The adjacency matrix for the above example graph is:
    Adjacency Matrix Representation
    
    Pros: Representation is easier to implement and follow. Removing an edge takes O(1) time. Queries like whether there is an edge from vertex ‘u’ to vertex ‘v’ are efficient and can be done O(1).
    
    Cons: Consumes more space O(V^2). Even if the graph is sparse(contains less number of edges), it consumes the same space. Adding a vertex is O(V^2) time.
    Please see this for a sample Python implementation of adjacency matrix.
    
    
    
    Adjacency List:
    An array of lists is used. The size of the array is equal to the number of vertices. Let the array be an array[]. An entry array[i] represents the list of vertices adjacent to the ith vertex. This representation can also be used to represent a weighted graph. The weights of edges can be represented as lists of pairs. Following is the adjacency list representation of the above graph.
    
BFS

    Breadth First Traversal (or Search) for a graph is similar to Breadth First Traversal of a tree (See method 2 of this post). The only catch here is, unlike trees, graphs may contain cycles, so we may come to the same node again. To avoid processing a node more than once, we use a boolean visited array. For simplicity, it is assumed that all vertices are reachable from the starting vertex.
    For example, in the following graph, we start traversal from vertex 2. When we come to vertex 0, we look for all adjacent vertices of it. 2 is also an adjacent vertex of 0. If we don’t mark visited vertices, then 2 will be processed again and it will become a non-terminating process. A Breadth First Traversal of the following graph is 2, 0, 3, 1.
    
DFS

    Depth First Traversal (or Search) for a graph is similar to Depth First Traversal of a tree. The only catch here is, unlike trees, graphs may contain cycles, a node may be visited twice. To avoid processing a node more than once, use a boolean visited array.