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
