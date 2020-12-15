一，promise对象（异步回调）——精髓是状态
1.1 之前用函数用传函数作为入参来解决异步回调问题。

1.2 现在是promise.then() 来解决异步回调

1.3 多步回调 通过then() 链式操作
promise.then(function(){
	
	return data1
}).then(function(data1){ // return promise对象 中传给resolve数据

	return "data2"
}).then(function(){ // return 数据，then中接收到 return的数据
	
})

1.4 Promise.all

1.5 Promise.race 那个接口快就那个为准


then() 函数

七、模块化
1、export命令
as 关键字重命名
2、import命令 
静态加载：变量不可编辑
静态加载，针对静态加载增加了 import()
3、export default 命令
默认有default命令的时候，import 不带 {} 来调用，因为返回的就是一个变量 。
写法的配对：
export default
import x from xxx

export 
imprt {} from xxx
import * from xxx
3、import()

八、模板字符串（template string）

与es5不同：
可以不用引用比的js模版来渲染数据。
渲染方式：
${name}
$(function('name'))

九，Class 和传统构造函数有何区别
class Class {
    curstructor(x,y){
        this.x = x;
        this.y = y;
    }
    add(){
        return this.x + this.y;
    }
}
extends 关键字实现继承，
有extends 必须有super，它代表父类的构造函数。// 与php中的super一样

Class 和传统构造函数有何区别
1、Class 在语法上更加贴合面向对象的写法
2、Class 实现继承更加易读、易理解，对初学者更加友好
3、本质还是语法糖，使用prototype