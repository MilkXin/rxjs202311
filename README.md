
mergeMap是并发的，那它怎么能控制请求处理顺序是请求发送的顺序呢。

上游数据 1,2,3 4,5
mergeMap变成Promise
一个Promise并行执行的，谁先完成不一定
开始顺序肯定是1 2 3 4 5 
结束顺序不一定了

swtichmap 没太懂还是
上游数据 1     2
变成Promise1 Promise2
2

怎么打印了2个，刚才一个
switchMap, concatMap, mergeMap
switchMap有新的老的不要了，所以只有最后一个
 concatMap, mergeMap有新的老的还要，多个

addEventListener('mosedown') 什么时候 removeEventListener('mousedown')
可以通过取消订阅 取消监听
of 和 from 有什么区别
function of(...args) {
  return from()
}
of 是通过from来实现 from可以把任意的值数组 Promise 迭代器转化成可观察对象
老师，可以看一下package.json吗？
"dependencies": {
    "@testing-library/jest-dom": "^5.16.5",
    "@testing-library/react": "^13.4.0",
    "@testing-library/user-event": "^13.5.0",
    "body-parser": "^1.20.1",
    "cors": "^2.8.5",
    "express": "^4.18.2",
    "morgan": "^1.10.0",
    "react": "^18.2.0",
    "react-dom": "^18.2.0",
    "react-scripts": "5.0.1",
    "rxjs": "^7.8.0",
    "web-vitals": "^2.1.4"
  },
mergeMap控制个数那有点不太明白
mergemap加了concurrent 会不会有溢出风险
mergeMap(project: (value: T, index: number) => O concurrent?: number) ,
所以mergeMap第2的参数是可以控制并发个数的
拖拽那个例子，withlatestfrom mousedown的时候，订阅的这个事件是不是已经过了
已经发生过了，取的也是上次发生的那个值


subject和可观察对象的区别是啥
Subject=可观察对象+Subscriber

明白了，不是重新订阅
subject是多播，obserable不能

subject可以有多个观察者
observable也可以有多个观察者
都可以多播放，但是subject它所有的观察者得到数据是同一份，而observable不 同的观察者得到的数据不一样
其他语言有类似rxjs的库吗？还是rxjs是前端创造出来的？

原理是reactiveX
有不同的语言的实现
rxjava



老师 withLastestFrom 和 lastValueFrom 都是获取最后一个 最新的数值， 有什么区别？
withLastestFrom 取的是一个数组 ，需要二个可观察对象，
lastValueFrom只有一个可观察对象
有取消api了吗
不能取消掉吧 是不是express中直接取消的？
取消怎么实现的
勇敢的心:取消怎么实现的

AbortController