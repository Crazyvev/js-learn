高阶函数map（）与filter（）的使用
map与filter同样作用于数组中的每一个元素，map返回的是数组中的具体指，而filter只需要返回ture或false以此来筛选元素
用filter筛选数组中的重复元素
r = arr.filter(function (element, index, self) {
    return self.indexOf(element) === index;
});
去除重复元素依靠的是indexOf总是返回第一个元素的位置，后续的重复元素位置与indexOf返回的位置不相等，因此被filter滤掉了。
