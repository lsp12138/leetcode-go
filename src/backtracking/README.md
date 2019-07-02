# 回溯

回溯需要考虑四个东西：

1. 递归结束条件
2. 递归限制条件（何时调用递归）
3. 递归函数的参数
4. 调用递归函数后的回退

## 回溯时的递归函数传入切片需要格外注意

由于切片的底层还是数组，为了防止递归函数多处同时操作底层数组造成结果错误，将单个结果加入到最终结果时需要加入单个结果的拷贝数组。

## 回溯时调用递归函数后啥时候回退

如果调用的递归函数在for循环里，一般都会回退，参考17，此时面临的选择是用或不用当前值。

如果调用的递归函数在if里，且在不同if限制条件下都调用了递归函数，一般不回退，参考22，此时面临的是多个值选哪一个。

## 输入无重复和有重复的数

参考39，40，与46，47，与78，90。

输入有重复时往往先排序，然后遍历时去重（当前值与上一个值比较）。