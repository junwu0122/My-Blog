---
title: 將" Blog "架設到" Github Pages "上
---
# 前置作業

## 下載" Node.js "

下載LTS版本即可
安裝選預設就好
<!-- # H1
## H2
### H3
#### H4 -->
下載Node.js是為了npm套件來安裝" hexo "

安裝後重開" Windows PowerShell "
先輸入" node "確認是否安裝完畢
輸入" .exit "離開後使用"npm"安裝hexo
```
npm.cmd install hexo-cli -g
```
有時候系統沒辦法直接使用npm指令
所以加上.cmd使用管理員權限

## 使用" Hexo " 一鍵部屬指令
先建置一個你想放入網站code的資料夾
假設放在桌面,名字取" Blog "
使用"ls"指令確認有" Blog "資料夾後
使用"cd /Blog"進到Blog的目錄下
輸入
```
hexo init blog
```
使用ls指令會發現目錄下多了一個/blog的資料夾
使用"cd /blog"進到Blog/blog的目錄下
輸入"code ."開啟VSCODE編輯器
叫出VSCODE裡的Git Bash(終端機Ctrl+`),通常在+號旁邊的﹀裡找的到

在Git Bash中輸入
```
npm install
```
安裝相關套件完後輸入
```
hexo server
```
就能建立一個預設的hexo網頁了!
但目前都只是建立在本地端而已

## 如何架設到" Github Pages上 "

### 建立一個" Github Repositories"
名字假設取 My-blog
Create完會有教學指令教你怎麼設定新的repo
```
git init
git add README.md
git commit -m "first commit"
git branch -M main
git remote add origin <替換成你的HTTPS 記得去掉"<>">
git push -u origin main
```
這樣就建立好一個My-blog的repo並且進行push(上傳到github server)的動作

### 部屬(Deploy)到" Github Pages "

1. [安裝 hexo-deployer-git](https://www.npmjs.com/package/hexo-deployer-git)
2. 到專案資料夾(最外層)找到" _config.yml "並新增以下
```
deploy:
   type: git
   repo: https://github.com/<你github的username>/<repo名稱>.git
   # example, https://github.com/hexojs/hexojs.github.io
   branch: gh-pages
```
3. 在Git Bash中執行
```
hexo clean
hexo g -d
git add .
git commit -m "modify config"
git push
```
4. 在 "_config.yml"設定檔中修改" URL "網址, ex: https://<你Github的username>.github.io/<專案名稱>/
🍭這樣就完成部屬的步驟了!
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
