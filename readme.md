[26] 链表 LinkedList
- 算法
- 数据结构  链表
- webpack 跑起来
给定一个链表(实现一个),和一个特定值X，对链表进行分割，使所有小于X的节点都在大于或等于X的节点之前
保证原来的顺序
LinkedList (n)LinkedListNode
存储数据可以不连续
head->next->node1->..node->tail->next=null

head = 1->4->3->2->5->2  x=3
1->2->2->4->3->5
1. 一分为二  节点 就是在Val 后接next属性
  两个链表 next 小的链表 next-> 大链表的头节点    使两个链表连接起来
  怎么在组成链表的过程中
  四个指针
  lowerHeader
  lowerTail
  highHeader
  highTail
  lowerHeader = head
  4? 跳过 1->next 放开 1->4的指针断开   1是结点 next = null
  1->lowerHeader->next 2 ->2
  4->highHeader->..->5
  最后让lowerHeader->next = highHeader
  while 一下就可以

  