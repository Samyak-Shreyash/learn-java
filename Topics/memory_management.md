## Memory in Java

When we talk about memory in Java, we talk about the memory in the JVM where objects and their references are stored. Similarly, memory Management in Java, is essentially the process of allocation and de-allocation of objects.

> But, as we know, both of these work automatically in Java. Then, why do we even care to know/worry about them..

> For the simple reason, that a good programmer is not just judged just by the code they write, but also, by knowing, how their code works.

![](https://cdn-images-1.medium.com/max/1200/1*9Gp_qFh0Nz22FmpSb8h2RQ.png)

JVM actually creates memory area with multiple data areas created by the thread during execution time. The memory areas are destroyed when JVM exits, whereas data areas are destroyed when the thread exits.

#### Native Method Stacks

Native Method Stacks is a specialized memory area only for those JVM versions which support native methods or C-methods. Created, when a thread is created, it can be fixed or dynamic in nature.

#### Program Counter(PC) Register

In Computer architecture terms, Program Counter Register tracks the current instruction executing at any given time. In Java, with the multi-threaded architecture of JVM, the PC Register is created at the instantiation of any new threads. PC keeps a pointer to the current statement that is being executed in that thread.

#### Method Area

Method Area is the part of the memory which is shared among all the threads. It is created during the creation of the JVM and is used to store class structures, constructors, super class name or interface names. It stores the fully qualified name to get proper references to these objects.

#### JVM Stack

Stack Memory is created during thread instantiation. It can be either fixed or dynamic in nature. It is allocated per thread and is used to store data and partial results. It contains heap objects’ references with certain visibility(till the life of that thread).

***Stack Frame *** is a data structure that contains the thread’s data. It represents the thread’s state in that current method. It is created at the invocation of the method. At any moment, only a single frame is active at any point in a given thread of control. It is called the current method and the frame is called current frame. The frame is local to the thread and cannot be referenced by other threads. The current method is stopped when another method is invoked or the current method completes.

#### Heap Area

It is created by the java runtime when the JVM starts and is used to allocate memory to objects and JRE classes. It can have fixed or dynamic size. When the new keyword is used, object is assigned a space in heap, and it’s (Strong Reference) stored in the stack. When the heap is full, garbage is collected.

References:

1. [java-heap-space-vs-stack-memory](https://www.journaldev.com/4098/java-heap-space-vs-stack-memory)
2. [memory-management-in-java](https://www.javatpoint.com/memory-management-in-java)
3. [Head First Java](https://www.amazon.in/Head-First-Java-Brain-Friendly-Guide/dp/8173666024)
