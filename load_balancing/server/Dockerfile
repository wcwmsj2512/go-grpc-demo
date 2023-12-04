# 使用 Go 1.20 作为基础镜像
FROM golang:1.20
# 使用轻量级的 alpine 作为最终的基础镜像
FROM alpine:latest
# 设置工作目录
WORKDIR /app
# 将本地的 server 可执行文件复制到镜像中的工作目录
COPY server /app/server

# 暴露应用程序的端口（如果有需要）
EXPOSE 50051

# 定义启动命令
CMD ["./server"]