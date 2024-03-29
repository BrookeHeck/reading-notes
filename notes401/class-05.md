# Implementation: Linked Lists

## BigO
- Describes the efficiency of an algorithm/function
  - Running time - amount of time a function needs to complete
  - memory space - amount of memory resources a function uses to store data and instructions

- BigO describes the worst case efficiency of an algorithm
- 4 Key Areas for analysis
  1. input size
    - size of the parameter values that are read by the algorithm
    - also accounts for the size of each parameter as well
  2. units of measurement
  - ***Time***
    - time in milliseconds from the start of function execution to it ends
    - number of operations executed
    - number of basic operations, refers to the operations that contribute the most to total running time
  - ***Space***
    - amount of space needed to hold code for the algorithm, bytes required to store the characters for instructions
    - amount of space required to hold the input
    - amount of space required to hold the output data
    - amount of space needed to hold the working space

  3. orders of growth

    <img src='./img/ordersOfGrowth/bigo1.png' width='50%' height='auto'>
    <img src='./img/ordersOfGrowth/bigo2.png' width='50%' width='50%' height='auto' >
    <img src='./img/ordersOfGrowth/bigo3.png' width='50%' width='50%' height='auto' >
    <img src='./img/ordersOfGrowth/bigo4.png' width='50%' width='50%' height='auto' >
    <img src='./img/ordersOfGrowth/bigo5.png' width='50%' width='50%' height='auto' >
    <img src='./img/ordersOfGrowth/bigo6.png' width='50%' width='50%' height='auto' >
    <img src='./img/ordersOfGrowth/bigo7.png' width='50%' width='50%' height='auto' >
    <img src='./img/ordersOfGrowth/bigo8.png' width='50%' width='50%' height='auto' >

  4. best case, worst case, and average case
  - Worst Case: efficiency for worst possible input of size n
    - Big O
  - best case: efficiency for best possible input size n
    - Big Omega
  - average case: efficiency for a typical or random input 
  size of n
    - Big Theta

 - OVERVIEW

 <img src='./img/ordersOfGrowth/bigo9.png' width='50%' width='50%' height='auto' >

## Linked Lists
- Linked list is sequence of nodes that reference the next node
- can be implemented as a singly or doubly linked list

- Traversal: traversal of linked lists relies on Next
  - while loops work well with linked lists because you can call next until you find the node your looking at
  - if we try to traverse a node that is null, a NullReferenceException error is thrown
  - the Current variable will tell us which node we are on in the traversal
  - the Head is always the first node in the list
  - Big O for time would be O(n), worst case scenario the node we are looking for is at the end
  - Big O for space is O(1), no additional space is needed when already given a linked list
  
```
  ALGORITHM Includes (value)
  // INPUT <-- integer value
  // OUTPUT <-- boolean

  Current <-- Head

  WHILE Current is not NULL
    IF Current.Value is equal to value
      return TRUE

    Current <-- Current.Next

  return FALSE
```

  - Adding a Node
    - be careful that every node in the list references the correct next node
    - when adding nodes change the reference of the head node, and make the reference of the new node, the node that the head was previously referencing
    - Big O will always be O(1) time and space because it takes the same amount of time and space

  ```
  ALGORITHM Add(newValue)
  // INPUT <-- Value to add
  // OUTPUT <-- No output

  newNode <-- NEW Node
  newNode.Value <-- newValue
  newNode.Next <-- Head
  Head <-- newNode
  ```


## Things I want to learn more about

### Links
[Big O: Analysis of Algorithm Efficiency](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/big_oh.html)

[Linked Lists](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-05/resources/singly_linked_list.html)

[What’s a Linked List, Anyway? [Part 1]](https://medium.com/basecs/whats-a-linked-list-anyway-part-1-d8b7e6508b9d)

[What’s a Linked List, Anyway? [Part 2]](https://medium.com/basecs/whats-a-linked-list-anyway-part-2-131d96f71996)