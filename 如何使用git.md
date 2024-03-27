# 如何使用 git 管理你的代码、文档版本

## 最基础的三步

1. `git init`，使用此命令时将会在当前目录下生成一个 `.git/` 目录，存在此目录表示此文件夹内的文件由 git 进行版本管理，最多只会执行一次，一般会直接克隆下来远程代码仓库的代码，此时会自动同步远程的 git 信息；
   <img src="./screenshot/git-init.png" />
2. `git add $FILE_PATH`，使用此命令将编写好的代码文件或者文档提交到暂存区中，使用方法如下；
   1. `git add ./code/**/*.ts`，将当前目录下 code 文件夹内的文件夹中包含`.ts`结尾的文件添加到暂存区；
      <img src="./screenshot/git-add.png" />
   2. `git add ./screenshot/**`，将当前目录下 screenshot 下的所有文件提交到暂存区；
      <img src="./screenshot/git-add-1.png" />
   3. `git add .`，将当前文件夹下所有不在`.gitignore`文件中的改动提交到暂存区；
      <img src="./screenshot/git-add-2.png" />
3. `git commit -m ''`，将当前所有暂存的记录提交到**本地仓库**中；
   <img src="./screenshot/git-commit.png" />
4. `git status`，使用此命令可以查看当前文件夹下所有文件的跟踪以及修改情况
   1. 新建了一个空的 json 文件后，这个文件会出现在`Untracked files`中
      <img src="./screenshot/git-status.png" />
   2. 当执行`git add empty.json`后，会出现 new file 这个状态，表示当前文件已经处于 git 跟踪管理的范围了
      <img src="./screenshot/git-status-1.png" />
   3. 如果原本处于 git 跟踪的范围内，此时修改文件并 add 之后会处于 modified 状态
      <img src="./screenshot/git-status-2.png" />
