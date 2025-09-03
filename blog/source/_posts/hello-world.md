---
title: 將"Blog"架設到"Github Pages"上
---
# 前置作業

## 下載"Node.js"

下載LTS版本即可
安裝選預設就好
<!-- # H1
## H2
### H3
#### H4 -->
下載Node.js是為了npm套件來安裝"hexo"

安裝後重開"Windows PowerShell"
先輸入"node"確認是否安裝完畢
輸入".exit"離開後使用"npm"安裝hexo
```
npm.cmd install hexo-cli -g
```
有時候系統沒辦法直接使用npm指令
所以加上.cmd使用管理員權限
<!-- ```python
print("你好")
```
ol order list

1. 123
2. 123
3. 123

ul 

- 1
- 2
- 3 -->
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

More info: [Deployment](https://hexo.io/docs/one-command-deployment.html)
