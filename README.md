# Git 基本指令

---------------------
## 基本說明
### origin
- git預設遠端倉庫名稱

### master
- git分支主線預設名稱

### .gitignore
- 忽略 不需要上傳的檔案

---------------------------
## init
```
# 建立 git 設定檔
> git init
```
---------------------------
## remote
```
# 查看目前所有的遠端倉庫
> git remote 

# 查看目前所有的遠端倉庫詳細 http/ssh(url)
> git remote -v 

# 查看遠端倉庫更多的信息
> git remote show [遠端倉庫名稱 or origin]

# 修改遠端倉庫名稱
> git remote rename [遠端倉庫名稱 or origin] [修改名稱]

# 修改某個遠端倉庫的url
> git remote set-url [遠端倉庫名稱 or origin] [http/ssh url]

#新增遠端倉庫
> git remote add {遠端倉庫名稱可自訂，如果未填寫以預設'origin'} [http/ssh url]

#移除遠端倉庫
> git remote rm [遠端倉庫名稱 or origin]

```
-----------------------------
## clone 指令
```
# 克隆(下載)git 上的檔案
> git clone {遠端倉庫名稱可自訂，如果未填寫以預設'origin'} [http/ssh url]

```
## add
```
# 基本用法
> git add [file]

# add 所有檔案
> git add *
> git add .
> git --all

# 特殊用法
> git add *.js
> git add /1/2/*.js
> git add /1/2

```
## reset
```
git reset
git reset HEAD [file]
```
## fetch
```
git fetch [origin]
```
## push
```
git push [遠端倉庫名稱 or origin] [分支名稱 or master]
```
## commit
```
# commit 檔案
> git commit 

# -a 上傳以追蹤所有檔案
> git commit -a

# -m 增加commit 說明
> git commit -m "說明"

# -m -a 簡寫
> git git -am "說明"
```
## pull
```
git pull 
```
## diff
```
git diff
```
## status
```
git status
git status -s
```
## log
```
git log
```
## tag
參考：https://caloskao.org/git-tag-operations/
```
git tag
```
## checkout
```
git checkout -b [分支名稱 自訂]
git checkout [分支名稱]
```
## branch
```
git branch
git branch -d [分支名稱]
```
## meage
```
git meage [分支名稱 or master]
```
## rm
```
# 刪除檔案
> git rm [file]
```
## mv 
```
# 修改名稱
> git mv [fileName] [new FileName]
```

-------------------------------
參考：https://git-scm.com/book/zh/v2
