### JavaSE 高级 之 多线程

- 简述线程、程序、进程的基本概念，以及他们的关系是什么？以及各自的优缺点？
- 说说并行与并发的区别？
  - 你的项目中有没有使用到并发？
- 为什么需要使用线程？
- 使用多线程可能带来的问题有哪些？
- 什么是上下文切换？
- 线程的基本状态以及状态图？请写出对应的Object方法

- 多线程有多少种实现方式？
  - 最常用的是那种？
  - Runnable和Callable接口的区别？
  - 为什么需要使用线程池
  - 执行execute()方法和submit()方法的区别是什么？
  - 知道线程池的实现原理吗？
  - JDK提供了哪些创建线程池的方法
  - 在实际工作中你是怎么使用线程池的？如何定义线程池的核心线程大小？
  - 知道ThreadPoolExecutor类吗？重要的参数知道吗？(给出代码实例)
    - ThreadPoolExecutor的饱和策略知道吗？
    - 能够手写一个线程池吗？
  - 生产上你如何设置合理线程池参数？
  - 知道线程池的启动策略吗？
  - 如何控制某个方法允许并发访问线程的个数？
  - 三个线程a、b、c并发允许，b、c需要a的线程是怎么实现的？
- 公平锁/非公平锁/可重入锁/递归锁/自旋锁谈谈你的理解？请手写一个自旋锁
- CountDownLatch/CyclicBarrier/Semaphore 使用过吗？

- 什么是线程死锁？如何避免死锁？请写出一个死锁的案例
- 知道阻塞队列吗？
  - 为什么用？有什么好处？
  - BlockingQueue的核心方法知道吗？
  - 阻塞队列的应用知道吗？
  - 你知道哪些阻塞队列？都是怎么实现的？
- 说说sleep()方法和wait()方法的区别和共同点
- 为什么调用start()方法会执行run()方法。为啥不直接调用run()方法
- synchronized 关键字
  - 自己使用到了synchronized了嘛？
  - synchronized 的三种使用方式知道嘛？
  - 知道 synchronized 的底层原理吗？
  - 说一下JDK1.6之后对synchronized 关键字底层做了哪些优化？可以介绍一下这些优化吗？
  - 除了synchronized ，你了解ReentrantLock的吗？
  - synchronized 和 ReentrantLock的区别你知道吗？
  - 你知道可重入锁和不可重入锁吗
- volatile关键字的理解
  - JMM内存模型了解吗？
  - 并发编程的三个重要特性volatile满足了哪些？
  - volatile和synchronized的区别你知道吗？
- 你知道 ThreadLocal吗？
  - 你能否给出ThreadLocal的案例代码吗？
  - 你知道ThreadLocal的底层原理吗？
  - 了解ThreadLocal的内存泄露问题吗？
- 你有没有使用jps和jstack定位死锁？请给出具体的截图流程和文字说明
- 知道Atomic原子类吗？请介绍一下Atomic原子类
- JUC包中的原子类是哪四类？
  - 讲讲各自原子类的使用？
  - 能不能讲一下AtomicInteger的原理？
- 知道AQS吗？
  - AQS原理是什么？
  - AQS对资源的共享方式
  - 请整理一下AQS组件总结
- 同一个类中的2个方法都加了同步锁，多个线程能同时访问同一个类中的这两个方法吗？
- 说出同步线程个线程调度相关的方法