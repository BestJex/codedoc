# 总

### 1）常见的集合有哪些？

###### Map接口和Collection接口是所有集合框架的父接口

- Collection接口的子接口包括：Set接口和List接口
- Map接口的实现类主要有：HashMap、TreeMap、Hashtable、ConcurrentHashMap以及Properties等
- Set接口的实现类主要有：HashSet、TreeSet、LinkedHashSet等
- List接口的实现类主要有：ArrayList、LinkedList、Stack以及Vector等

1. ArrayList底层是数组。

2. LinkedList底层是双向链表。

3. HashMap底层与HashTable原理相同，Java 8版本以后如果同一位置哈希冲突大于8则链表变成红黑树。

4. HashTable底层是链地址法组成的哈希表（即数组+单项链表组成）。

5. HashSet底层是HashMap。

6. LinkedHashMap底层修改自HashMap，包含一个维护插入顺序的双向链表。

7. TreeMap底层是红黑树。

8. LinkedHashSet底层是LinkedHashMap。

9. TreeSet底层是TreeMap。

   ### 2) HashMap与HashTable的区别？

   > 1. HashMap没有考虑同步，是线程不安全的；Hashtable使用了synchronized关键字，是线程安全的；
   > 2. HashMap允许K/V都为null；后者K/V都不允许为null；

   ### 3) ConcurrentHashMap和Hashtable的区别？

   > ConcurrentHashMap 结合了 HashMap 和 HashTable 二者的优势。HashMap 没有考虑同步，HashTable 考虑了同步的问题。但是 HashTable 在每次同步执行时都要锁住整个结构。 ConcurrentHashMap 锁的方式是稍微细粒度的。

   ### 4)ConcurrentHashMap实现原理

   - JDK1.7 : 【数组（Segment） + 数组（HashEntry） + 链表（HashEntry节点）】

   > - ConcurrentHashMap（分段锁） 对整个桶数组进行了分割分段(Segment)，每一把锁只锁容器其中一部分数据，多线程访问容器里不同数据段的数据，就不会存在锁竞争，提高并发访问率。
   > - Segment是一种可重入锁ReentrantLock，在ConcurrentHashMap里扮演锁的角色，HashEntry则用于存储键值对数据。

   - JDK1.8 : Node数组+链表 / 红黑树

   > - 利用CAS+Synchronized来保证并发更新的安全，底层依然采用数组+链表+红黑树的存储结构。

   ### 5) ArrayList 和 Vector 的区别？

   > - Vector 是线程安全的,ArrayList 是线程不安全的。
   > - Vector在数据满时增长为原来的两倍，而 ArrayList在数据量达到容量的一半时,增长为原容量的1.5倍。

   ### 6) ArrayList和LinkedList的区别？

   > - LinkedList基于链表的数据结构；ArrayList基于动态数组的数据结构
   > - LinkedList 在插入和删除数据时效率更高，ArrayList 查询效率更高；

   ### 7) HashMap 默认的初始化长度是多少？

   - 在JDK中默认长度是16，并且默认长度和扩容后的长度都必须是 2 的幂。

   ### 8) HashMap 构造方法中初始容量、加载因子的理解

   - 初始容量代表了哈希表中桶的初始数量，即 Entry< K,V>[] table 数组的初始长度
   - 加载因子是哈希表在其容量自动增加之前可以达到多满的一种饱和度百分比，其衡量了一个散列表的空间的使用程度，负载因子越大表示散列表的装填程度越高，反之愈小。

## 一、Map

### 1.HashMap
#### （1）LinkedHashMap

### 2.SortedMap

#### （1）TreeMap

#### （2）NavigableMap

### 3.Hashtable

#### （1）Properties

## 二、Collection

### 1.List

#### (1) ArrayList

#### (2) LinkedList

#### (3) Vector

### 2.Set

#### (1) HashSet

#### (2) SortedSet

#### (3) TreeSet

#### (4) KeySet

## 三、Iterator

### 1.ListIterator

## 四、Collections

## 五、Collections

## 六、Enumeration
###  JavaSE 高级 之 集合

- 请画出集合框架的继承体系图
- 说说List、Set、Map三者的区别？
- ArrayList和LinkedList的区别？
- 你知道RandomAccess接口吗？他的作用是什么？
- 你了解双向链表和双向循环链表吗？
- 集合的安全性问题？
  - 请问ArrayList、HashSet、HashMap是线程安全的吗？如果不是线程安全的集合怎么办？
- ArrayList底层怎么实现的？
  - 在什么样的场景下使用ArrayList
  - 它是线程安全的吗？为什么？
  - 如果我想使用线程安全的ArrayList，应该怎么做？
  - ArrayList的常用方法有哪些？
  - ArrayList的扩容机制是怎样的？
- 知道ArrayList和Vector的区别吗？为什么要用ArrayList取代Vector呢？
- HashMap和Hashtable的区别？
  - 知道HashMap的扩容机制吗？
  - 你知道HashMap的底层数据结构吗？不同版本的数据结构知道吗？
  - 为什么要用这样的结构实现？
  - 为什么HashMap总是使用2的幂作为哈希表的大小？
  - 知道扰动函数吗？作用是什么？
  - HashMap的长度为什么是2的幂次方？
- HashSet如何检查重复？
  - HashSet的底层原理是什么？
- HashMap多线程操作死循环问题？
- ConcurrentHashMap和Hashtable的区别
  - ConcurrentHashMap是否有升级？如果有，你知道升级的原理吗？
  - ConcurrentHashMap底层如何实现的？请结合自己画图分析
- comparable和Comparator的区别
- Comparator定制重排序？请给出排序示例代码
  - compareTo方法
- 请写出集合框架底层数据结构总结以及其操作的特点
  - List
    - ArrayList
    - Vector
    - LinkedList
  - Set
    - HashSet
    - LinkedHashSet
    - TreeSet
  - Map
    - HashMap
    - LinkedHash Map
    - Hashtable
    - TreeMap
- 如何选用集合
- 除了这些集合其他的集合了解吗？
- 并发集合和普通集合了解吗？
- 数组和链表使用的常见了解吗？
- Map中的key和value可以为null吗？
- Collections的常用API方法