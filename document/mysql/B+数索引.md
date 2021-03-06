#B+数索引
**什么是B+树**
>* B+数索引是传统意义上的索引，是关系型数据库系统最常用也是最有效的索引。
>* B+数的索引类似二叉树，根据key-value快速查找数据
>* 注意：B不代表二叉（binary），而是代表平衡（balance），从平衡二叉树演化而来，不是二叉树。
>* 盲点：B+树根据索引找到的不是对应的行数据，而是页，然后数据库把页读到内存中，再查到想要的数据。

**B+树相关的数据结构与算法**
>* 二分查找法
>>* 即折半查找法。
>>* 基本思想：一组递增或递减的有序数字，跳跃式查找，与查找区域内的中间位置数字对比，
如果小于中间数，则查找中间数左边，否则右边，每次比较排除一半
>*平均查找次数：对于一个有序的10位数。(1+2+...+10)/10=5.5.对于折半查找(4+3+2+4+..+3)/10=2.9
折半查找最多查四次，顺序找找最多为10次。

**二叉查找数和平衡二叉树**
>* 二叉查找树是一种经典的数据结构。左节点大于跟节点，右节点大于跟节点。
>* 如果想要查询效率最高，需要保证树是平衡的，变成平衡二叉树（AVL树）。
>* 平衡二叉树：首先是二叉查找树，然后任意节点的子树高度差不超过1。
>* 平衡二叉树的查询性能不是最高，最高的是最优二叉树，不过需要大量的操作，一半平衡二叉树就够了。
>* 增删的时候，通过左旋和右旋来维持平衡。一般用于内存接哦股对象中。

**B+树**
>* B+树是为磁盘或者其他直接存取辅助设备设计的一种平衡查找树。
>* 主要概念：跟节点  叶子节点 扇出（fan out） 高度 
每层的节点数据从左到右一次变大的。
>* B+树的操作
插入 删除
>* B+树索引：就是B+树在数据库的实现。一般都是2-4层，因此查询速度很快。
>>* 聚集索引：存储行数据
>>* 辅助索引：存储键值，根据键值查找行数据。(辅助索引可以查到的数据不要从聚集索引查)
>>* B+索引的操作 增加 删除索引


