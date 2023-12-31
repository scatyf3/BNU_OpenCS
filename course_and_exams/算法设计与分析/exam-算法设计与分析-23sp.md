- 1：
    - 复杂度这一概念的意义、多项式渐进更小的复杂度是否更好
    - p，np，npc问题的含义，怎么证一个问题是npc
- 2：
    - 两组复杂度排序
        - $O(n^{1/2}),O(logn^2),O(log^2n),O(nlogn),O(2^n)$
        - $O(2^10),O(2^{2^n}),O(2^{n^2}),O(2^{2logn}),O(n^2logn)$
    - 三个递推式子算复杂度（数值不太确定）
        - 一个规模为n的问题可以被拆分为2个规模为n-1的问题，子问题求解时间为常数时间，求复杂度
        - 一个规模为n的问题可以被拆分为9个规模为n/3的问题，子问题求解时间为O（n^2），求复杂度
        - 一个规模为n的问题可以被拆分为2个规模为n/3的问题，子问题求解时间为O(n)，求复杂度
    - 已知g(n)=O(f(n)),证明g(n)+f(n)=O(f(n))
- 3：8个数的数组，写归并和快排操作过程，其中快排以第一个数为pivot
    8 7 10 16 ...5 ...（记不清了，用一个作业题代替下）
    $$ \quad 89 \quad 67 \quad 43\quad 27 \quad 11 \quad \underline{43} \quad 54$$
- 4：贪心 时间选择问题。安排一些同学使用学校的乒乓球房间，其中i同学使用需求的起始时间是s（i），结束时间是f（i），尽量使能使用乒乓球房的同学最多
    - 用自然语言描述算法思路
    - 给出十个同学的需求表格，请问最多能安排几个同学，给出计算过程
    (没有原题的数据，给一个ppt上的例子供参考)
    $$
    \begin{array}{c|ccccccccccc}
    i & 1 & 2 & 3 & 4 & 5 & 6 & 7 & 8 & 9 & 10 & 11 \\
    \hline s_{i} & 1 & 3 & 0 & 5 & 3 & 5 & 6 & 8 & 8 & 2 & 12 \\
    f_{i} & 4 & 5 & 6 & 7 & 8 & 9 & 10 & 11 & 12 & 13 & 14
    \end{array}
    $$
- 5：回溯和剪枝 已知一个3*3矩阵，其第i行第j列的数据是第i位男运动员和第j位女运动员搭配的劣势值最小（注：最后一行，除了1之外忘记了数据，但是大差不差这个数值量）
$$
P=\begin{bmatrix}
  2 & 6 & 3 \\
  1&12&10 \\
  3 & 1 &4
\end{bmatrix}
$$
    - 用子集树表现解空间
    - 用___(FIFO,LIFO,优先队列)表示活结点
    - 剪枝策略:curP 当前的劣势值;minP,最小的劣势值，初始化为正无限
        - 若curP___maxP，则剪枝
        - （？还有一个，是限界函数吗？）
    - 画出在子集树上搜索解的过程
- 6：已知有n个小球，其中有一个较轻，其他的都是等质量。用一个机械天平找出这个较轻的小球,使称量的次数尽量少
    - 用自然语言描述算法思路
    - 写出伪代码
    - 分析复杂度
- 7：一个公司在n天里都要寄快递，每天寄送的快递数量是$/omega (i)$其中有两种方案。方案A：每天单独计费，每天的费用是r元/件。方案B：连续k天付费，每天c元。我们要找出使付费最小的最优方案
    - 证明存在最优子结构，写出递推式
    - 使用贪心算法或者动态规划法求解问题，对应的证明贪心选择性质或者重叠子问题
    - 写出伪代码
    - 给出了一个规模为10的例子，计算最优方案

