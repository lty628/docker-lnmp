# docker-lnmp

## 使用前提

- 已部署dock er
- 已经安装docker-compose
- 

## 使用

```bash
# 进入项目根目录
cd docker-lnmp
# 初次使用
docker-compose up -d
# 修改nginx或php配置后重启
docker-compose restart
# 取消使用
docker-compose down
```

## 构建镜像

如果你想自己构建镜像

```bash
cd build/dockerfile
docker build -t php72:v1.0.0 . -f ./Dockerfile-php72
docker build -t php74:v1.0.0 . -f ./Dockerfile-php74
```

## 目录说明

| 目录  | 用途                 | 说明                                                         |
| ----- | -------------------- | ------------------------------------------------------------ |
| build | Dockerfile存放位置   | 镜像构建说明                                                 |
| conf  | 存放php、nginx等配置 | 以各自目录区分如： conf/nginx 存放的为nginx配置              |
| data  | 持久化数据           | 如数据库等，同样应以目录区分                                 |
| logs  | php、nginx等日志目录 | 以目录区分                                                   |
| www   | 项目代码存放处       | 该目录下的文件或目录根据用户自定义，注意调整对应nginx配置即可 |

