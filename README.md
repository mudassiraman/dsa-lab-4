### Exercise 1: Linked List with Dummy Head Node (`HList`)

A **Linked List with a Dummy Head Node** simplifies insertion and deletion operations by introducing a special node at the start of the list that doesn’t hold any data. This ensures that every node (including the first node with data) has a predecessor, which makes operations like adding or removing nodes easier since we don’t have to treat the head differently.

#### Key Operations:

1. **Constructor (`HList()`)**: Initializes the list with a dummy head node. This head node points to `nullptr` initially, meaning there are no data nodes in the list.

2. **Check if List is Empty (`emptyList()`)**: Returns `true` if the list contains no data nodes. The dummy head always exists, so we check if the node after the dummy head is `nullptr`.

3. **Insert After a Node (`insert_after(oldV, newV)`)**: Searches for a node with value `oldV` and inserts a new node with value `newV` after it. The list is traversed starting from the node after the dummy head.

4. **Insert at Beginning (`insert_begin(value)`)**: Inserts a new node with the given value right after the dummy head, making it the first data node in the list.

5. **Insert at End (`insert_end(value)`)**: Traverses the list to find the last node and adds a new node with the specified value at the end.

6. **Delete Node by Value (`delete_Node(val)`)**: Removes the first node in the list that contains the specified value. The list is traversed, and the node’s predecessor is updated to skip over the node being deleted.

7. **Delete First Node (`delete_begin()`)**: Removes the first data node in the list (i.e., the node right after the dummy head).

8. **Delete Last Node (`delete_end()`)**: Traverses the list to find the last node and removes it, ensuring the second last node now points to `nullptr`.

9. **Traverse and Display List (`traverse()`)**: Traverses the entire list (skipping the dummy head) and prints out the values of all data nodes in the list.

---

### Exercise 2: Circular Linked List (`CList`)

In a **Circular Linked List**, the last node in the list points back to the first node, creating a loop or circular structure. This allows the list to be traversed continuously without encountering `nullptr`, which is typical in linear linked lists.

#### Key Operations:

1. **Constructor (`CList()`)**: Initializes an empty circular linked list. The list starts with no nodes, so `head` is `nullptr`.

2. **Check if List is Empty (`emptyList()`)**: Returns `true` if there are no nodes in the list (i.e., when `head` is `nullptr`).

3. **Insert at Specific Position (`insert_at(pos, value)`)**: Inserts a new node at the given position in the list (except the first position). The list is traversed, and the node is inserted at the specified index, maintaining the circular structure.

4. **Insert at Beginning (`insert_begin(value)`)**: Inserts a new node at the start of the list. The new node becomes the first node, and the last node is updated to point to it, maintaining the circular link.

5. **Insert at End (`insert_end(value)`)**: Inserts a new node at the end of the list. The new node’s `next` pointer is set to point back to the head, maintaining the circular structure.

6. **Delete Node at Position (`deleteNode(pos)`)**: Removes the node at the specified position in the list (except the first node). The list is traversed, and the node is removed while keeping the circular link intact.

7. **Delete First Node (`delete_begin()`)**: Removes the first node in the list, updates the head to the next node, and ensures the last node still points to the new head.

8. **Delete Last Node (`delete_end()`)**: Traverses the list to find the last node and removes it. The new last node’s `next` pointer is set to point to the head.

9. **Traverse and Display List (`traverse()`)**: Traverses the entire circular linked list starting from the head and prints the value of each node. Since the list is circular, traversal stops when it loops back to the head.

---

### Summary of Concepts:
- **Linked List with Dummy Head Node**: Simplifies handling special cases for the first node by introducing a dummy head that always exists, ensuring that insertions and deletions can be handled uniformly.
  
- **Circular Linked List**: A structure where the last node points back to the first node, allowing for continuous traversal and unique operations like looping through the list without hitting a null pointer. This requires special handling for both insertions and deletions to maintain the circular property.
