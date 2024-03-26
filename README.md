# 答题系统

本答题系统可以支持手机和电脑进行网页在线答题。题型可包括选择题和主观题。本系统可以部署在Github Page上进行使用。

## 代码下载

当系统在Github Page上部署时，如果您想改变在线系统的题目，需要进行以下操作。

### 在本地安装 Node.js 环境和 Git 环境，建议安装 Visual Studio Code 作为编辑器。这里给出教程链接

[nodejs详细安装步骤](https://blog.csdn.net/muzidigbig/article/details/80493880)

[git安装教程（详细版本）](https://blog.csdn.net/weixin_61485030/article/details/131114418)

[Visual Studio Code (VS Code)安装教程](https://blog.csdn.net/Javachichi/article/details/131438751)

### 下载代码。这一步需要在安装 Git 环境以后进行操作。在本地打开 Git Bash 后输入以下命令

```sh
git clone https://github.com/myr66666/question-making.git
```

> 注意：在克隆之前需要确定目前命令行所在的目录。如果想拷贝在桌面，可以通过“cd”命令进行跳转。用法：cd [想要跳转的目录]。

## 本地部署

在下载完代码后，需要在本地建立代码运行环境，然后就可以在本地运行系统并测试。

### 在本地打开 Git Bash，输入以下命令安装代码环境

```sh
npm install
```

### 运行系统

1、测试环境，可用于热部署（边修改边运行，实时展现修改内容）。

```sh
npm run dev
```

当出现以下内容时，输入展示的网址即可查看运行效果

```sh
  VITE v3.1.8  ready in 521 ms

  ➜  Local:   http://localhost:5173/question-making/
  ➜  Network: use --host to expose
```

2、生产环境，最接近真实效果。**注意：这一步在第一次运行下载的代码时必须操作，之后每一次提交代码前都建议操作。**

```sh
npm run build
```

## 修改提交

想要修改题目的内容，需要进行如下操作。**注意：想要进行本步需要先进行“代码下载”、“本地部署”两步。**

1、打开 Git bash ,拉取代码的更新。这一步防止有其他人更新远端代码而造成冲突。

```sh
git pull
```

2、进行热部署

```sh
npm run dev
```

当出现以下内容时，输入展示的网址即可查看运行效果

```sh
  VITE v3.1.8  ready in 521 ms

  ➜  Local:   http://localhost:5173/question-making/
  ➜  Network: use --host to expose
```

3、修改题目

题目的路径位于 src/assets/data/question2.json 中。本系统只需更改本文件即可。

4、提交更改。先在命令行中ctrl+c退出热部署状态，然后输入以下命令。

```sh
npm run build
git add .
git commit -m "可修改的注释内容"
git push
```

5、云端部署。代码虽然已经提交，但需要在云端将新的内容部署上去。

```sh
bash deploy-github.sh
```
