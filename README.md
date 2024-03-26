# 答题系统

本答题系统可以支持手机和电脑进行网页在线答题。题型可包括选择题和主观题。本系统可以部署在Github Page上进行使用。

## 代码下载

当系统在Github Page上部署时，如果您想改变在线系统的题目，需要进行以下操作。

1、在本地安装 Node.js 环境和 Git 环境，建议安装 Visual Studio Code 作为编辑器。这里给出教程链接。

[nodejs详细安装步骤](https://blog.csdn.net/muzidigbig/article/details/80493880)

[git安装教程（详细版本）](https://blog.csdn.net/weixin_61485030/article/details/131114418)

[Visual Studio Code (VS Code)安装教程](https://blog.csdn.net/Javachichi/article/details/131438751)

2、下载代码。这一步需要在安装 Git 环境以后进行操作。在本地打开 Git Bash 后输入以下命令。

```sh
git clone https://github.com/myr66666/question-making.git
```

> 注意：在克隆之前需要确定目前命令行所在的目录。如果想拷贝在桌面，可以通过“cd”命令进行跳转。用法：cd [想要跳转的目录]。

## 本地部署

在下载完代码后，需要在本地建立代码运行环境，然后就可以在本地运行系统并测试。

1、在本地打开 Git Bash，输入以下命令安装代码环境

```sh
npm install
```

2、运行系统。

```sh
npm run dev
```

### Compile and Minify for Production

```sh
npm run build
```
