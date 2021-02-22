# 贪心算法

## 简介

贪心算法就是，在每次操作时都做出**当下最好**的选择，从而使最后得到的结果是最优解。做出局部选择时，**不考虑这个选择对将来的影响**，而且做出选择之后**不会回退到以前**。因为全局结果是局部结果的简单求和，且**局部结果互不相干**，所以**局部最优策略**也就是全局最优策略。

但并不是所有问题都可以使用贪心算法得到最优解，重点是**贪婪策略**的选择，难点在于如何证明局部最优解就可以得到全局最优解。

贪心算法有点像动态规划，只不过，每个局部选择都只依靠另**一个**局部选择。要证明贪心算法能够得到全局最优解，只需要证明在填表 (动态规划的状态表) 的时候，每填一个格子我们只需要查询另一个格子，而不需要综合考虑几个格子。因为贪心算法每次只考虑一个子问题，所以解决问题的时间复杂度一般是线性的。

## 算法

-   初始化结果数组
-   在每一步中，把当前项加入结果数组中
-   如果此时结果数组是一个可行解，那就保留当前项
-   如果不是，那就去除当前项，并且之后不再考虑这一项

## 相关题目类型

### 分配问题

-   [455.分发饼干](https://github.com/suukii/91-days-algorithm/blob/master/topics/greedy/ext-assign-cookies.md)
-   [135.分发糖果](https://github.com/suukii/91-days-algorithm/blob/master/topics/greedy/ext-candy.md)

### 区间问题

-   [435.无重叠区间](https://github.com/suukii/91-days-algorithm/blob/master/topics/greedy/ext-non-overlapping-intervals.md)

TODO

-   [ ] http://web.stanford.edu/class/archive/cs/cs161/cs161.1176/Lectures/CS161Lecture14.pdf
-   [ ] http://web.stanford.edu/class/archive/cs/cs161/cs161.1176/Sections/final_review-1.pdf
-   [ ] file:///H:/Algorithm/LeetCode%20101%20-%20A%20LeetCode%20Grinding%20Guide%20(C++%20Version).pdf
