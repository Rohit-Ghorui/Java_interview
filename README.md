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
