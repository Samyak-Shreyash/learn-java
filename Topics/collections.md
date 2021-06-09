# Collections

In general terms, a collection represents a group of objects. In Java, collections are handled by collection framework. Collections framework is an unified architecture for representing and manipulating collections.

![Collections Framework](https://d2h0cx97tjks2p.cloudfront.net/blogs/wp-content/uploads/sites/2/2018/04/Collection-Framework-01.jpg)

## Need for Collection Framework

Before JDK 1.2, Java implemented collections with arrays, vectors and hashtables. The implementation of all these collections were defined independelty with no correlation among themselves as they had no common interface. So, the user had to remember different methods, syntax and constructors.

> With collection framework, Java mandated common implementations, constructors, destructor methods and error codes.

## Advantages

1. **Reduces Programming effort** by providing pre-defined Data Structures and algorithms.
2. **Increases Performance** by providing high-performance data structures.
3. **Provides interoperability between unrelated APIs** by establishing common language to pass collections back and forth.
4. **Fosters Software Reuse** by providing a standard interface for collections and algorithms.

## Hierarchy of Collection Framework

The Colletion framework extends the iterable interface at its root which is present in the Java.util package.

![Hierarchy of Java Collection framework]( ![1622634849527.png](./1622634849527.png)https://static.javatpoint.com/images/java-collection-hierarchy.png)

### Iterable interface

It's the root interface for all collection classes. It contains only one abstract method.

```
Iterator<T> iterator()
```

### Collection Interface

Collection interface is implemented by all classes in the collection framework. It declares the methods that every collection will have, thus building the foundation.

#### List Interface

This is one of the child interfaces of the Collection interface. It inhibits a list data structure to store ordered collection of objects. It can have duplicate values.

##### ArrayList

* Uses a dynamic array to store duplicate elements of different data types.
* It maintains the insertion order and is non-synchronized.
* Stored elements can be randomly accessed.

##### Linked List

* Uses a doubly linked list internally to store elements.
* It maintains the insertion order and is non-synchronized.
* Manipulation is fast since no shifting is required.

##### Vector

* Uses a dynamic array to store elements.
* Is synchronized and contains many methods that are not a part of Collection framework.

###### Stack

* Subclass of Vector.
* implements last-in-first-out data structure. i.e - *stack*
* Contains all vector class methods and also provides its own methods like push() and peek().

#### Queue Interface

1. An Ordered list used to hold elements which are about to be processed.
2. Queue maintains first-in-first-out order.

##### Priority Queue

* implements Queue interface
* It holds the elements/objects based on their priorities.
* It does not allow null values to be stored.

##### Deque

* Extends queue interface.
* Remove and add elements from both the side.
* Works as double-ended queue enabling operations on both ends.

###### ArrayDeque

* implements Deque interface.
* Faster than ArrayList and Stack with no capacity restrictions.

  `Deque ad = new ArrayDeque()`

#### Set Interface

* extends the Collection interface.
* represents the unordered set of elements
* It does not allow any duplicates, but at most a null value is allowed.

##### HashSet

* implements Set interface
* represents the collection that uses a hash table for storage.
* Uses hashing to store the elements.
* It contains Unique items

  `Set<Integer> s1 = new HashSet<Integer>`

##### LinkedHashSet

* Represents LinkedList implementation of Set.
* extends HashSet class and implements Set interface.
* Contains Unique elements.
* maintains the insertion order and permits null elements.

##### SortedSet Interface

* Alternate of Set interface that provides a total ordering of its elements.
* elements are arranges in the increasingg order.

###### TreeSet

* TreeSet Class implements the Set interface that uses a tree for storage.
* Contains unique elements.
* Access and retrieval time of TreeSet is quite fast.
* elements are stored in ascending order.
  `SortedSet<String> set = new TreeSet();`
