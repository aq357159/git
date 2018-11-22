# Git 基本指令

## 基本說明
### origin(remote_name)
- git預設遠端倉庫名稱

### master(branch_name)
- git分支主線預設名稱

### .gitignore
- 忽略 不需要上傳的檔案

## init
```
# 建立 git 設定檔
> git init
```

## remote
```
# 查看目前所有的遠端倉庫
> git remote 

# 查看目前所有的遠端倉庫詳細 http/ssh(url)
> git remote -v 

# 查看遠端倉庫更多的信息
> git remote show [遠端倉庫名稱 or remote_name]

# 修改遠端倉庫名稱
> git remote rename [遠端倉庫名稱 or remote_name] [修改名稱]

# 修改某個遠端倉庫的url
> git remote set-url [遠端倉庫名稱 or remote_name] [http/ssh url]

#新增遠端倉庫
> git remote add {遠端倉庫名稱可自訂，如果未填寫以預設'origin'} [http/ssh url]

#移除遠端倉庫
> git remote rm [遠端倉庫名稱 or remote_name]

```

## clone 指令
```
# 克隆(下載)檔案
> git clone {遠端倉庫名稱可自訂，如果未填寫以預設'origin'} [http/ssh url]

# 克隆(下載)分支檔案

> git clone {遠端倉庫名稱可自訂，如果未填寫以預設'origin'} [http/ssh url] -b [分支名稱]
> git clone {遠端倉庫名稱可自訂，如果未填寫以預設'origin'} [http/ssh url] --branch [分支名稱]

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
git fetch [remote_name]
```
## push
```
# 上傳到遠端倉庫
> git push [遠端倉庫名稱 or remote_name] [分支名稱 or branch_name]

# 紀錄本次push 倉庫跟分支 下次可直接 使用 git push
> push -u [遠端倉庫名稱 or remote_name] [分支名稱 or branch_name]

# 刪除遠端分支
> git push [remote_name] --delete [branch_name]
> git push [remote_name] :[branch_name]
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
 參考：https://gitbook.tw/chapters/github/pull-from-github.html
```
git pull 
```
## diff
 參考：https://git-scm.com/docs/git-diff
```
git diff
```
## status
參考：https://git-scm.com/docs/git-status
```
# 顯示工作樹狀態
> git status

# 顯示工作樹狀態 簡易格式
> git status -s
> git status --short


' ' = unmodified
M = modified
A = added
D = deleted
R = renamed
C = copied
U = updated but unmerged


X          Y     Meaning
-------------------------------------------------
  [AMD]   not updated
M        [ MD]   updated in index
A        [ MD]   added to index
D                deleted from index
R        [ MD]   renamed in index
C        [ MD]   copied in index
[MARC]           index and work tree matches
[ MARC]     M    work tree changed since index
[ MARC]     D    deleted in work tree
[ D]        R    renamed in work tree
[ D]        C    copied in work tree
-------------------------------------------------
D           D    unmerged, both deleted
A           U    unmerged, added by us
U           D    unmerged, deleted by them
U           A    unmerged, added by them
D           U    unmerged, deleted by us
A           A    unmerged, both added
U           U    unmerged, both modified
-------------------------------------------------
?           ?    untracked
!           !    ignored
-------------------------------------------------


# 查看branch狀態
> git status -b 
> git status --branch

```
## log
```
git log
```
## tag
參考：
https://caloskao.org/git-tag-operations/
</br >
https://git-scm.com/book/zh/v2/Git-%E5%9F%BA%E7%A1%80-%E6%89%93%E6%A0%87%E7%AD%BE
```
git tag
```
## checkout
```
# 前往指定分支
> git checkout [分支名稱(branch_name)]

# 前往指定分支 並 建立分支
> git checkout -b [分支名稱(branch_name) 自訂] 

# 取得遠端分支
> git checkout --track [遠端倉庫 or remote_name]/[遠端分支 or branch_name]
> git checkout -b {分支名稱，如不填寫以遠端名稱為主} [遠端倉庫 or remote_name]/[遠端分支 or branch_name]

```
## branch
```
# 查看本地所有分支 
> git branch

# 查看遠端根本地所有分支
> git branch -a
> git branch -r

# 刪除本地分支
> git branch -d [分支名稱(branch_name)]
# 強制刪除本地分支
> git branch -D [分支名稱(branch_name)]

```
## meage
```
git meage [分支名稱 or branch_name]
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
參考：https://git-scm.com/book/zh/v2
