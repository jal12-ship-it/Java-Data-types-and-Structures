# Java data type and data structures

## Data Types

Data types in programming languages helps the compiler or the interpreter understand how the programmer intends to use the data. It is a classification of data. A variable in Java must be a specified data type. Like many other programming languages, Java also supports various types of data, including integer, real, character, string, and Boolean. Data types in Java are classified into two:

1. Primitive Data Types
2. Non-Primitive Data Types

![Data types in Java](https://1.bp.blogspot.com/-65HLAHaShcY/XZ3iXu324eI/AAAAAAAAAPY/EX6ZZyWxZZwqJX9sUtL5dxMGm8PzVsQWgCEwYBhgL/s1600/datatype.png)

### Primitive Data Type

These are the most basic data types available in the Java language that specifies the size and type of variable values. They are single valued and have no additional methods. There are 8 primitive data types that can be divided into two:

#### Integer

##### byte (1 byte)

Byte data type is an 8-bit signed two's complement integer. The value of byte ranges from -128 to 127 with 0 as its default value. Due to such small range byte data type is used in large arrays where memory saving is required.
Syntax

```java
byte byteVar = 127;
byteVar++;
System.out.println(byteVar)
```

If the value of byteVar is incremented by 1 it overflows and sets the value to -128.

##### short (2 bytes)

The short data type is a 16-bit signed two's complement integer. The value ranges from -32,768 to 32,767 and its default value is 0. Just like byte, short can also be used to save memory.
Syntax

```java
short shortVar;
```

##### int (4 bytes)

The int data type is a 32-bit signed two's complement integer. The value ranges from -2147483648 to 2147483647 and its default value is 0. In general, int is used to create numeric variables.

```java
int intVar;
```

##### long (8 bytes)

The int data type is a 64-bit signed two's complement integer. The value ranges from -9223372036854775808 to 9223372036854775807 and its default value is 0. This is used when int is not large enough to store the value.

```java
long longVar;
```

#### Float

##### float (4 bytes)

The float data type is a single-precision 32-bit IEEE 754 floating-point. It can store values upto 7 decimal digits and its default value is 0.0f. To save memory in large arrays of floating point numbers float is used instead of double.

```java
float floatVar = 0.06f;
```

##### double (8 bytes)

The double data type is a double-precision 64-bit IEEE 754 floating point. It can store values upto 16 decimal digits and its default value is 0.0d. In general, double is used for decimal values.

```java
double doubleVar = 1.99d;
```

> It is recommended not to use float and double for precise values as they were designed especially for scientific calculations where approximation errors are acceptable.

#### Character

##### char (2 byte)

The char data type is a single 16-bit Unicode character. The value ranges from ‘\u0000’ (0) to ‘\uffff’ (65535) and the default value is ‘\u0000’. It stores a single character.

```java
char charVar = 'A';
```

#### Boolean

##### boolean (1 bit)

The boolean data type specifies only 1 bit of information but its size is virtual machine dependent. The value is either true or false and default value is false.

### Non-Primitive Data Types (Reference Variables or Object References)

Reference data types holds a memory address of variable values while primitive data type holds the value itself in the memory. Hence, they are called reference data types as they refer to objects. Also these are not pre-defined as that of primitive data types(except String).

#### Classes

A class is a user defined prototype used to create objects. It describes the set of properties or methods that are common to all objects of the same type. It contains fields and methods that represent the behaviour of an object. A class gets invoked by the creation of the respective object.

```java
public class MyClass {
    int someVar = 100; //This is a field
    public String name = "My name"; //This is also a field

    //This is a method
    public int someMethod() {
        return 1;
    }
}
```

#### Interfaces

An interface is declared like a class. The key difference is that the interface contains methods that are abstract by default; they have nobody.

```java
interface printable {  
    void print();  
}  
class A1 implements printable {  
    public void print()
    {
        System.out.println("Hello");
    }   
    public static void main(String args[]) {  
        A1 obj = new A1();  
        obj.print();  
    }  
}
```

#### Strings

The String data type stores a sequence or array of characters. A string is a non-primitive data type but it is predefined in Java. String literals are enclosed in double-quotes.

```java
class Main {
  public static void main(String[] args) {
 
    // create strings
    String string = "Java String Data type";
 
    // print strings
    System.out.println(S1);   
  }
}
```

#### Arrays

An array is used to hold elements of the same type. It is an object in java, and the array name (used for declaration) is a reference value that carries the base address of the continuous location of elements of an array.

```java
int Array_Name = new int[7];
```

## Data Structures in Java

Data structure is a way of storing and organizing data. Data structure provide a way to process and store data efficiently.

![Data Structers in Java](https://d1m75rqqgidzqn.cloudfront.net/wp-data/2022/07/22114048/image-6.png)

1. Linear Data Structures: It is a single level data structure in which all elements are arranged in sequential order.  
2. Non-Linear Data Structures: These are multi-level data structures in which data is not arranged in sequential order.

![Linear vs non-linear](https://d1m75rqqgidzqn.cloudfront.net/wp-data/2022/07/22120317/image-7.png)

### Linear Data Structures

#### Array

Array is linear data structure which stores fixed number of similar elements. Array can store primitive data types as well as object but it should be of same kind. This is one of most used data structures in java.

To declare a new string array:

```java
String[] strArr = new String[10];
```

Here, String is data type, strArr is variable name and 10 is size of the array

Arrays can be of:

1. Single Dimensional Arrays
2. Two-Dimensional Arrays
3. Multi-Dimensional Arrays

![Example of a 1D array in java](https://www.edureka.co/blog/wp-content/uploads/2018/01/7-2.png)

Advantages

- Can randomly access array elements using index
- It represents multiple elements of same type with single name
- Can implement various data strucures such as LinkedList, Stack and Queue using Array

Disadvantages

- Need to know number of elements in advance.
- Can not modify array once its size is defined
- Insertion and deletion are costly operation in array.

#### Stack (To store data one on the other)

A stack is a Last In First Out (LIFO) data structure that can be implemented physically as an array or a linked list. It simply has one pointer, top, which points to the stack's topmost element. When a new element is added to the stack, it is placed at the top, and the element can only be removed from the stack. To put it another way, a stack may be thought of as a container in which insertion and deletion can be done from one end.

Common Operations on stack are:

1. Push()- To add an item to the top of the stack
2. Pop()- To remove an item from the top of the stack
3. Peek()- It tells us what is on the top of the stack without removing it.
4. isEmpty()- This method returns true if stack is empty else, returns false.

![Example of a stack in Java](https://www.callicoder.com/static/b55c9fdd2a75568271a20da5f0ec675f/d22c2/java-stack-data-structure.jpg)

Advantages of Stack

- Stack manages the data in a LIFO method, which is not possible with a linked list and array.
- Local variables are stored in a stack when a function is called, and automatically get destroyed once returned.
- You can use Stack to manage how memory is allocated and deallocated.
- Stack is more secure and reliable since it does not easily get corrupted.
- Stack does not allow resizing of variables.

Disadvantages of Stack

- Stack overflow can occur if you create too many objects on the stack.
- When variable storage is overwritten, the function or programme can sometimes behave in an unpredictable manner.
- Stack memory is limited.
- Data cannot be randomly accessed in a stack.

(+Operations: push(ele), pop(), isEmpty(), peek())

#### Queue

A queue is a data structure that follows the FIFO (First-In-First-Out) principle, in which elements are added to the end of the list and removed from the beginning.

Common operations on queue are:

1. Enqueue()- Adding elements at the rear end of the queue.
2. Dequeue()- Deleting elements from the front end of the queue.

![Queues in Java](https://jenkov.com/images/java-collections/java-queue.png)

Advantages of Queue
Queues have the benefit of being able to handle a variety of data types while also being flexible and quick. In addition, queues have the potential to be infinitely long, as opposed to fixed-length arrays.

Disadvantage of Queue
A major disadvantage of a classical queue is that a new element can only be inserted when all of the elements are deleted from the queue.

There are two popular variations of queues:

##### Circular Queues

Circular Queues are the queues implemented in circle form rather than a straight manner. Circular queues overcome the problem of unutilized space in the linear queues that we implement as arrays.

![circular-queue](https://user-images.githubusercontent.com/60174007/183363568-a366e84c-2b05-4024-9219-e89e9a2ed34f.png)

##### Deque

A double-ended queue or a deque is a refined queue in which can add or remove the elements at either end but not in the middle.

![Deque-in-Java](https://media.geeksforgeeks.org/wp-content/uploads/anod.png)

#### Linked List

The LinkedList class, just like the ArrayList, is a collection that can hold numerous items of the same type. Here the elements are not stored in contiguous locations and each element is a separate object with a data part and address part. Each element is known as a node and is linked using pointers and addresses.

Linked List is a part of the Collection framework present in java.util package.

Two types of Linked lists:

1. Single Linked List-  Singly linked list allows traversal elements only in one way.
2. Double Linked List- Doubly linked list allows element two way traversal.

![Exaample of a linked list in Java](https://4.bp.blogspot.com/-GZA5JUSRXMw/VovF9Z8etWI/AAAAAAAAEgQ/8uFzxgqAS48/w1200-h630-p-k-no-nu/Singly%2Blinked%2Blist%2Band%2Bdoubly%2Blinked%2Blist%2Bin%2BJava.jpg)

Advantages of Linked List

- The linked list is a dynamic data structure. We can allocate and deallocate the memory at run-time itself.
- The node can be easily inserted or deleted using the insertion and deletion function.
- The linked list makes good use of memory. Because we don't have to allocate memory ahead of time.
- It has an extremely rapid access time and can be accessed at a specific time without any memory overhead.
- Linear data structures like stack and the queue can be easily used linked list.

Disadvantages of Linked List

- As each node of the linked list points to a pointer, it requires more memory to store the elements than an array.
- Traversing the nodes of a linked list is quite tough. We won't be able to access any node at random in this case.(As we do in the array by index.)
- In a linked list, reverse traversing is harder since the pointer demands extra memory.

### Non-Linear Data Structures

#### Trees (Hierarchical Fashion)

Tree is a hierarchical data structure that stores the information naturally in the form of a hierarchy style. It is one of the most powerful and advanced data structures which is a non-linear compared to arrays, linked lists, stack, and queue. It represents the nodes connected by edges.

Terms used in tree data structure:

1. Root- It is the first top-level node. The entire tree is referenced through it. It does not have a parent.
2. Parent Node- Parent node is an immediate predecessor of a node
3. Child Node- All immediate successors of a node are its children
4. Siblings- Nodes with the same parent are called Siblings
5. Path- Path is a number of successive edges from the source node to the destination node
6. Height of Node- Height of a node represents the number of edges on the longest path between that node and a leaf
7. Height of Tree- Height of tree represents the height of its root node
8. Depth of Node- Depth of a node represents the number of edges from the tree’s root node to the node
9. Edge- Edge is a connection between one node to another. It is a line between two nodes or a node and a leaf

![Tree structure](https://examples.javacodegeeks.com/wp-content/uploads/2019/12/1.jpg.webp)

##### Binary Tree

Binary tree is the type of tree in which each parent can have at most two children. The children are referred to as a left child or right child. This is one of the most commonly used trees. When certain constraints and properties are imposed on the Binary tree it results in a number of other widely used trees like BST (Binary Search Tree), AVL tree, RBT tree etc.

![Binary Tree structure](https://examples.javacodegeeks.com/wp-content/uploads/2019/12/binary-search-tree-768x528.jpg.webp)

##### Binary Search Tree

A BST is a binary tree where nodes are ordered in the following way:

- The value in the left subtree are less than the value in its parent node
- The value in the right subtree are greater than the value in its parent node
- Duplicate values are not allowed.

##### AVL Tree

AVL tree is a self-balancing binary search tree. The name AVL is given on the name of its inventors Adelson-Velshi and Landis. This was the first dynamically balancing tree. In AVL tree, each node is assigned a balancing factor based on which it is calculated whether the tree is balanced or not. In AVL tree, the heights of children of a node differ by at most 1. The valid balancing factors in AVL trees are 1, 0 and -1. When a new node is added to the AVL tree and tree becomes unbalanced then rotation is done to make sure that the tree remains balanced. The common operations like lookup, insertion and deletion take O(log n) time in AVL tree. It is widely used for Lookup operations.

##### Red-Black Tree

Red-Black is another type of self-balancing tree. The name Red-Black is given to it because each node in a Red-Black tree is either painted Red or Black according to the properties of the Red- Black Tree. This makes sure that the tree remains balanced. Although the Red-Black tree is not a perfectly balanced tree but its properties ensure that the searching operation takes only O(log n) time. Whenever a new node is added to the Red-Black Tree, the nodes are rotated and painted again if needed to maintain the properties of the Red-Black Tree .

#### Graph (Connected Nodes)

A graph is a data structure for storing connected data like a network of people on a social media platform. Vertices and edges make up a graph. The entity (for example, people) is represented by a vertex, and the relationship between entities (for example, a person's friendships) is represented by an edge.

![Graphs in Java](https://miro.medium.com/max/700/1*PRSdO4485XYMPbmy7PgHnQ.jpeg)

Advantage of Graph
The fundamental benefit of a graph data structure is that it allows you to use all graph-related computer science algorithms. You can use all of the power of graph algorithms to solve your problem once you've worked out how to represent your domain logic as a graph.

Disadvantage of Graph
The main disadvantage is its large memory complexity.

Graph Data Structures in Java can be classified on the basis of two parameters: direction and weight.

1. Direction
    - Directed- A directed graph is a set of nodes or vertices connect together with each other and all the edges have a direction from one vertex to another. There is a directed edge for each connection of vertices.
    - Undirected- An undirected graph is a set of nodes or vertices which are connected together, with no direction.
2. Weight
    - Weighted- A weighted graph is a graph in which the weight is present at every edge of the graph. A weighted graph is also a special type of labeled graph.
    - An unweighted graph is the one in which there is no weight present on any edge.

## Refrences

<https://press.rebus.community/programmingfundamentals/chapter/data-types/>
<https://techvidvan.com/tutorials/data-structure-in-java/>
<https://www.geeksforgeeks.org/>
<https://www.javatpoint.com/>
<https://www.w3schools.com/>
<https://examples.javacodegeeks.com/>

