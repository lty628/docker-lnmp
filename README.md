# docker-lnmp

## 使用

```bash
docker-compose up -d
```

## 构建镜像

如果你想自己构建镜像

```bash
cd build
docker build -t php72:v1.0.0 . -f ./Dockerfile-php72
```

