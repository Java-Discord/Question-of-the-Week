
# Question of the Week (ARCHIVED)
→ moved to https://pages.javadiscord.net/qotw

Questions and answers of all QOTW starting 28.03.2021 - This includes all answers, including wrong ones

## What is QOTW?
QOTW, or Question of the week, is a weekly java-related question you can answer and be awarded points for. Check it out in `#question-of-the-week` on the [Java Discord](javadiscord.net).

## Questions/Answers

 - [Week 21 (21.03.2021 - 28.03.2021)](#week21)  
 - [Week 22 (28.03.2021 - 04.04.2021)](#week22)
 - [Week 23 (05.04.2021 - 11.04.2021)](#week23)
 - [Week 24 (11.04.2021 - 18.04.2021)](#week24)
 - [Week 25 (18.04.2021 - 25.04.2021)](#week25)
 - [Week 26 (26.04.2021 - 02.05.2021)](#week26)
 - [Week 27 (02.05.2021 - 09.05.2021)](#week27)
 - [Week 28 (09.05.2021 - 16.05.2021)](#week28)
 - [Week 29 (16.05.2021 - 23.05.2021)](#week29)
 - [Week 30 (23.05.2021 - 30.05.2021)](#week30)

<a name="week21"></a>
### Week 21 (21.03.2021 - 28.03.2021) | What are the advantages of multithreading?

 - **Submission by dan1st#7327**

Singlethreaded programs can only execute one thing at a time. If multiple operations should be executed in parallel, it would be required to check for other operations constantly. If the thread blocks (because of e.g. I/O or a loop), the whole program blocks. This makes asynchronous I/O the only option for I/O operations with a single thread as the program cannot execute other operations while waiting for I/O. Also, multiple threads cab utilize multiple CPU cores and therefore speed up computations. This is very well described in the book `Java Concurrency in Practice`.

 - **Submission by Spider EveryOS#8098**

Threading takes advantages of the OS's scheduling processes and allows you to make multiple tasks appear as if they were running concurrently. Additionally, on systems with multiple cores, multi-threading may allow programs to leverage the power of multiple cores at once.

 - **Submission by OneWholesomeDev#7465**

Multithreading allows making use of simultaneous calculations and operations. Which means in certain cases and when used correctly, you may get better performance off a certain process or algorithm. Thus you can split the possible bottlenecking 100 % load for one thread down to multiple 40 % load-threads. - Can be faster - No bottleneck

 - **Submission by AttilaTheHun#9489**

Multithre_ding_ allows us to run numerous task simultaneously, which is extra useful when you need several tasks running at the same time, or when you are doing some blocking operations. However it is good to keep in mind that working with multiple threads can lead to some unexpected behavior, mainly if the threads are accessing the same resources. Multithreading is also used in brute-force algorithms to check all the cases in a shorter time, making them much more powerful.

---

<a name="week22"></a>
### Week 22 (28.03.2021 - 04.04.2021) | What are the main differences between Array and Collection?

 - **Submission by dan1st#7327**

[Arrays are a language feature that allows to store multiple elements of the same type (any type is allowed) in memory. Arrays have a fixed length.](https://docs.oracle.com/javase/specs/jls/se15/html/jls-10.html)
[`Collection`](https://docs.oracle.com/en/java/javase/11/docs/api/java.base/java/util/Collection.html) is an general purpose interface for data structures. It is part of the standard library and not part of the language itself. It is also not possible to just create a collection but only to create instances of concrete implementations of `Collection`.

An example of a Collection is ArrayList. ArrayList is a concrete List (special form of s collection) that uses arrays internally. ArrayList starts with no elements (by default) and allows to add elements at any point (the internal array id recreared when needed). While there is only a single array implementation, there a many different Collections for different purposes. Most of them have a variable length, some have a fixed/maximum length.

 - **Submission by Spider EveryOS#8098**

An array is a fixed-length data type which allows you to hold many objects.
A collection is a class that can be either fixed-length or variable-length. It also holds objects, but does so in a different way depending on the type of collection. For example, maps have both an index key and a value.
The syntactic method of accessing the two is different. Arrays can be indexed with the `[i]` syntax, while Collections are often indexed with getters, setters, and other auxiliary methods.

 - **Submission by Andrew.#3939**

Arrays are a fixed-size, contiguous block of memory that is allocated for storing primitives or objects, whereas the Java Collections Framework is a layer of abstraction that provides programmers with a set of pre-implemented data structures, some of which use arrays as their internal data storage medium. Arrays have a special bracket-syntax for accessing and setting the value of variables at specific points in the array, using integer indexes starting from zero and going to the size of the array - 1, whereas collections offer methods for data access instead. Generally, collections use more memory, but offer more functionality than arrays for the average developer.

 - **Submission by Dioxin#9863**

Arrays are low-level data structures, while collections are high-level data structures.

Although both are objects in Java, collections provide a more functional interface: you can `sort`, you can `clear()`, and you can query active elements using `size()` (which differs from array's `length`, which queries the fixed-size of the array).

Some of the functions that make collections more functional than arrays are `add`, `remove`, and `contains`.

---

<a name="week23"></a>
### Week 23 (05.04.2021 - 11.04.2021) | What is the difference between ScheduledExecutorService and ExecutorService interface?

 - **Submission by dan1st#7327**

`ExecutorService` is an interface that allows to run tasks asynchronously. The utility class `Executors` provides various methods for obtaining `ExecutorService`s.
`ScheduledExecutorService` is another interface that extends `ExecutorService`. It does not only allow to run tasks but it allows to run tasks after a specific amount of time passes or periodically. Objects of `ScheduledExecutorService` can also be executed using `Executors`, especially using `Executors.newScheduledThreadPool()` or similar.

 - **Submission by Dioxin#9863**

*due to the immense formatting I will just put a picture here*
![image of submission by Dioxin#9863](https://user-images.githubusercontent.com/66334318/114774615-a8462780-9d70-11eb-9b66-73d900f612ba.png)

 - **Submission by Ike#2932**
 
*this did not score a point btw*

One is scheduled and one is not

 - **Submission by Spider EveryOS#8098**

*Dynxsty thought about not counting this but decided to*

The scheduled version of the executor has a specified delay before the thread for the task is started.

---

<a name="week24"></a>
### Week 24 (11.04.2021 - 18.04.2021) | What is Encapsulation?

- **Submission by AL#3358**

In programming, data encapsulation refers to access to hidden data or information from outside. Prevent direct access to internal data structures, but via defined interfaces

- **Submission by Spider EveryOS#8098**

Encapsulation is how all fields should be marked as private because other classes should not be able to access or tamper with a class's internals. Instead, getters and setters should be used to query or change the state of an object.

More specifically:
Other classes should not know how a class operates, only that it does. The data is part of the object (not a global variable or something) so it stays in the object. This helps make management of software easily, as you don't have, say, the Keyboard class changing a float representing a tax rate. Class' data are their own to know, and they can define how their data is managed as they like.

- **Submission by dan1st#7327**

Encapsulation is the process of hiding implementation details. While a class needs to know its implementation details, they should not be exposed to other classes. This gives the programmer the flexibility to easily change the implementation details without changing other classes. For example, vectors could be represented like this:
```java
@Immutable
public class SimpleVector{
  private final int x;
  private final int y;
  public int getX(){
    return x;
  }
  public int getY(){
    return y;
  }
//other stuff
}
```

This vector can simply be changed to use polarized form if the developer i.e. thinks the class is more efficient for some operations:
```java
@Immutable
public class SimpleVector{
  private final int alpha;
  private final int len;
  public int getX(){
    return len*Math.cos(alpha);
  }
  public int getY(){
    returnlen*Math.sin(alpha);
  }
//other stuff
}
```

This would not be possible if the `x` and `y` values of the class were `public`. In that case, the variables `x` and `y` could not change without changing other classes that uses them.
Encapsulation is especially important when writing libraries and classes that should be used often as incompatibilities would be way worse in that case.

- **Submission by Future_vive#2953**

Encapsulation is one the four OOP princeples. it refers to data binding i.e, accessing data through methods - like encapsulating data into methods.

- **Submission by AttilaTheHun#9489**

Encapsulation is a core OOP thingy. It is the data hiding when you don't want others to manipulate your variables directly, but only via designated methods, such as getters and setters.

The purpose is that it looks good you don't need to care about the class in other places than in the class itself, you can always work with the designated methods.

---

<a name="week25"></a>
### Week 25 (18.04.2021 - 25.04.2021) | What are the differences between String and StringBuffer?


- **Submission by dan1st#7327**

`String` is an immutable class whose objects hold texts.
Instead of allowing modification, `Strings` have various methods for creating another, different `String`.

`StringBuilder` is a class that represents mutable `Strings`. It allows to e.g. append data or remove characters. It is not thread safe.

`StringBuffer` is a thread-safe variant of `StringBuilder`.

All of those classes implement `CharSequence`. `CharSequence` is an interface for objects representing a sequence of characters like the name suggests. CharSequence provides primitive methods for working with sequences of characters while the concrete classes allow for much more.


- **Submission by Spider EveryOS#8098**

A String is an immutable data type representing an immutable array of characters (in other words, "text"). It is similar to the `char*` and `char[]` constructs found in other languages, except that it is *immutable* (and cannot be changed).

A StringBuffer is a lot like the StringBuilder class, which I'm sure a lot of us have used. One big difference between the two, however, is that StringBuffer is thread-safe, and also much slower. A StringBuffer is a *mutable* dataclass that allows for creating a string by invoking a series of `.append(*)` calls, and then invoking `.toString()`. The initial capacity of a StringBuffer is set via the constructor.

- **Submission by daysling#6969**

Strings are immutable but StringBuffer are mutable.. Strings takes more memory, extends Object classes equals() where StringBuffer are fast and doesn't extend Object classes equals().


- **Submission by Loading BG#7962**

`String` is immutable - once set cannot be changed
`StringBuffer` is mutable - you can append and delete characters


- **Submission by Dioxin#9863**

`String` is an immutable collection of letters.

`StringBuffer` is a mutable synchronized collection of letters

`StringBuilder` is a mutable non-synchronized collection of letters, which is preferred over `StringBuffer` to improve performance when not accessed by multiple threads

---

<a name="week26"></a>
### Week 26 (26.04.2021 - 02.05.2021) | What is Context Switching?

- **Submission by dan1st#7327**

Context switching is when the CPU (actually a CPU core) switches from executing one thread to another. This requires to swap stacks and consumes time where the CPU (core) cannot do actual processing. When using a lot of threads and/or make threads block often, context switches are introduced which may harm performance. Threads could block because of I/O, timed waits or locking. In the case of locking, it could be avoided by using nonblocking algorithms or busy waiting (actually done by `synchronized` if the JIT thinks it is more efficient).
Project Loom aims to reduce the impact of context switching using fibers but this is still in development.
As with all performance topics:
> Premature optimization is the root of all evil
> 
Do not try to optimize everything. Mease where performance problems are, fix those and measure the change your fix made.

- **Submission by Dioxin#9863**

**Context Switching**
Allows a single CPU core to run multiple tasks by quickly switching between tasks.

A task is paused/suspended. The state of the task is stored to be resumed later. The CPU is then free to process another task. Eventually, the task suspends, and a previous task resumes.

When and how this occurs depends on the type of multit-tasking implemented.

**Cooperative Multitasking**
Tasks are in control of when tasks (themselves) suspend. A scheduler launches the program, then waits for the program to return control back to the scheduler.

Lightweight scheduler, used in embedded systems. However, it's possible for a single poorly written task to hog the CPU, causing the system to hang.

**Preemptive Multitasking**
A scheduler is in control of when tasks suspend. An interrupt system determines when to suspend a task. Tasks are suspended once they've exceeded the time slice assigned to them.

Heavier scheduler, used in modern desktop operating systems. Time slices ensure every tasks gets time to be processed.

- **Submission by Spider EveryOS#8098**

Context Switching is the OS's process of switching from one thread to another. When working within a single core, rarely can 2 threads truly run simultaneously. Instead, the OS must unload the execution data for one program and load the execution data for the other.
This is quite a bit lower level than Java, so I may be wrong, but if I understand correctly:
* Registers are backed up into memory for the current context
* Registers are loaded from memory for the new context. This includes things like (in general) EAX, EBX, ECX, EDX, (for the stack) EBP, ESP, and other registers I'm not aware of because I don't work this low level (I use Java ™️)
* After this, the EIP register needs set to the correct address to execute the code for the new context. You can't directly change the value stored by EIP, but my best guess on how this is done is via a well-place JMP instruction.
I am not sure how the processor forces a thread to yield control to the OS (to do this switching), but my best guess is that it would be via some sort of hardware interrupt on a repeating timer or something, which would give the OS control even if the thread was still running a task.

I could be totally off as, once again, I don't work at this level.

---

<a name="week27"></a>
### Week 27 (03.05.2021 - 09.05.2021) | What is the difference between JDK, JRE and JVM?

- **Submission by dan1st#7327**
*picture to keep formatting without interfering with markdown formatting*

![image](https://user-images.githubusercontent.com/66334318/117809674-be0b1780-b25e-11eb-968a-404c5dd7ea4f.png)


- **Submission by Spider EveryOS#8098**

JDK - The Java development environment contains tools essential to developing java applications. For example, it includes tools for compiling Java and generating JavaDocs. It also includes the JRE as an added touch.
JVM - The Java Virtual Machine allows for running Java bytecode. It is needed as a layer in between the machine and the code, since most physical machines cannot directly Java bytecode.
JRE - The Java Runtime Environment is what "normal" Java users install. It includes everything needed for a user to run a Java program, such as the files for the JVM, the Java package containing the default runtime libraries, any native files that are accessed from the default runtime libraries, and the default network security certificates.

- **Submission by The Next Guy ⬛🟧#7606**

The JVM, is the Java Virtual Machine. It processes byte codes into Machine Language of the architecture it's installed on and also manages garbage collection. The JRE is the Java Runtime Environment. It contains the JVM built for the architecture it's installed on. It allows running of java programs but not compilation. The JDK is the Java Development Kit. Like the JRE, it contains the JVM, but it also comes with compiler tools to create java and jni programs.

- **Submission by AttilaTheHun#9489**

Right, so JDK (Java Development Kit) is a set of tools and libraries you need to create and run Java programs, it contains stuff like compiler and jar builder, but also comes with JRE
JRE (Java Runtime Environment) is what actually runs the Java programs, it provides libraries and resources your program may need to work and also creates the JVM
JVM (Java Virtual Machine) is the byte-code executor, for computers are usually used to their kind of machine code and do not understand Java byte-code natively

- **Submission by Secret Agent X#0172**
  *obviously didn't score a point*

i have no idea

- **Submission by redmagic#5089**

JDK is java development kit has the libraries and tools you could call it the compiler for java, JRM is java runtime environment providing class libraries, and JVM is java virtual machine for running the language on any operating system

---

<a name="week28"></a>
### Week 28 (09.05.2021 - 16.05.2021) | What are the main uses of the super keyword?

- **Submission by Spider EveryOS#8098**

The `super` keyword allows for calling methods and constructors that have been overriden.
In a constructor, you can make a call to the any of the parent constructors, but it must be the first call of the constructor.
Additionally, you can make super calls to any of the superclass's methods via a super.methodCall(...), as long as you are currently in a non-static method or constructor.

- **Submission by  AttilaTheHun#9489**

The `super` keyword is used to access the superclass of the current class, for example if you would extend JFrame, you would need to call `super("Super Cool Window Title")` which calls the constructor of the super class JFrame. In android, your activity class usually extends Activity or AppCompatActivity or some other activity and in your `onCreate()` you need to call `super.onCreate()`.

Summary: `super` stand for superclass (the extended class) and allows you to access it

- **Submission by dan1st#7327** *image because of the formatting*

![image](https://user-images.githubusercontent.com/66334318/119236771-898a3c00-bb39-11eb-8fab-f685e0f5cd4c.png)

- **Submission by MeeseeksDev#7622**

The super word is used when referring to a parent class instanse

- **Submission by Therapy FC#1238**

Hello, so basically u use "super" when u wanna call the parent object of the one your working with , aka to access "superclass" Contrucctor

- **Submission by M1nordragon#9286**

The main use of the super keyword is running the contructor of an extended class.

- **Submission by daysling#6969**

super keyboard is a keyword in java which helps to inheriate properties/methods/working methods of superclass to the child class.

---

<a name="week29"></a>
### Week 29 (16.05.2021 - 23.05.2021) | What is the `Final` variable?

- **Submission by nyarian#7075**

it's a variable the value of which can't be changed after initialization

- **Submission by AttilaTheHun#9489**

Final variable is a variable that can not be reassigned, usually defining constants instead of the mythic `const` keyword.

Methods can be final, too, meaning they can not be overridden.

Be sure to use the `final` keyword closest with the variable name, such as `public static final int X...` so it sounds the cool Java way 😎

- **Submission by dan1st#7327**

The keyword `final` makes sure that a variable cannot be changed.
For objects, it only makes sure that the reference to the variable cannot be changed. In contrast to `const` in some other programming languages, `final` does not make objects immutable.
As `final` variables cannot change, they must be assigned before they are first accessed. This can happen with the declaration (for all variables), in a `static` block (for static variables), in a constructor or non-static initializer (for instance variables) or in all code branches between creation and first access of a local variable.
```java
final int i=0;
final List<String>list=new ArrayList<>();
//final int a;//compiler error (not initialized)
//i=1337;//compiler error
//i++;//compiler error
//list=new LinkedList<>()//compiler error
list.add("Hello");//allowed, does not modify the reference
```

*^ Comment by dynxsty:* 

![image](https://user-images.githubusercontent.com/66334318/119645167-06f5cb00-be1e-11eb-985d-470b160d0651.png)


- **Submission by daysling#6969**

Final keyword us a keyword in java that declare a variable/class as constant, final variables/classes can't be modified.

- **Submission by Spider EveryOS#8098**

When used on a variable, `final` just means that the reference is immutable (the reference cannot be changed). `final` variables and "effectively final" variables play nice with lambdas, whereas normal variables do not.
When used on a class, `final` means that the class may not be extended,
When used on a method, `final` means that said method cannot be overridden.

- **Submission by Cirax856#4026**

Final variable is a variable, that is in it's final state. It's value cannot be change by anything anywhere.

---

<a name="week30"></a>
### Week 30 (23.05.2021 - 30.05.2021) | What is the difference between `Compile-Time Polymorphism` and `Runtime Polymorphism`?

*no answers yet*
