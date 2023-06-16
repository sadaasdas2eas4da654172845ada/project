git作用
集中式版本控制系统（vcs）=>svn
分布式版本控制系统（decs）=>git

git的作用

在项目开发的进程中对值得记录的时间节点进行“备份”方便后期恢复（后悔药）
方便团队协作开发

git管理文件的三种状态
Git有三种状态，你的文件可能较于其中之一:
已提交(committed)、已修改(modified)和已暂存(staged)
·已修改表示修改(新增 更新 删除)了文件，但还没保存到数据库中。
·已暂存表示对一个已修改文件的当前版本做了标记，使之包含在下次提交的快照中。
·已提交表示数据已经安全地保存在本地数据库中。
这会让我们的Git项目拥有三个阶段:工作区、暂存区以及Git目录。

初次运行git前的配置
配置用户名和邮箱
git config --global user.name "xxx"
git config --global user.email "xxx"

查看配置信息
git config --list

查看单个信息
git config user.name
git config user.emali


获取 git 仓库（repo）
自行初始化git仓库（git init）


克隆远程(服务器)仓库 (git clone http://192.168.122.33:3080/shenhongchun/SLXM.git)

U 未跟踪
A 
M 跟踪后被修改



创建快照（备份）
git add . 将所有文件放到暂存区
git commit -m "提交信息" 将暂存区提交到仓库（某个功能完成的时候/在必要时候提交）

【工作区】git add . -->  暂存区 git commit -m "xxx" --> 【repo】
【工作区】 git commit -a -m "xxx"   --> 【repo】(vim 编译器操作)


git reset --soft commit_id 将当前版本的内容回退到暂存区
git reset --hard commit_id 将当前版本的内容删除
git reset --mixed commit_id (默认) 将当前版本的内容回退到工作区
HEAD=>当前版本
HEAD^=>当前版本的上一个版本
HEAD~n=>当前版本的上n个版本
暂存区 <--  git reset --soft commit_id 【repo】
工作区  <-- git reset commit_id 【repo】
移除  <-- git reset --hard commit_id 【repo】