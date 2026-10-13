
# 任务一：环境配置 

## 一、理解任务要求

- 配置 Python 深度学习环境
  - Miniconda 安装
  - Python 虚拟环境创建
  - PyTorch 安装
  - Git 简单使用与 GitHub 个人仓库搭建

---

## 二、我的思路与执行及报错后处理

### miniconda 的安装

1. 我先上了 Anaconda 的官网，按照其指令下载了 miniconda
2. 我让豆包直接给我了国内镜像站的下载路径
3. 我尝试开一个新的虚拟环境

   ⚠ **报错：豆包给我的其中一个路径是错的**

```
UnavailableInvalidChannel: HTTP 404 NOT FOUND
 for channel anaconda/pkgs/pytorch <https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/pytorch>
 ```

- 可知它给我说明了路径不存在，于是我亲自去清华镜像站官网查出正确路径，该路径中 `/pkgs/pytorch/` 应该是 `/cloud/pytorch/`
- 我再次输入 `conda create -n udlab python=3.11`，输出 `done`，环境创建完成

### 安装 PyTorch

1. 版本选择：因为我的电脑用的不是 NVIDIA 显卡，所以我直接选择了 CPU 版本
2. 我开始修改 pip 配置，换成国内镜像版，这样下载快一点
3. 然后我开始下载 `pip install torch torchvision torchaudio`，共三个包
4. 最后我进 python 后输入 `import torch` 未报错，安装成功

### Git 与 GitHub 连接配置

1. 我先到 GitHub 中建立了一个新仓库（Allero.II）
2. 我不知道怎样连接 Git 与 GitHub，在豆包指引下我把 git 的用户名和邮箱设置为和 GitHub 的一样
3. 豆包按我要求生成了一个密钥 `ssh-keygen -t ed25519 -C "googonce11223@gmail.com"`，默认路径，不设密码
（抱歉之前这里写成了“我按豆包要求”，我记不得是我自己打错了还是叫豆包帮我修格式时它干的好事）
4. 我把密钥复制下来，到 GitHub 网站的 SSH keys 页面添加上了
5. 我输入 `ssh -T git@github.com` 测试连接，输入 yes

⚠ **报错：它说 Permission denied，权限被拒绝了，配对失败**

```
Warning: Permanently added 'github.com' (ED25519) to the list of known hosts.
git@github.com: Permission denied (publickey).
```

- 我自己整了半天，又新开了一个仓库，等等等等，依然失败，最后问豆包，它让我检查一下有没有把密钥复制错，果然是复制漏了一节
- 再次测试，显示连接成功

### 笔记书写与上传

1. 我先把仓库克隆到本地
2. 我进入文件夹后新建了一个文件
3. 因为不会写 markdown 文件，所以我先自己简要学习了一下，然后自己先写了，再叫豆包帮我修改了一下格式

---

## 三、AI 使用说明

我此次主要用豆包 Lite 辅助，主要用它收集资料、排查错误、以及讲解学习。尤其是在设置 SSH 密钥方面、Markdown 文档书写方面，帮助很大，节省了四处搜资料、找方法的时间。

---

## 四、收获与总结

1. 学会基本的 Markdown 文档书写格式
2. 养成每一步都要验证的意识
3. 学会判断报错信息、排查问题




