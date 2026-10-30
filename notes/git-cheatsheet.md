# Git 命令速查

## 每天都会用的

| 命令 | 作用 |
| --- | --- |
| `git status` | 我现在改了什么、哪些已暂存 |
| `git diff` | 具体改动的内容 |
| `git add .` | 把所有改动加入暂存区 |
| `git commit -m "说明"` | 打一个存档点 |
| `git push` | 上传到 GitHub |
| `git pull` | 把 GitHub 上的更新拉下来 |
| `git log --oneline --graph --all` | 看历史（带分支图） |

## 分支

| 命令 | 作用 |
| --- | --- |
| `git branch` | 列出本地分支，`*` 是当前分支 |
| `git switch -c 分支名` | 新建并切换（旧版用 `checkout -b`） |
| `git switch 分支名` | 切换分支 |
| `git merge 分支名` | 把该分支合并进当前分支 |

## 撤销与回退

| 命令 | 作用 |
| --- | --- |
| `git restore 文件名` | 丢弃工作区里未暂存的改动 |
| `git restore --staged 文件名` | 把文件移出暂存区（改动还在） |
| `git commit --amend` | 修补上一次提交（还没 push 时用） |
| `git reset --soft HEAD~1` | 撤销上一次提交，改动保留在暂存区 |
| `git reset --hard HEAD~1` | 危险：彻底丢弃上一次提交和改动 |

## 远程仓库

| 命令 | 作用 |
| --- | --- |
| `git remote -v` | 查看关联的远程仓库 |
| `git remote add origin <地址>` | 关联远程仓库 |
| `git push -u origin main` | 首次推送并记住上游分支 |
| `git clone <地址>` | 把远程仓库完整复制到本地 |

## 三条铁律

1. **push 之前先 `git status` + `git pull`。**
2. **提交信息写"做了什么"，不写"改了文件"。** 好的：`修复登录按钮在窄屏下错位`；差的：`update`。
3. **密钥、密码、`.env` 永远不进仓库。** 写成习惯，靠 `.gitignore` 兜底。
