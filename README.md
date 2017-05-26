# docker-notadd

Notadd 第一版 docker 镜像

当前可供测试和开发使用，请勿用作生产环境。默认只能使用sqlite 数据库安装。

`如果您还未安装 docker，请从 http://get.daocloud.io  安装`

## 一键安装

```
docker run -p 8080:80 --name notadd notadd/notadd
```

访问 http://localhost:8080


###  映射本地目录

请确保 /home/wwwroot 目录存在，且首次运行时目录为空。

```
docker run -p 8080:80 -v /home/wwwroot:/var/www notadd/notadd
```

### 使用 composr 及 PHP 命令

```
docker exec -ti notadd /bin/sh
```


### 自定义网站配置

默认不支持网站自定义配置，如需要配置开发或生产环境，建议使用 laradock。

## 使用laradock 安装

参见： https://docs.notadd.com/laradock/
