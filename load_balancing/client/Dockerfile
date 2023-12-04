# 使用 Go 1.20 作为基础镜像
# FROM golang:1.20
# 使用轻量级的 alpine 作为最终的基础镜像
#FROM alpine:latest
FROM golang:1.20
# 复制 entrypoint.sh 到镜像中

FROM centos
COPY entrypoint.sh /entrypoint.sh
RUN ls -l /
# 赋予执行权限
RUN chmod +x /entrypoint.sh

# 设置工作目录
WORKDIR /app
# 将本地的 client 可执行文件复制到镜像中的工作目录
COPY grpc-client /app/client

# 定义启动命令
#CMD ["/entrypoint.sh"]
CMD ["sh", "-c", "echo 'Hello World' && tail -f /dev/null"]
