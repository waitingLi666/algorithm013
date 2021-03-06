**字典树**  
即Trie树，又称单词查找树或键树，是一种树形结构。典型应用是用于统计和排序大量的字符串(但不仅限于字符串)，经常被搜索引擎系统用于文本词频统计。  
1)优点：最大限度地减少无谓的字符串比较，查询效率比哈希表高。  
2)注意：Trie树，不是一颗二叉树，是多叉树。  
3)基本性质：  
>结点本身不存完整单词；  
>从根结点到某一结点，路径上经过的字符连接起来，为该结点对应的字符串；  
>每个结点的所有子结点路径代表的字符都不相同。  


**并查集**  
基本操作：  
>makeSet(s):建立一个新的并查集，其中包含s个单元素集合  
>unionSet(x,y)：把元素x和元素y所在的集合合并，要求x和y所在的集合不相交，如果相交则不合并  
>find(x)：找到元素x所在的集合的代表，该操作也可以用于判断两个元素是否位于同一个集合，只要将它们各自的代表比较一下就可以了。  


**高级搜索**  
1）剪枝  
在状态树进行搜索的时候，如果发现这个分支已经处理过了，就把它暂存在缓存里，整个分枝就可以剪掉，不需要再手动进行计算。或分枝较差，也可以剪掉。  
2）双向BFS  
从起点和终点两边扩展节点,当节点发生重合时即找到最优解。  
3）启发式搜索  
利用问题拥有的启发信息来引导搜索，达到减少搜索范围、降低问题复杂度的目的。关键在启发式函数，该函数是一种告知搜索方向的方法，提供了一种明智的方法来猜测哪个邻居结点会导向一个目标。  


**AVL树**  
1）本质是二叉搜索树。  
2）平衡因子：它的左子树的高度减去它的右子树的高度(有时相反)的值介于{-1,0,1}之间。  
3）通过旋转操作来进行平衡：左旋、右旋、左右旋、右左旋。  
>左旋：右右子树  
>右旋：左左子树  
>左右旋：先左子树后右子树  
>右左旋：先右子树后左子树  
4）不足：结点需要存储额外信息，且调整次数频繁  


**红黑树**  
一种近似平衡的二叉搜索树，确保任何一个结点的左右子树的高度差小于两倍。需满足条件：  
>每个结点要么是红色，要么是黑色；  
>根结点是黑色  
>每个叶结点(NIL结点)是黑色的  
>不能有相邻接的两个红色结点  
>从任一结点到其每个叶子的所有路径都包含相同数目的黑色结点  
对比AVL树和红黑树，如果查找较多，考虑AVL树，因为其是严格的平衡二叉搜索树；如果插入删除较多，可考虑红黑树，因为其不需要像AVL树那样频繁调整平衡。  

本章学习的时候，有种“书读百遍,其义自见”的感觉。许多知识点看第一遍的时候是很懵的，带着思考看第二遍第三遍的时候，能明白这个知识点是什么意思。因时间有限，要达到灵活运用知识点的效果，还需要不断地实践，在实践中加深理解。

