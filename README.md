算法分类:
1.前缀和
    比如求一个数组中连续子数组的和能被k整除
    具体流程:
    数组A:
    [a1,a2,a3,a4,a5.....an]
    根据数组A新建一个前缀和数组即数组B：
    [0,a1,a1+a2,a1+a2+a3,.....a1+a2+...+an]

    分别对数组B每个元素mod k
    [0,m1,m2,...mn]
    然后统计求模后相同的元素个数，比如：
    {0:t1,1:t2,...k-1:tk}
    然后计算子数组数量
    Σ(ti*(ti-1)/2)
    (只有当余数相同的前缀和对应的子数组的和才能被k整除)
