# leetcode
## 题目
给定一个数组 nums，编写一个函数将所有 0 移动到数组的末尾，同时保持非零元素的相对顺序。

示例:

输入: [0,1,0,3,12]
输出: [1,3,12,0,0]

说明:

    必须在原数组上操作，不能拷贝额外的数组。
    尽量减少操作次数。

## 思路

求爬楼梯的最小花费，考虑动态规划解法，因为每爬上一个楼梯后你可以选择爬一级或两级楼梯，因此每次都是从前面一级或者是前面两级的位置过来的，因此得出dp转移方程，用dp[i]表示爬到第i层的最小花费 

dp[i] = min(dp[i-2]+cost[i-2],dp[i-1]+cost[i-1]) 