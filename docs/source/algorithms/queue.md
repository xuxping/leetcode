# 队列   
队列的特点是先入先出，一种操作受限的线性表数据结构。

## 种类
1. 采用数组实现的队列，如果tail到达队尾，需要进行数据搬移   
2. 采用链表实现   
3. 循环链表  


## 用途  
1. 阻塞队列   
阻塞队列其实就是在队列基础上增加了阻塞操作。简单来说，就是在队列为空的时候，从队头取数据会被阻塞。因为此时还没有数据可取，直到队列中有了数据才能返回；如果队列已经满了，那么插入数据的操作就会被阻塞，直到队列中有空闲位置后再插入数据，然后再返回。
对于大部分资源有限的场景，当没有空闲资源时，基本上都可以通过“队列”这种数据结构来实现请求排队。