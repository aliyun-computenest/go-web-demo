# Go Web示例应用
此应用是一个快速入门示例，用于展示阿里云应用管理如何使用Buildpacks构建部署Go应用。
Buildpacks从go.mod中读取go的版本。
注意有些go Buildpack实现要求go.mod中的module name至少包含一个/

# 在阿里云应用管理上部署应用
阿里云应用管理支持从Git仓库部署此应用。可以从以下入口访问应用管理:

- [系统运维管理控制台入口](https://oos.console.aliyun.com/app)
- [云服务器控制台入口](https://ecs.console.aliyun.com/app)
- [计算巢控制台入口](https://computenest.console.aliyun.com/app)

步骤：
1. 在创建应用页面，选择“通过Git仓库创建”
2. 在“应用来源”部分，选择Git平台，授权应用管理使用您的Git平台账号。在“Git clone地址”上填写本仓库的地址
4. 本应用默认应用使用80端口。如需变更，在“应用监听端口”参数指定。
5. 按需修改云服务器的配置。
6. 点击创建后应用开始部署。
7. 部署成功后访问`http://公网IP:端口`

# 手工构建和执行应用
前提条件：安装go 1.20
构建应用：在应用代码所在目录，执行`go build`，会编译出go-web-demo二进制文件
执行应用：执行go-web-demo
打开浏览器，访问`http://localhost`

