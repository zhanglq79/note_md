- [基本语法](#%e5%9f%ba%e6%9c%ac%e8%af%ad%e6%b3%95)
  - [Java基本类型和大小](#java%e5%9f%ba%e6%9c%ac%e7%b1%bb%e5%9e%8b%e5%92%8c%e5%a4%a7%e5%b0%8f)
  - [值传递和引用传递区别, Java中有引用传递么?](#%e5%80%bc%e4%bc%a0%e9%80%92%e5%92%8c%e5%bc%95%e7%94%a8%e4%bc%a0%e9%80%92%e5%8c%ba%e5%88%ab-java%e4%b8%ad%e6%9c%89%e5%bc%95%e7%94%a8%e4%bc%a0%e9%80%92%e4%b9%88)
  - [创建线程的方法](#%e5%88%9b%e5%bb%ba%e7%ba%bf%e7%a8%8b%e7%9a%84%e6%96%b9%e6%b3%95)
  - [静态代理&动态代理](#%e9%9d%99%e6%80%81%e4%bb%a3%e7%90%86%e5%8a%a8%e6%80%81%e4%bb%a3%e7%90%86)
  - [为什么String设计成不可变的](#%e4%b8%ba%e4%bb%80%e4%b9%88string%e8%ae%be%e8%ae%a1%e6%88%90%e4%b8%8d%e5%8f%af%e5%8f%98%e7%9a%84)
- [并发](#%e5%b9%b6%e5%8f%91)
  - [Lock和synchronized的区别：](#lock%e5%92%8csynchronized%e7%9a%84%e5%8c%ba%e5%88%ab)
  - [volatile关键字的作用](#volatile%e5%85%b3%e9%94%ae%e5%ad%97%e7%9a%84%e4%bd%9c%e7%94%a8)
  - [Java中有哪些线程池类型, 适合什么场景](#java%e4%b8%ad%e6%9c%89%e5%93%aa%e4%ba%9b%e7%ba%bf%e7%a8%8b%e6%b1%a0%e7%b1%bb%e5%9e%8b-%e9%80%82%e5%90%88%e4%bb%80%e4%b9%88%e5%9c%ba%e6%99%af)
- [JVM](#jvm)
  - [JVM内存结构](#jvm%e5%86%85%e5%ad%98%e7%bb%93%e6%9e%84)
  - [JMM线程模型](#jmm%e7%ba%bf%e7%a8%8b%e6%a8%a1%e5%9e%8b)
  - [JVM内存模型](#jvm%e5%86%85%e5%ad%98%e6%a8%a1%e5%9e%8b)
  - [静态链接&动态链接](#%e9%9d%99%e6%80%81%e9%93%be%e6%8e%a5%e5%8a%a8%e6%80%81%e9%93%be%e6%8e%a5)
- [设计模式](#%e8%ae%be%e8%ae%a1%e6%a8%a1%e5%bc%8f)
  - [手写单例模式，特别是双重检验锁以及静态内部类](#%e6%89%8b%e5%86%99%e5%8d%95%e4%be%8b%e6%a8%a1%e5%bc%8f%e7%89%b9%e5%88%ab%e6%98%af%e5%8f%8c%e9%87%8d%e6%a3%80%e9%aa%8c%e9%94%81%e4%bb%a5%e5%8f%8a%e9%9d%99%e6%80%81%e5%86%85%e9%83%a8%e7%b1%bb)
  - [手写工厂模式](#%e6%89%8b%e5%86%99%e5%b7%a5%e5%8e%82%e6%a8%a1%e5%bc%8f)
  - [理解 MVC，结合 SpringMVC 回答](#%e7%90%86%e8%a7%a3-mvc%e7%bb%93%e5%90%88-springmvc-%e5%9b%9e%e7%ad%94)
  - [理解代理模式，结合 Spring 中的 AOP 回答](#%e7%90%86%e8%a7%a3%e4%bb%a3%e7%90%86%e6%a8%a1%e5%bc%8f%e7%bb%93%e5%90%88-spring-%e4%b8%ad%e7%9a%84-aop-%e5%9b%9e%e7%ad%94)
  - [分析 JDK 中常用的设计模式，例如装饰者模式、适配器模式、迭代器模式等](#%e5%88%86%e6%9e%90-jdk-%e4%b8%ad%e5%b8%b8%e7%94%a8%e7%9a%84%e8%ae%be%e8%ae%a1%e6%a8%a1%e5%bc%8f%e4%be%8b%e5%a6%82%e8%a3%85%e9%a5%b0%e8%80%85%e6%a8%a1%e5%bc%8f%e9%80%82%e9%85%8d%e5%99%a8%e6%a8%a1%e5%bc%8f%e8%bf%ad%e4%bb%a3%e5%99%a8%e6%a8%a1%e5%bc%8f%e7%ad%89)


## 基本语法
### Java基本类型和大小
- byte: 1字节
- short: 2字节
- int: 4字节, 大小刚好超过20亿
- long: 8字节
- float: 4字节
- double: 8字节
- boolean: 1字节
- char: 2字节

### 值传递和引用传递区别, Java中有引用传递么?
结论: Java中没有引用传递, 只有值传递.

### 创建线程的方法
Runable和Callable的区别是什么?

### 静态代理&动态代理

### 为什么String设计成不可变的
- 因为String在Java中是不可变的。Java运行时环境可以节省大量的堆空间，因为不同的String变量可以引用池中的相同String变量。如果String不是不可变的，那么String缓冲池失去作用，因为任何变量已经改变了值，它也会反映在其他变量中。
- 如果String是可变的，那么它将对应用程序造成严重的安全威胁。例如，数据库用户名，密码作为String传递以获取数据库连接，并在套接字编程主机和端口详细信息中作为String传递。由于String是不可变的，因此无法更改其值，否则任何黑客都可能更改引用的值以导致应用程序中出现安全问题。
- 由于String是不可变的，因此对于多线程是安全的。可以跨不同的线程共享单个String实例。这避免了使用同步来保证线程安全。字符串是隐式线程安全的。
- 字符串在java类加载器中使用，不可变性提供了安全性，类由Classloader加载。例如，假设尝试加载java.sql.Connection类的实例，但引用的值更改为myhacked.Connection类，可以对数据库执行不需要的操作。
- 由于String是不可变的，因此在创建时缓存它的哈希码，不需要再次计算。这使得它成为Map中键的一个很好的候选者，它的处理速度比其他HashMap键对象快。这就是String是最广泛用作HashMap键的原因

## 并发
### Lock和synchronized的区别：
- Lock是一个接口，而synchronized是Java中的关键字，synchronized是内置的语言实现, synchonized在编译时用管程实现了互斥和同步
- synchronized在发生异常时，会自动释放线程占有的锁，因此不会导致死锁现象发生；而Lock在发生异常时，如果没有主动通过unLock()去释放锁，则很可能造成死锁现象，因此使用Lock时需要在finally块中释放锁；
- Lock可以让等待锁的线程响应中断，而synchronized却不行，使用synchronized时，等待的线程会一直等待下去，不能够响应中断；
- 通过Lock可以知道有没有成功获取锁，而synchronized却无法办到。
- Lock可以提高多个线程进行读操作的效率。
- 在性能上来说，如果竞争资源不激烈，两者的性能是差不多的，而当竞争资源非常激烈时（即有大量线程同时竞争），此时Lock的性能要远远优于synchronized。所以说，在具体使用时要根据适当情况选择。

### volatile关键字的作用
并发的三个概念: 原子性, 有序性, 

保证线程之间的可见性和运行的有序性(禁止指令重排). 可见性 被修饰的变量,线程取变量要从主存取,计算完直接写入主存而不是高速缓存.(在jmm中定义的8种操作中, 即是read前紧跟load, store后紧跟write). 可见性的保证, 通过jit编译的代码反汇编可以看到在对volatile变量的赋值后紧跟一个lock指令, 这个指令相当于内存屏障, 将数据写回主存同时让其他处理器的高速缓存中中的该值失效. 另一方面, 由于Happen-before原则的存在, 可以通过volatile关键字实现捎带同步, 是比cas更加轻量和tricky的同步方式. 用volatile同步的限制场景是变量值不依赖原值. 例如累加就不可以用其实现.

### Java中有哪些线程池类型, 适合什么场景
- newCachedThreadPool()，它是一种用来处理大量短时间工作任务的线程池
- newFixedThreadPool(int nThreads)，重用指定数目（nThreads）的线程，其背后使用的是无界的工作队列
- newSingleThreadExecutor()，它的特点在于工作线程数目被限制为 1，操作一个无界的工作队列
- newSingleThreadScheduledExecutor() 和 newScheduledThreadPool(int corePoolSize)，创建的是个 ScheduledExecutorService
- newWorkStealingPool(int parallelism)
- 自定义的ThreadPoolExecutor(int corePoolSize, int maximumPoolSize, long keepAliveTime, TimeUnit unit, BlockingQueue<Runnable> workQueue, ThreadFactory threadFactory, RejectedExecutionHandler handler)

## JVM
### JVM内存结构

### JMM线程模型

### JVM内存模型

### 静态链接&动态链接

## 设计模式

### 手写单例模式，特别是双重检验锁以及静态内部类

```java
//饿汉模式
public class EagleSingleton {
  private static EagleSingleton INSTANCE;
  static {
    INSTANCE = new EagleSingleton();
  }
  private EagleSingleton() {

  }

  public static EagleSingleton getInstance() {
    return INSTANCE;
  }
}

// 懒汉模式 DCL
public class LazzySingleton {
  private static volatile LazzySingleton INSTANCE;
  private LazzySingleton() {

  }
  public static LazzySingleton getInstance() {
    if (INSTANCE == null) {
      synchronized(LazzySingleton.class) {
        if (INSTANCE == null) {
          INSTANCE = new LazzySingleton();
        }
      } 
    }
    return INSTANCE;
  }
}

```

### 手写工厂模式

### 理解 MVC，结合 SpringMVC 回答

### 理解代理模式，结合 Spring 中的 AOP 回答

### 分析 JDK 中常用的设计模式，例如装饰者模式、适配器模式、迭代器模式等




