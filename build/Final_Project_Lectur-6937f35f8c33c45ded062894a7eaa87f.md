# Linked Hash Map: Concept

## Motivation
In our introductory data structures course, whenever the disadvantages of various foundational structures (such as memory overhead or search speed) were mentioned, we found ourselves questioning whether we simply have to accept these limitations in real-world applications, or if there are ways to overcome them. For instance, during our recursive lab session on the Fibonacci sequence, we learned how adding an array (memoization) could drastically reduce time complexity. This inspired us to wonder: 

**"Can we apply a similar optimization strategy to overcome the inherent limitations of a Linked List?"**

## Basic Notion
- Doubly Linked List (DLL): DLL allocates an extra pointer (prev) gor bidrectional traversal compared to singly or circular linked lists. Searching for an element requires linear traversal, resulting in a time complexity of O(n).
- Hash Map: Hash map passes a key through a hash function generates an index, allowing direct memory access in O(1) time complexity.

## Core Notion
- Structure: It maintains both a **Hash Map and a Doubly Linked List** simultaneoulsy. The DLL maintains the insertion/access order, while the Hash Map handles instantaneous searching.
- Core Algorithms
    - Insert: Adds a new key-value pair to the Hash Map and appends a node to the DLL.
    - Search: Instantly locates the DLL node using the Hash Map in O(1) time.
    - Delete: Removes the node from both the DLL and the Hash Map.
    - Move: Relocates a specific node within the DLL (e.g., moving it to the head).

## Application
- LRU Cache: A caching strategy that discards the least recently used items first when the cache reaches its capacity.
    - Role of DLL: Maintains the chronological order of data usage.
    - Role of Hash Map: Allows instantaneous checking of whether a piece of data already exists in the cache.
- Inventory System
    - Role of DLL: Keeps items sorted based on custom criteria (e.g., recently equipped, acquired time).
    - Role of Hash Map: Allows players to instantly search for or modify an item by its unique ID.

## Lab session
1. Code Overview & Display (class definition, item insert/remove, controller search, LRU Cache)
2. Experiencing the DLL Search Limitation Firsthand
3. Interactive Activity: "Build Your Own Inventory Sorter"
- [Lab_session_Code_Demo](DS_final_project_code_demo)

## Conclusion
The core message of this project is that **the structural flaws of a primary data structure do not have to be a dead-end.** By strategically combining it with complementary data structures, we can engineer highly optimized solutions for real-world software development.