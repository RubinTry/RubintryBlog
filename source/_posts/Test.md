---
title: 自制框架
date: 2020-03-31 20:52:06
tags: Android开发
---

****

## RuHttp


&nbsp;&nbsp;&nbsp;&nbsp;**[RuHttp][readme]**是一个高性能、高并发、高扩展性的安卓http客户端，它可以使您的内容加载更快并节省带宽。

## 特性
1.目前支持基于http的GET、POST请求
2.支持Android x
3.支持高并发


## 如何引入
```groovy
implementation 'cn.rubintry.ruhttp:ruhttp:1.0.0'
```

### 如何使用
```java
   RuHttp ruHttp = new RuHttp.Builder<>()
                .setMethod(MethodType.POST)//指定请求方式
                .setUrl(url)
                .addParam("key", "value")
                .addParam("key", "value")
                .addParam("key", "value")
                .setType(你的model类.class)
                .setHttpRequestListener(new IRuHttpRequestListener<你的model类>() {
                    @Override
                    public void onSuccess(你的model类 o) {
                        ...
                    }

                    @Override
                    public void onFail(Throwable e) {
                        ...
                    }
                }).build();
    //发起请求
    ruHttp.execute();
```


## License
```text
Copyright 2020 Sunzhong Lu

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

    http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```


<!-- ---
title: Hello World
---
Welcome to [Hexo](https://hexo.io/)! This is your very first post. Check [documentation](https://hexo.io/docs/) for more info. If you get any problems when using Hexo, you can find the answer in [troubleshooting](https://hexo.io/docs/troubleshooting.html) or you can ask me on [GitHub](https://github.com/hexojs/hexo/issues).

## Quick Start

### Create a new post

``` bash
$ hexo new "My New Post"
```

More info: [Writing](https://hexo.io/docs/writing.html)

### Run server

``` bash
$ hexo server
```

More info: [Server](https://hexo.io/docs/server.html)

### Generate static files

``` bash
$ hexo generate
```

More info: [Generating](https://hexo.io/docs/generating.html)

### Deploy to remote sites

``` bash
$ hexo deploy
```

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html) -->


[readme]: https://github.com/Rubintry/RuHttp