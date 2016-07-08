# Find the Duplicate Number

## 解法1

很显然可以排序然后找重复数，这样并没有利用数在[1, n]区间的性质

## 解法2

因为数在[1, n]区间内，而且只有一个数重复，那么如果不是重复的数，必有：

```
num[num[i]] + n < 2*n, i 在[1, n]之间
```

所以对每一个i，我们操作 num[num[i]]+n，最后找出大于2*n的数，返回该数的位置即可。

#### Note:

如果不是重复数，num[i]在[1, 2n]间，在加n前要判断，否则要越界
