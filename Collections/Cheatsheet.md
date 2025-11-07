#  Collections

## Cheat-sheet table for collections in java.

| USE-CASE | INTERFACE | TYPICAL IMPLEMENTATION | KEY PROPERTIES |
|----------|-----------|------------------------|----------------|
| Ordered list of elements| **List** | *ArrayList* | Allows duplicates, maintains insertion order, allows nulls, not thread-safe. Access: O(1), Insert/Delete: O(n) |
| | | *LinkedList* | Allows duplicates, maintains insertion order, allows nulls, not thread-safe. Access: O(n), Insert/Delete: O(1) |
| Unique Elements | **Set** | *HashSet* | No duplicates, no gauranteed order, allows one null, not thread-safe. Add/Remove/Contains: O(1) |
| | | *LinkedHashSet* | No duplicates, maintains insertion order, allows one null, not thread-safe. Add/Remove: O(1) |
| | | *TreeSet* | No duplicates, sortd order, no nulls, not thread-safe. Add/Remove/Cotains:O(logn) |
| Key-value pairs | **Map** | *HashMap* | No duplicate keys, unorderd, allows one null key and multiple null values, not thread-safe, Get/Put: o(1) |
| | | *TreeMap* | No duplicate keys, sorted by key, no null keys, allows null values, not thread-safe. Get/Put: O(logn) |
| | | *HashTable* | No duplicate keys, unorderd, no null keys/values, thread-safe(synchronized). Get/Put: O(1) |
| | | *ConcurrentHash* | No duplicate keys, unorderd, no null keys/values, thread-safe(high concurrency). Get/Put: O(1) |
| FIFO queue | **Queue** | *LinkedList* | Allows duplicates, maintains insertion order, allows nulls, not thread-safe. Offer/poll: O(1) |
| | | *Priority queue* | Allow duplicates, sorted by priority, no nulls, not thread-safe. Offer/Poll: O(logn) | 
| Double ended queue | **Dequeue** | *ArrayDequeue* | Allows duplicates, maintains insertion order, no nulls, not thread-safe. Add/Remove at ends: O(1) |
| | | *LinkedList* | Allows duplicates, maintains insertion order, allows nulls, not thread-safe. Add/Remove at ends: O(1) |


## Choosing the right Java interface.

- Need key-value pairs ---->|Yes|----> **MAP**
  - |No|---> Traversal according to insertion order ---->|Yes| ----> **LIST**
    - |No| ---> LIFO FIFO, Remove by priority ---->|Yes| ----> **QUEUE**
      - |No| ---> Duplicate elements present ---->|No| ----> **SET**
        - |Yes| ----> **LIST**

## Concrete Collection Selection Diagram
![Collection selection diagram](https://www.baeldung.com/wp-content/uploads/2022/11/Concrete-Collection-Selection-Diagram.png)


      
