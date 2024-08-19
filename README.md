# docker-wordpress
docker compose一键搭建wordpress
https://www.kagura.me/dev/20240819173628.html

## 第一步：克隆仓库

首先，克隆仓库到你的本地环境：

```bash
git clone https://github.com/KingFalse/docker-wordpress.git
```

## 第二步：修改域名

在克隆完成后，打开项目文件夹并修改 `Caddyfile` 文件中的域名配置。请确保你的域名已经解析到当前服务器的IP地址。

```bash
nano Caddyfile
```

在文件中找到以下内容并修改为你的域名：

```
kagura.me {
	reverse_proxy wordpress:80
}
```

## 第三步：启动Docker容器

完成上述修改后，使用以下命令启动Docker容器：

```bash
docker-compose up -d
```

容器启动后，你的网站将会在配置的域名上可用。
