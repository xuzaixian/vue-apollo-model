# Store

store是用于全局存储Model实例的集合，后续会在Model中提供跨Model引用的模式。

## Multi Client
0.4.0版本以后，vue-apollo-model支持多clients的设置，例如
```javascript
new Store({
    defaultClient,
    clients: {
        aClient,
        bClient,
    },
});
```

其中`defaultClient`为必传项，`clients`为选填项，在具体的`apolloQuery`或`apolloMutation`中，开发者可以自行定义所使用的client实例，当`clients`并不包含指定的key时，`vue-apollo-model`会默认回退使用`defaultClient`进行请求。


