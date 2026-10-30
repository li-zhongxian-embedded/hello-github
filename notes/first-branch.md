# 第一条分支

这个文件是在 `feature/first-branch` 分支上创建的。

## 为什么要开分支

`main` 应该永远是"能用"的版本。想改东西时：

```bash
git switch -c feature/想做的事   # 从 main 开一条平行世界
# 改代码、提交……
git push -u origin feature/想做的事
# 然后在 GitHub 网页上提 Pull Request，请人 review 后合并
```

改坏了怎么办？`git switch main` 就回来了，`main` 一个字节都没动。
