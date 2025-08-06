# Java_interview
oneshot
# ✅ Core Java Concepts

### Difference between JDK and JRE?

JDK (Java Development Kit) is a full-featured software development kit required to develop Java applications. It includes the JRE (Java Runtime Environment) and development tools like `javac`. JRE only provides the libraries and JVM to run Java applications, but not to develop them.

### Why is Java platform-independent?

Java is platform-independent because its compiler converts code into bytecode, which the JVM interprets. Since JVMs are available for all major platforms, the same bytecode can run on any system without modification.

### Difference between an abstract class and an interface?

* An abstract class can have both abstract and non-abstract methods.
* Interfaces can only have abstract methods (until Java 8), and static/default methods (from Java 8 onwards).
* A class can implement multiple interfaces but can only extend one abstract class.

### Difference between final, finally, and finalize?

* `final`: Used to declare constants, prevent method overriding or inheritance.
* `finally`: A block that always executes after try-catch, used for cleanup.
* `finalize()`: A method called by GC before destroying an object (deprecated now).

### Difference between stack and heap memory?

* **Stack**: Used for method execution and local variables; it's fast and managed by the JVM.
* **Heap**: Used for dynamic memory allocation of objects and classes; it's larger but slower.

### Difference between method overloading and method overriding?

* **Overloading**: Methods with the same name but different parameters in the same class.
* **Overriding**: Redefining a method from the superclass in the subclass with the same signature.

### Difference between a private and a protected modifier?

* `private`: Access only within the class.
* `protected`: Access within the same package and subclasses in other packages.

### What is constructor overloading in Java?

Constructor overloading means defining multiple constructors with different parameter lists to initialize objects in various ways.

### What is the use of the super keyword in Java?

`super` is used to refer to the immediate parent class. It's commonly used to call the superclass constructor or access parent class members.

### Difference between static methods, static variables, and static classes in Java?

* `static method`: Belongs to the class, not instances.
* `static variable`: Shared across all instances of the class.
* `static class`: Nested class that cannot access non-static members of the outer class.

### What exactly is System.out.println in Java?

`System` is a class, `out` is a static field of `PrintStream`, and `println()` is a method of `PrintStream`. So it prints to the console.

### What part of memory is cleaned in garbage collection?

Heap memory is cleaned during garbage collection, not the stack.

---

# 👨‍💻 Object-Oriented Programming

### What are the Object-Oriented Features supported by Java?

* Encapsulation
* Inheritance
* Polymorphism
* Abstraction

### What are different access specifiers used in Java?

* `private`: Only within class
* `default`: Package-private
* `protected`: Package + subclass
* `public`: Everywhere

### Difference between composition and inheritance?

* **Inheritance**: "Is-a" relationship.
* **Composition**: "Has-a" relationship. More flexible and promotes loose coupling.

### Purpose of an abstract class?

Used when we want to define a common base with some shared functionality and force subclasses to implement specific methods.

### Differences between a constructor and a method?

* Constructor is used to initialize objects; method is used for behavior.
* Constructor has no return type; method does.
* Constructor is called automatically; method must be called explicitly.

### What is the diamond problem and how is it solved?

The diamond problem arises in multiple inheritance. Java avoids it by not allowing multiple inheritance with classes. Interfaces with default methods are handled using rules of precedence.

### Difference between local and instance variables?

* **Local variables**: Defined within methods, limited scope.
* **Instance variables**: Defined in the class and accessible across methods using `this`.

### What is a Marker interface in Java?

A marker interface has no methods but is used to signal to the JVM or framework (e.g., `Serializable`).

---

# 📊 Data Structures and Algorithms

### Why are strings immutable in Java?

For security, caching, and thread-safety. Once created, a string cannot be modified, which ensures reliable behavior.

### Difference between creating String using new() and literal?

* **Literal**: Goes into the string pool and is reused.
* **new String()**: Creates a new object in heap memory even if it already exists in the pool.

### What is the Collections framework?

A unified architecture for representing and manipulating collections. Includes interfaces like `List`, `Set`, `Map` and classes like `ArrayList`, `HashSet`.

### Difference between ArrayList and LinkedList?

* `ArrayList`: Better for indexing, slower for inserts/deletes.
* `LinkedList`: Better for frequent insertions/deletions.

### Difference between a HashMap and a TreeMap?

* `HashMap`: Unordered, faster.
* `TreeMap`: Sorted by keys, slower.

### Difference between a HashSet and a TreeSet?

* `HashSet`: No order, faster.
* `TreeSet`: Sorted set, slower.

### Difference between an Iterator and a ListIterator?

* `Iterator`: One-directional traversal.
* `ListIterator`: Bidirectional traversal with extra functionalities.

### Purpose of the Comparable interface?

Used to define the natural ordering of objects (e.g., sorting via `Collections.sort()`).

### Purpose of the java.util.concurrent package?

It provides thread-safe collections, executors, atomic variables, and utilities for building concurrent applications efficiently.

---

# 🚨 Exception Handling

### What is an exception?

An exception is an event that disrupts the normal flow of a program during runtime.

### How does an exception propagate in Java?

If not caught, it propagates up the call stack until it is handled or terminates the program.

### Difference between checked and unchecked exceptions?

* **Checked**: Must be handled or declared (e.g., IOException).
* **Unchecked**: Run-time exceptions (e.g., NullPointerException).

### Use of try-catch block in Java?

It is used to catch exceptions and handle them gracefully to prevent abnormal termination.

### Difference between throw and throws?

* `throw`: Used to explicitly throw an exception.
* `throws`: Declares the exception in method signature.

### What is the use of the finally block?

Used to execute cleanup code that must run whether an exception occurs or not.

### What’s the base class of all exceptions?

`Throwable` is the root class. It has two main subclasses: `Exception` and `Error`.

### What is Java EE?

Java EE (Jakarta EE now) is a set of specifications for developing enterprise-level applications, including Servlets, JSP, EJB, and more.

### Difference between a Servlet and a JSP?

* **Servlet**: Java code in HTML.
* **JSP**: HTML in Java code. JSPs are more convenient for presentation, while servlets are better for control logic.

---

# 🧵 Multithreading

### What is a thread and its lifecycle stages?

A thread is a lightweight subprocess. Lifecycle: New → Runnable → Running → Blocked/Waiting → Terminated.

### Difference between a process and a thread?

A process is an independent program. Threads are parts of the same process sharing memory.

### Thread priorities in Java?

Priorities range from 1 (MIN) to 10 (MAX), with 5 being the default (NORM\_PRIORITY).

### What is context switching?

The process of storing and restoring the state of a thread so that execution can resume from the same point later.

### User thread vs Daemon thread?

* **User threads**: Keep the JVM alive.
* **Daemon threads**: Run in the background and die when all user threads finish.

### What is synchronization?

It ensures that only one thread accesses a shared resource at a time to avoid inconsistency.

### What is a deadlock?

A state where two or more threads are blocked forever, waiting for each other’s resources.

### Use of wait() and notify()?

They allow threads to communicate. `wait()` pauses a thread; `notify()` wakes up a waiting thread.

### Difference between synchronized and volatile?

* `synchronized`: Ensures atomicity and mutual exclusion.
* `volatile`: Ensures visibility of changes across threads but doesn’t guarantee atomicity.

### Purpose of sleep() method?

It pauses the thread for a specified duration without releasing the lock.

### Difference between wait() and sleep()?

* `wait()`: Used for inter-thread communication; releases the lock.
* `sleep()`: Just pauses; doesn’t release the lock.

### Difference between notify() and notifyAll()?

* `notify()`: Wakes one waiting thread.
* `notifyAll()`: Wakes all waiting threads on the object.

Intermediate
---------------------------------------------------------
🔹 JVM Internals
Q: What are the different class loaders in Java?
A: Java has three main class loaders:

* **Bootstrap ClassLoader** – Loads core Java classes from rt.jar.
* **Extension ClassLoader** – Loads classes from the ext directory.
* **Application ClassLoader** – Loads classes from the classpath (i.e., user-defined classes).

Q: What is the difference between Class.forName() and ClassLoader.loadClass()?
A:

* `Class.forName()` loads the class and initializes it (runs static blocks).
* `ClassLoader.loadClass()` loads the class but doesn't initialize it until explicitly needed.

Q: What is PermGen/Metaspace in Java?
A:

* **PermGen** (Permanent Generation) was used until Java 7 to store class metadata.
* In **Java 8**, it was replaced by **Metaspace**, which grows dynamically and stores class metadata outside the heap.

🔹 Memory Management
Q: Explain the memory structure of JVM.
A:

* **Heap** – Stores objects and class instances.
* **Stack** – Stores method calls and local variables.
* **Method Area (MetaSpace)** – Stores class metadata, static variables, and bytecode.
* **Program Counter Register** – Keeps track of the current instruction.
* **Native Method Stack** – For native (non-Java) code.

Q: What are strong, weak, soft, and phantom references?
A:

* **Strong**: Default reference, prevents GC.
* **Soft**: Collected only when memory is low.
* **Weak**: Collected during next GC cycle.
* **Phantom**: Collected but accessible via a reference queue, used for cleanup.

Q: How does Garbage Collection work? What are GC algorithms?
A:
GC reclaims memory by removing unused objects. Major algorithms:

* **Serial GC** – Single-threaded, for small apps.
* **Parallel GC** – Multi-threaded, high throughput.
* **CMS (Concurrent Mark Sweep)** – Minimizes pause times.
* **G1 (Garbage First)** – Splits heap into regions, balances pause time and throughput.
* **Java 11+**: ZGC, Shenandoah – Low latency collectors.

🔹 Advanced OOP Concepts
Q: What is method hiding in Java?
A: When a static method in a subclass has the same signature as in the superclass, it hides the superclass method. It’s not runtime polymorphism.

Q: Can we override a private or static method?
A:

* **Private methods** can’t be overridden as they are not inherited.
* **Static methods** are not overridden; they are hidden.

Q: What is covariant return type?
A: It allows an overridden method to return a subtype of the original method’s return type.

🔹 Design and Best Practices
Q: What is a Singleton class and how do you implement it?
A: A class with only one instance across the application.

```java
class Singleton {
    private static final Singleton instance = new Singleton();
    private Singleton() {}
    public static Singleton getInstance() {
        return instance;
    }
}
```

Q: Explain the Factory Design Pattern in Java.
A: The Factory Pattern provides an interface for creating objects but lets subclasses decide which class to instantiate. It promotes loose coupling.

Q: What is immutability? How to create an immutable class?
A:
Immutability means object state can’t change once created.
To make a class immutable:

* Make it final.
* Make fields private final.
* No setters.
* Return copies for mutable fields.

🔹 Generics
Q: What are generics in Java? Why are they used?
A:
Generics allow type-safe code and eliminate the need for casting.
Example: `List<String>` ensures only strings are added.

Q: What is type erasure in generics?
A:
At runtime, all generic type info is erased. `List<String>` and `List<Integer>` become just `List`.

Q: Difference between ? extends T and ? super T?
A:

* `? extends T`: Accepts subtypes of T — used for reading.
* `? super T`: Accepts supertypes of T — used for writing.

🔹 Java 8 Features
Q: What are functional interfaces?
A: Interfaces with only one abstract method. Example: Runnable, Comparator, Function.

Q: What is a lambda expression?
A: A concise way to represent a functional interface:

```java
(int a, int b) -> a + b
```

Q: What are Streams and how are they used?
A: Streams allow functional-style operations on collections.

```java
list.stream().filter(x -> x > 5).map(x -> x * 2).collect(Collectors.toList());
```

Q: What is the Optional class in Java?
A: A container object to represent nullable values and avoid NullPointerException.

🔹 Functional Programming
Q: Difference between map() and flatMap()?
A:

* `map()` transforms each element.
* `flatMap()` transforms and flattens nested structures.

Q: How do you use filter(), collect(), and reduce() in streams?
A:

* `filter()` – filters elements.
* `collect()` – terminal operation to gather results.
* `reduce()` – aggregates elements (e.g., sum).

🔹 Concurrency Enhancements
Q: What is the Executor framework?
A: It manages thread creation and reuse via ExecutorService.
Example: `Executors.newFixedThreadPool(5)`

Q: Difference between synchronized and ReentrantLock?
A:

* `synchronized` is simpler but less flexible.
* `ReentrantLock` provides better control (tryLock, fairness, interruptibility).

Q: Callable vs Runnable?
A:

* Runnable doesn't return a result or throw checked exceptions.
* Callable returns a value and can throw exceptions.

🔹 File I/O & Serialization
Q: Difference between Serializable and Externalizable?
A:

* Serializable is marker-based and uses default serialization.
* Externalizable lets you control serialization manually via `readExternal()` and `writeExternal()`.

Q: What happens if a serialized class has a non-serializable field?
A: A `NotSerializableException` is thrown unless the field is marked transient.

🔹 Annotations & Reflection
Q: What are annotations? Can you create custom annotations?
A: Annotations provide metadata. Yes, custom annotations are possible using `@interface`.

Q: How does reflection work in Java? What are its use cases?
A: Reflection allows inspection and manipulation of classes at runtime.
Use cases: frameworks (Spring), testing, serialization libraries.

🔹 Practical Coding
Q: How would you avoid a memory leak in Java?
A:

* Use weak references where applicable.
* Avoid static references to large objects.
* Close resources properly.
* Monitor heap usage with profilers.

Q: How would you handle concurrent modifications on a collection?
A:

* Use ConcurrentHashMap or CopyOnWriteArrayList.
* Use Collections.synchronizedList() for simple cases.
* Avoid modifying collections while iterating — use `iterator.remove()` if needed.

