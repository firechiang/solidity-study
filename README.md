#### 一、安装开发工具 remix-project（也可直接使用官方提供服务 https://remix.ethereum.org/）
```
# 下载源码
$ git clone https://github.com/ethereum/remix-project.git
$ cd cd remix-project
# 切换到最新稳定分支
$ git checkout xxx
# 全局安装 nrwl 客户端（注意：该软件需要 Nodejs 12.9以上版本）
$ yarn global add @nrwl/cli
$ yarn install
$ yarn run build:libs # Build remix libs
# 编译打包
#$ nx build remix-ide --with-deps
$ yarn nx build
# 全局安装本地文件共享服务（用于加载本地文件）
$ npm install -g @remix-project/remixd
```

#### 二、启动开发工具 remix-project
```
# 启动开发工具服务（访问：http://127.0.0.1:8080）
#$ nx serve
$ yarn nx serve
# 启动本地文件共享服务，将目录 /home/chiangfire/data-dev/workspace-solidity 共享给 http://127.0.0.1:8080 服务
# 注意：另起命令行执行，而且服务域名要和浏览器上一致。该共享程序启动较慢需耐心等待
$ remixd -s /home/chiangfire/data-dev/workspace-solidity --remix-ide http://127.0.0.1:8080
#remixd -s /home/chiangfire/data-dev/workspace-solidity --remix-ide https://remix.ethereum.org
```

