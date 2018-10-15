# 如何保持github上fork的项目与原项目同步
首先先通过 github 的 web 页面 fork 目标的项目
前提是自己已经设置好了git,并且配置了相应的权限
然后使用git clone命令在本地克隆自己 fork 的项目：

git clone https://github.com/YOUR-USERNAME/project—name

然后需要复制被自己fork的项目的git地址
切换到自己之前克隆的项目的路径下，使用：

git remote -v
就可以看到当前项目的远程仓库配置

然后使用下面的命令：

git remote add upstream 原始项目仓库的git地址
然后如果你继续使git remove -v命令查看的话，就会发现这个时候已经和原始的被fork的项目产生了关联。
如果想保持项目同步的话，一般使用下面的命令就好了：

git fetch upstream
git merge upstream/master