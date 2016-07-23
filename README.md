promise
=======

es6 promise

**俩年前随手写的，近来发现有人在用，更新下 README.md**

这是一个极小的 promise 库，仿照 es6 promise api 做了简单实现

- 实例化

    ```
        new Promise(function(resolve,reject){
            setTimeout(function(){
                resolve('ok')
            },500)
        }).then(function(msg){
            console.log(msg)
        }).catch(function(err){
            console.log(err)
        })
    ```
- api

    - Promise.all
    - Promise.race
    - Promise.resolve
    - Promise.reject
    - Promise.delay


简单提供了一个 delay 方法，可以循环处理，如

```
var pro = Promise.resolve()
for (var i = 0; i < 5; i++) {
    pro = pro.delay(500).then(function(){
        console.log(Date.now())
    })
}
```

另外补上当时写的实现说明链接 http://www.cnblogs.com/ygm125/p/3735677.html







