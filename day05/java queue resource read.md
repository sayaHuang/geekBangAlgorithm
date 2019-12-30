[TOC]

#java queue resource read
##总览
> Queue接口在java.util包中可用，并且扩展了Collection接口。 队列集合用于保存要处理的元素，并提供各种操作，如插入，删除等。它是对象的有序列表，其使用仅限于在列表末尾插入元素，并从头开始删除元素 列表，即遵循FIFO或先进先出原则。 作为一个接口，队列需要一个具体的类进行声明，最常见的类是Java中的PriorityQueue和LinkedList。需要注意的是，这两种实现都不是线程安全的。 如果需要线程安全的实现，PriorityBlockingQueue是一种替代实现。


##接口中声明了以下方法
1. `add()` - 此方法用于在队列尾部添加元素。 更具体地说，如果使用链表，则在链表的最后，或者在实施优先队列的情况下，根据优先级。

2. `peek()` - 此方法用于查看队列头而不删除它。 如果队列为空，则返回Null。

3. `element()` - 此方法类似于peek（）。 当队列为空时，它将引发NoSuchElementException。

4. `remove()` - 此方法删除并返回队列的头部。 当队列为空时，它将引发NoSuchElementException。

5. `poll()` - 此方法删除并返回队列的头部。 如果队列为空，则返回null。

6. `size()` - 此方法返回队列中的元素总量。

##LinkedList对queue接口的实现