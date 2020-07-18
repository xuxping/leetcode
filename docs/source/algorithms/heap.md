# 堆

## 常见算法题：
1、堆排序  
2、合并K个链表或文件  
3、topK  
4、流里面的中值、中位数：  
维护两个堆，一个大顶堆，一个小顶堆。大顶堆中存储前半部分数据，
小顶堆中存储后半部分数据，且小顶堆中的数据都大于大顶堆中的数据。
5、看如何求 99% 响应时间   
维护两个堆，一个大顶堆，一个小顶堆。假设当前总数据的个数是 n，
大顶堆中保存 n*99% 个数据，小顶堆中保存 n*1% 个数据。
大顶堆堆顶的数据就是我们要找的 99% 响应时间。

## 如何获取top10最热门的关键词
1、将 10 亿条搜索关键词先通过哈希算法分片到 10 个文件中
2、每个文件都只有 1 亿的关键词，去除掉重复的，可能就只有 1000 万个，每个关键词平均 50 个字节，所以总的大小就是 500MB。1GB 的内存完全可以放得下。
3、针对每个包含 1 亿条搜索关键词的文件，利用散列表和堆，分别求出 Top 10，然后把这个 10 个 Top 10 放在一块，然后取这 100 个关键词中，出现次数最多的 10 个关键词