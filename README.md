# FTP-Server
基于C++实现的FTP服务器与客户端
## 环境配置

### 系统要求

* Linux（推荐 Ubuntu 22.04）
* g++ 11.0 及以上版本
* POSIX Thread Library（pthread）

### 检查编译器

```bash
g++ --version
```

### 安装编译器（Ubuntu）

```bash
sudo apt update
sudo apt install g++
```

---

## 项目启动流程

### 1. 克隆项目

```bash
git clone https://github.com/你的用户名/FTP-Server.git
cd FTP-Server
```

### 2. 编译服务器

```bash
g++ server.cpp -o server -pthread
```

### 3. 编译客户端

```bash
g++ client.cpp -o client
```

### 4. 启动服务器

```bash
./server
```

启动成功后显示：

```text
服务器启动，端口2100...
```

### 5. 启动客户端

```bash
./client
```

输入服务器信息：

```text
ip: 127.0.0.1
port: 2100
```

### 6. 登录

默认账号：

```text
username: yanbing
password: 123
```

登录成功后进入 FTP 命令行：

```text
ftp>
```
### 7. 常用命令

查看文件列表：

ftp> ls

下载文件：

ftp> get test.txt

上传文件：

ftp> put test.txt

退出客户端：

ftp> quit
