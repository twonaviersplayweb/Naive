数据结构的基本知识
==============

<p>数据结构三要点</p>
1. 数据元素之间的逻辑关系
2. 数据元素及其关系在计算机中的存储方式
3. 施加在数据上的操作（检索，插入，删除，更新，排序）

<p>数据结构的简单表示</p>
B=(D,R), D为元素合集，R为D上元素关系的合集

<p>逻辑的结构类型</p>
1. 集合，元素间无联系
2. 线性结构，一对一关系
3. 树形结构，一对多关系
4. 图形结构，多对多关系

<p>存储结构类型</p>
1. 顺序存储结构，节省空间，不便于修改
2. 链式存储结构，便于修改，空间利用率低
3. 索引存储结构，增加索引表，操作类似指针，降低了空间利用率
4. 散列存储结构，通过关键字计算值，效果nice

>抽象数据类型（ADT）
ADT=（D，S，P），D为数据对象，S为D上关系集，P为数据对象的基本运算集
ADT两个特征：数据抽象，数据封装

<p>算法5个特征</p>
1. 有穷性
2. 确定性
3. 可行性
4. 有输入
5. 有输出

>执行时间：基本运算所需的时间乘以运算次数，由基本运算的执行次数来计量

<p>T(n)=O(f(n))</p>
1. n——问题规模
2. T(n)——执行时间
3. f(n)——时间复杂度
4. O——Order，数量级，表随问题规模n的增大，算法执行时间的增长率和f(n)的增长率相同

>若f(n)是正整数n的一个函数，则T(n)=O(f(n))表存在一个正的常数c和n0,使得当n>=n0时都满足T(n)<=cf(n),即只求出T(n)的最高阶项，忽略低阶项和常数


<p>C实例</p>

```#define MAX 20```

void martix(int n, int A[MAX][MAX], int B[MAX][MAX], int C[MAX][MAX])
{

    int i, j;

    for(i = 0; i < n; i++){                       /*频度为n+1，执行n次*/

        for(j = 0; j < n; j++)                    /*频度为n(n+1),执行n+1次*/

        C[i][i] = A[i][j] + B[i][j]               /*n^2*/

    }
}

>T(n) = n+1+n(n+1)+n^2 = 2n^2+2n+1



