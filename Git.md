

# Git

git log --pretty=oneline --abbrev-commit。// 历史提交的commit_id
## Git标签管理
### 什么是标签
标签是一个快照。标签是某个版本的别名，为了便于管理，Git 可以给版本取个别名。

### 创建标签
git tag <name>  // 给当前最新调的commit 打标签
git tag <name> commit_id //给对应commit_id打标签

创建带有说明的表亲啊，用-a指定标签名，-m指定说明文字
git tag -a <name> -m "message"

### 删除标签
git tag -d <tagname>

### 推送标签至远程
git push origin <tagname>
git push origin --tags //一次性推送全部尚未推送到远程的本地标签

### 删除远程标签
git tag -d <tagname>
git push origin :refs/tags/<tagname>	