---
# 标题
title: 数组排序 sort
# 置顶
top: false
# 打赏
reward: true
# 分类
categories:
- 前端
# 标签
tags:
- javascript

---
使用高阶函数 sort() 来实现数组排序

<!-- more -->
排序算法
=================

排序的核心是比较两个元素的大小，在比较数字的时候我们可以根据数字的大小来进行排序，但是实际在写程序的时候我们可能需要处理更为复杂场景的排序功能，比方说比较字符串或者是对象，这个时候直接比较数字的大小是没有意义的，我们需要把处理方法函数抽离出来。

通常规定x， y两个元素，当x < y 的时候， 就返回 -1；当 x == y 的时候，就返回 0；如果 x > y 的时候，就返回 1。这样排序算法不需要关心具体的比较过程，而是根据排序结果直接进行排序。

JavaScript的Array的sort()方法就是用于排序的, 在使用之前请先了解该方法的默认排序规则，否则你会得到意想不到的结果: 
```
    var arr = [2, 1, 10, 5, 7]
    arr.sort()

    // 你以为的结果
    console.log(arr); // [1, 2, 5, 7, 10]

    // 真实结果
    console.log(arr); // [1, 10, 2, 5, 7]
```

发生以上结果是因为Array的sort()方法默认会把所有元素先转成String类型进行排序，字符串根据ASCII码进行排序。

数字排序
---------------

我们在使用sort()方法进行排序的时候，传入一个自定义函数来实现自定义排序。
比方说我们要实现一个从小到大的排序方法，我们可以这么写
```
var arr = [100, 20, 35, 46];
arr.sort(function (x, y) {
    if (x < y) return -1;
    if (x > y) return 1;
    return 0;
});
console.log(arr); // [20, 35, 46, 100]
```

如果是从大到小，可以把代码稍作调整，如下
```
var arr = [100, 20, 35, 46];
arr.sort(function (x, y) {
    if (x < y) return 1;
    if (x > y) return -1;
    return 0;
});
console.log(arr); // [100, 46, 35, 20]
```

字符串排序
---------------

默认情况下，对字符串排序，是按照ASCII的大小比较的，那么我们排序应该忽略大小写，按照字母序排序。

```
var arr = ['Google', 'apple', 'Microsoft'];
arr.sort(function (x, y) {
    a = x.toUpperCase();
    b = y.toUpperCase();
    if (a < b)  return -1;
    if (a > b) return 1;
    return 0;
}); 
//console.log(arr); ['apple', 'Google', 'Microsoft']
```

注意: 使用sort()方法会修改原数组
```
var arr = [2, 1, 5, 7]
arr.sort()
console.log(arr); // [1, 2, 5, 7]
```

<!-- ![nodejs](/images/liunx-node.png) -->



