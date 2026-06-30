# 大数据开发学习笔记

## 第一阶段：Linux 基础

### Day 01 —— Linux 基础命令

**学习日期：** 2026-06-30

---

## 今日学习目标

- 了解 Linux 操作系统及其在大数据开发中的作用
- 熟悉 Linux 的目录结构
- 掌握常用文件和目录管理命令
- 能够完成基本的文件创建、复制、移动和删除操作

---

## 今日学习内容

### 1. Linux 简介

Linux 是一种开源操作系统，也是目前企业服务器最常使用的操作系统。

在大数据开发领域，Hadoop、Spark、Hive、Flink、Kafka 等框架几乎都运行在 Linux 环境，因此掌握 Linux 是学习大数据开发的第一步。

---

### 2. Linux 目录结构

了解了 Linux 与 Windows 不同的目录结构，Linux 只有一个根目录 `/`。

常见目录如下：

| 目录 | 作用 |
|------|------|
| / | 根目录 |
| /home | 用户目录 |
| /root | root 用户目录 |
| /etc | 系统配置文件 |
| /usr | 软件安装目录 |
| /var | 日志文件 |
| /tmp | 临时文件 |
| /opt | 第三方软件安装目录 |

---

### 3. 常用命令

#### （1）查看当前目录

```bash
pwd
```

---

#### （2）查看目录内容

```bash
ls
ls -l
ls -a
```

---

#### （3）切换目录

```bash
cd
cd ..
cd /
cd ~
```

---

#### （4）创建目录

```bash
mkdir project
mkdir -p project/data/raw
```

---

#### （5）创建文件

```bash
touch test.py
touch a.txt b.txt c.txt
```

---

#### （6）查看文件内容

```bash
cat 文件名
```

---

#### （7）复制文件

```bash
cp a.txt b.txt
cp -r project backup
```

---

#### （8）移动文件或重命名

```bash
mv a.txt test/
mv old.txt new.txt
```

---

#### （9）删除文件

```bash
rm 文件名
rm -r 文件夹
rm -rf 文件夹
```

> **注意：** 删除命令不可恢复，使用 `rm -rf` 时需格外谨慎。

---

#### （10）查看帮助

```bash
man ls
ls --help
```

---

## 今日练习

完成了以下练习：

- 创建 BigData 学习目录
- 创建 Linux、Python、Java、Spark、Hive 子目录
- 创建 day01/practice 文件夹
- 创建 hello.txt、test.py、demo.sql 文件
- 复制 Linux 文件夹为 Linux_backup
- 删除 demo.sql 文件

---

## 今日总结

今天主要学习了 Linux 的基础知识以及常用命令，对 Linux 的目录结构有了初步认识，并掌握了文件和目录的基本管理操作。

通过练习，对 `pwd`、`ls`、`cd`、`mkdir`、`touch`、`cp`、`mv`、`rm` 等命令有了基本了解，也认识到 Linux 是后续学习大数据开发的重要基础。

---

## 遇到的问题

今天整体学习过程比较顺利，没有遇到较大的问题。

部分命令参数（如 `-r`、`-a`、`-l` 等）还需要在后续练习中进一步熟悉，加深记忆。

---

## 明日学习计划

- 文件查找命令（find、locate）
- 文件搜索（grep）
- 文件统计（wc）
- 文件压缩与解压（tar、zip）
- 输出重定向与管道（>、>>、|）

继续熟悉 Linux 常用命令，为后续学习 Shell 编程打下基础。

---

## 学习时长

约 **2 小时**

---