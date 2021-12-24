# 常用命令

<ol>
    <li>配置git快捷操作命令方法：</li>
    <li>在<code>Administrator</code>中新建<code>.bashrc</code>文件</li>
    <li>用记事本打开输入：<br />
        1、alias 快捷操作命令="git操作命令"<br />
        2、例如：<br />
            &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <code>alias</code> gp="<code>git push</code>"<br />
             &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <code>alias</code> gl="<code>git pull</code>"<br />
             &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <code>alias</code> ga="<code>git add</code>"<br />
             &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <code>alias</code> gcb="<code>git checkout -b</code>"<br />
             &nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;
            <code>alias</code> gco="<code>git checkout</code>"<br />
    </li>
</ol>

### git 命令

| 操作描述                           | 命令行                                             | 简写                       | 备注 |
| ---------------------------------- | -------------------------------------------------- | -------------------------- | ---- |
| 克隆远程代码                       | git clone [仓库地址]                               |
| 更新远程代码                       | git pull                                           | gl                         |
| 推送远程代码                       | git push                                           | gp                         |
| 新建分支                           | git checkout -b [分支名] && git switch -c [分支名] | gcb && '自行配置'          |
| 切换分支                           | git checkout [分支名]                              | gco [分支名]               |
| 删除分支                           | git branch -d [分支名]                             | gcd [分支名]               |
| 删除远程分支                       | git push origin --delete[分支名]                   |
| 查看工作区修改                     | git status                                         | gs                         |
| 提交到暂存区                       | git add .                                          | ga .                       |
| 提交到远程仓库                     | git commit - m '[jira-2222] 提交描述'              | gcm '[jira-2222] 提交说明' |
| 缓存工作区的修改                   | git stash                                          | gh                         |
| 把缓存区的修改放到工作区           | git stash pop                                      | ghp                        |
| 查看提交历史                       | git log                                            | glgg                       |
| 查看常用                           | git alias                                          | ga                         |
| 回滚到某个提交记录                 | git reset --hard 'commit id'                       |
| 更改提交到远程                     | git push origin HEAD -- force                      |
| 把一个分支的提交 copy 到另一个分支 | git cherry-pick [commit id]                        | gcp [commit id]            |

### nrm 命令

npm 源管理器

| 描述                  | 命令行                                            |
| --------------------- | ------------------------------------------------- |
| 安装                  | npm i nrm -g                                      |
| 查看当前源            | npm config get registry                           |
| 设置源                | npm config set registry [源名称]或者[nrm use npm] |
| 查看所有支持的源      | nrm ls                                            |
| 使用指定的 npm 下载源 | nrm use [name]                                    |
| 查看 nrm 帮助         | nrm help                                          |
| 跳转到指定源的官网    | nrm home [name]                                   |
| 测试哪个源更快        | nrm test                                          |

### nvs 命令

介绍 跨平台 node 版本管理工具 https://github.com/jasongin/nvs

| 描述                         | 指令             | 示例           |
| ---------------------------- | ---------------- | -------------- |
| 安装其他版本                 | nvs add [版本号] | nvs add 12.0.0 |
| 查看已安装的版本             | nvs ls           |
| 安装 node.js 最新的 LTS 版本 | nvs add lts      |
| 配置为默认版本               | nvs link lts     |
| 在当前 shell 切换版本        | nvs use [版本号] | nvs use 12     |
| 更多指令                     | nvs help         |

### OS 文件操作指令

<ol>
    <li><code>sudo vi /etc/hosts</code> 进入 <code>host</code> 文件 打开文件后</li>
    <li>按 <code>i</code> 可以进入 <code>INSEFRT</code> 模式编辑文件内容</li>
    <li>按 <code>esc</code> 可以退出编辑模式</li>
    <li>按 <code>shift + :</code>可以输入退出 vim 的方式 <code>:q</code> 直接退出,输入 <code>wq</code> 保存后退出,输入<code>wq!</code>保存后强制退出</li>
</ol>

| 描述                                                                             | 指令           | 示例                   |
| -------------------------------------------------------------------------------- | -------------- | ---------------------- |
| 进入文件所在目录: cd+文件所在目录位置                                            | cd             | cd /usr/local/filename |
| 返回上层目录                                                                     | cd.            | cd dirname             |
| 新建文件夹 ：mkdir 只能创建文件夹                                                | mkdir filename | mkdir dirname          |
| 在当前目录下创建新文件：touch 可以创建任意格式文件，只需文件后缀加上文件格式即可 | touch          | touch a.txt            |
| 显示当前目录的路径名                                                             | pwd            |
| 显示文类型                                                                       | file           | file filename          |
| 删除文件或目录                                                                   | rm             | rm -rf filename        |
| 复制文件或目录                                                                   | cp             | cp file1 file2         |
| 删除一个目录                                                                     | rmdir          | rmdir dirname          |

### npm 命令

<ol>
    <li>13.4.6 major(主版本号-颠覆性的更改): 13</li>
    <li>minor(次版本号-添加新功能，做一些修改): 4</li>
    <li>patch(补丁-奇数是不稳定的，偶数是稳定的): 6</li>
</ol>
<ol>
    <li>"jquery": "^1.12.4"</li>
    <li>"*" -- 最新版本</li>
    <li>^ -- 只锁定主版本号</li>
    <li>~ -- 锁定到次版本号</li>
    <li>空 -- 锁定到 patch</li>
</ol>

| 指令                     | 描述                                       |
| ------------------------ | ------------------------------------------ |
| npm list                 | 查看包之间的依赖关系                       |
| npm list                 | grep gulp                                  |
| npm i --production       | 只装生产环境的包                           |
| npm view jquery versions | 查看所有 jquery 的所有版本以供我们安装选择 |
| npm i jquery@2.2.4 -S    | 安装特定版本的 jquery                      |
| npm i jquery@1 -S        | 安装 1 的最高版本                          |
| npm outdated             | 查看过期包                                 |
| npm update               | 锁定主版本号升级到最新                     |
| npm cache clean --force  | 清除 npm 缓存                              |
