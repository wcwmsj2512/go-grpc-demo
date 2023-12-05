
FROM golang:1.20
FROM centos
COPY entrypoint.sh /entrypoint.sh
# 赋予执行权限
RUN chmod +x /entrypoint.sh

# 设置工作目录
WORKDIR /app
# 将本地的 client 可执行文件复制到镜像中的工作目录
COPY grpc-client /app/client

# 定义启动命令
CMD ["/entrypoint.sh"]
#CMD ["sh", "-c", "echo 'Hello World' && tail -f /dev/null"]
