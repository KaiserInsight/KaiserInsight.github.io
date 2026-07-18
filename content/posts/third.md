---
title: "Linux 命令"
date: 2026-07-16T08:00:00+08:00
summary: "Linux 常用命令。"
cover: "image/Still_250_001.png"
---

# 1. 系统信息

## 查看系统版本

    cat /etc/os-release


## 查看内核版本

    uname -r


## 查看完整系统信息

    uname -a


## 查看CPU

    lscpu


## 查看CPU核心数量

    nproc


## 查看内存

    free -h


## 查看磁盘

    df -h


## 查看运行时间

    uptime


---

# 2. 文件与目录

## 查看目录

    ls


## 详细列表

    ls -l


## 查看隐藏文件

    ls -a


## 人性化显示

    ls -lh


## 当前目录

    pwd


## 进入目录

    cd 目录


## 返回上级

    cd ..


## 返回home

    cd ~


## 创建目录

    mkdir dirname


## 递归创建

    mkdir -p a/b/c


## 创建文件

    touch file.txt


## 删除文件

    rm file.txt


## 强制删除

    rm -f file.txt


## 删除目录

    rm -rf dirname


## 复制文件

    cp source target


## 复制目录

    cp -r dir1 dir2


## 移动文件

    mv file /path


## 文件改名

    mv old new


---

# 3. 文件查看

## 查看文件

    cat file


## 分页查看

    less file


## 查看前10行

    head file


## 查看指定行

    head -n 20 file


## 查看最后10行

    tail file


## 实时查看日志

    tail -f logfile


---

# 4. 文件搜索

## 查找文件

    find / -name filename


## 查找普通文件

    find . -type f


## 查找目录

    find . -type d


## 按大小查找

    find / -size +1G


## 搜索文本

    grep "keyword" file


## 递归搜索

    grep -r "keyword" path


## 显示行号

    grep -n "error" file


---

# 5. 权限管理

权限：

    r = read
    w = write
    x = execute


## 查看权限

    ls -l


## 修改权限

    chmod 755 file


## 添加执行权限

    chmod +x script.sh


## 修改文件所有者

    chown user file


## 修改目录所有者

    chown -R user:group dir


---

# 6. 用户管理

## 查看用户

    cat /etc/passwd


## 添加用户

    useradd username


## 创建home目录

    useradd -m username


## 删除用户

    userdel username


## 修改密码

    passwd username


## 切换用户

    su username


## 管理员模式

    sudo -i


---

# 7. 软件管理

## Debian / Ubuntu

更新：

    apt update


升级：

    apt upgrade


安装：

    apt install package


删除：

    apt remove package



## CentOS / Rocky

安装：

    yum install package


更新：

    yum update


---

# 8. 进程管理

查看进程：

    ps aux


实时查看：

    top


高级：

    htop


搜索：

    ps aux | grep nginx


结束：

    kill PID


强制结束：

    kill -9 PID


后台运行：

    command &


---

# 9. 服务管理

查看服务：

    systemctl status nginx


启动：

    systemctl start nginx


停止：

    systemctl stop nginx


重启：

    systemctl restart nginx


开机启动：

    systemctl enable nginx


取消启动：

    systemctl disable nginx


---

# 10. 网络管理

查看IP：

    ip addr


查看端口：

    ss -tulpn


测试网络：

    ping www.baidu.com


DNS查询：

    nslookup domain.com


下载：

    wget URL


HTTP请求：

    curl URL


---

# 11. 磁盘管理

查看空间：

    df -h


查看目录大小：

    du -sh dirname


查看设备：

    lsblk


挂载：

    mount /dev/sdb1 /mnt


卸载：

    umount /mnt


---

# 12. 压缩解压


## tar.gz压缩

    tar -czvf file.tar.gz folder


## tar.gz解压

    tar -xzvf file.tar.gz


## zip压缩

    zip file.zip files


## zip解压

    unzip file.zip


---

# 13. SSH远程

连接：

    ssh user@host


指定端口：

    ssh -p 2222 user@host


上传：

    scp file user@host:/path


下载：

    scp user@host:/file .


---

# 14. 环境变量


查看：

    env


查看PATH：

    echo $PATH


设置：

    export NAME=value


永久设置：

    vim ~/.bashrc


刷新：

    source ~/.bashrc


---

# 15. 日志管理


查看日志：

    journalctl


实时：

    journalctl -f


服务日志：

    journalctl -u nginx


---

# 16. 定时任务


编辑：

    crontab -e


查看：

    crontab -l


格式：

    分 时 日 月 周 命令


例：

    0 3 * * * /backup.sh


---

# 17. Docker


查看版本：

    docker version


查看容器：

    docker ps


全部容器：

    docker ps -a


查看镜像：

    docker images


下载镜像：

    docker pull image


运行：

    docker run -d image


进入容器：

    docker exec -it id bash


查看日志：

    docker logs id


停止：

    docker stop id


删除：

    docker rm id


---

# 18. Git


初始化：

    git init


状态：

    git status


添加：

    git add .


提交：

    git commit -m "message"


拉取：

    git pull


推送：

    git push


克隆：

    git clone url


---

# 19. Vim


进入：

    vim file


插入：

    i


保存：

    :w


退出：

    :q


保存退出：

    :wq


强制退出：

    :q!


搜索：

    /keyword


---

# 20. 常用快捷键


|快捷键|作用|
|-|-|
|Ctrl+C|终止程序|
|Ctrl+D|退出|
|Ctrl+L|清屏|
|Ctrl+A|行首|
|Ctrl+E|行尾|
|Ctrl+U|删除前内容|
|Ctrl+K|删除后内容|
|Tab|自动补全|
|↑↓|历史命令|

---

# Linux命令速记

ls        查看文件

cd        切换目录

pwd       当前路径

cp        复制

mv        移动

rm        删除

find      查找

grep      搜索

chmod     权限

chown     所属

ps        进程

kill      结束进程

systemctl 服务

ssh       远程

scp       传输

tar       压缩

df        磁盘

du        大小

top       资源

docker    容器

git       版本控制
