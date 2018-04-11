一家做室内导航的公司。主要是笔试题目多。面试问了问工作经历。

题目比较中规中矩吧。答题时间不到半个小时，有些题目答得太快了没有进行进一步思考。
那个正则的问题忘记加g。
reduce的函数写的也不算很完善。
最后的输出题目也没输出数组。

1.什么是原型继承。提供代码进行讲解。
```
function P(){}
function C(){}
C.prototype = new P();
```
2.描述promise的使用场景。promise它所解决的问题以及现在对于异步操作的解决方案。

解决的问题：1.控制反转。
异步：生成器，promise,await。

3.通过reduce实现简单的数组求和。示例数组[1,2,3,4,5],简述reduce一般使用场景。
```
function reduce(arr,fn,start){
    var res,i=0;
    for(i;i<arr.length;i++){
        if(start == undefined && 0 == i){
            res = arr[i];
        }else{
            res = fn(res,arr[i]);
        }
    }
    return res;
}

reduce([1,2,3,4,5],function(a,b){return a+b})
```

4.如何实现一个img在div中上下居中。

5.请从'2017-05-15T09:10:23 Europe/Paris'提取出结果[2017,05,15,09,10,23].
```
'2017-05-15T09:10:23 Europe/Paris'.match(/\d+/g)
```

6.apply,call的用途和区别。最好从代码层面展开讲。

答：主要用来绑定this。
区别：1.参数不同。apply(window,[1,2,3])效果赞同于call(window,1,2,3)。
     2.call多数情况下执行效率更高。

7.css常用的transition解决方案，简述与keyframe区别。

8.如何判断变量x是否是对象。
```
Object.prototype.toString.call(x) == '[object Object]';
```

9.提供一个闭包的使用代码，描述概念及好处。
```
function addFn(x){
    return function(y){
        return x+y;
    }
}
var  add5 = addFn(5);
add5(6);//11
```

10.求输出。
```
var str = 'hello world';
var next = [].filter.call(str,function(s,index){
    return index>5;
    })
console.log(next);
```
答案是 ["w", "o", "r", "l", "d"]



