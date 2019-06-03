#### 拉取新分支
1. 切换到目标分支
```
git checkout <BranchName>
```
2. 拉取最新内容
```
git pull
```
3. 新建分支并切换到新分支
```
git checkout -b <BranchName>
```
4. 把新建的分支push到远端
``` 
git push origin <BranchName>
```
5. 当前分支与本地关联
```
git branch --set-upstream-to=origin/<BranchName>
```

#### 查看分支
```
git branch -a
```
#### 删除分支
1. 删除本地分支
```
git branch -d <BranchName>
```
2. 删除远程分支
```
git push origin -d <BranchName>
```
删除远程分支后，使用branch -a 命令依然可以看到分支信息，会显得分支很凌乱。
可以通过命令：
```
git remote show origin
```
查看remote地址，远程分支，还有本地分支与之相对应关系等信息。
最后根据提示，清理无效的分支：
```
git remote prune origin
```