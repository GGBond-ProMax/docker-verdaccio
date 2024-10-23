# 使用官方的 Node.js 镜像作为基础镜像
FROM node:18.20.4-alpine AS verdaccio

# 定义工作目录变量
ENV WORKDIR=/usr/src/app

# 创建工作目录
WORKDIR $WORKDIR

# 更换 npm 源并安装 verdaccio
RUN npm config set registry https://registry.npmmirror.com && \
    npm install -g verdaccio

# 设置要暴露的端口
EXPOSE 4873

# 直接运行 verdaccio
CMD ["verdaccio", "--listen", "0.0.0.0:4873"]
