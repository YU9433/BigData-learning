# 大数据开发学习笔记

## 第一阶段：Linux 基础

### Day 02 —— 文件查找与文本处理

**学习日期：** 2026-07-01

---

## 今日学习目标

- 熟悉 Linux 文件查找命令
- 掌握文本搜索与统计
- 学会查看日志文件
- 理解管道和重定向的使用
- 能够完成简单的日志分析任务

---

## 今日学习内容

### 1. find —— 查找文件

用于在指定目录中查找文件。

#### 查找当前目录所有文件

```bash
find .
```

#### 查找指定文件

```bash
find . -name "Day01.md"
```

#### 查找所有 Markdown 文件

```bash
find . -name "*.md"
```

#### 忽略大小写查找

```bash
find . -iname "*.md"
```

---

### 2. grep —— 搜索文本

grep 用于在文件中查找指定内容，是 Linux 中最常用的文本搜索命令。

例如 student.txt 内容：

```text
Tom
Jack
Lucy
Tom
Alice
Bob
```

#### 查找指定内容

```bash
grep "Tom" student.txt
```

#### 忽略大小写

```bash
grep -i "tom" student.txt
```

#### 显示行号

```bash
grep -n "Tom" student.txt
```

#### 统计出现次数

```bash
grep -c "Tom" student.txt
```

---

### 3. wc —— 文本统计

用于统计文件信息。

#### 查看统计信息

```bash
wc student.txt
```

输出内容依次表示：

- 行数
- 单词数
- 字符数

#### 常用命令

统计行数

```bash
wc -l student.txt
```

统计单词

```bash
wc -w student.txt
```

统计字符

```bash
wc -c student.txt
```

---

### 4. head —— 查看文件前几行

默认查看前十行。

```bash
head student.txt
```

查看前三行

```bash
head -3 student.txt
```

---

### 5. tail —— 查看文件最后几行

默认查看最后十行。

```bash
tail student.txt
```

查看最后两行

```bash
tail -2 student.txt
```

实时查看日志

```bash
tail -f spark.log
```

退出实时查看：

```text
Ctrl + C
```

---

### 6. 管道（|）

管道可以将前一个命令的输出作为后一个命令的输入。

统计 student.txt 中 Tom 出现次数：

```bash
grep "Tom" student.txt | wc -l
```

统计 Markdown 文件数量：

```bash
find . -name "*.md" | wc -l
```

---

### 7. 输出重定向（>、>>）

#### 覆盖写入

```bash
ls > filelist.txt
```

查看结果

```bash
cat filelist.txt
```

#### 追加写入

```bash
echo Hello >> filelist.txt
```

---

## 今日练习

完成了以下练习：

- 创建 student.txt
- 使用 grep 搜索指定内容
- 使用 grep -n 查看行号
- 使用 grep -c 统计出现次数
- 使用 wc 统计文件信息
- 使用 head 查看文件前几行
- 使用 tail 查看文件最后几行
- 使用 find 查找 Markdown 文件
- 使用管道统计 Markdown 文件数量
- 使用重定向保存目录列表

---

## 今日总结

今天学习了 Linux 中最常用的文件查找与文本处理命令。

掌握了 find、grep、wc、head、tail 等命令，并理解了管道（|）和输出重定向（>、>>）的工作原理。

这些命令在日常开发、日志分析以及大数据平台运维中都会频繁使用，也是后续学习 Hadoop、Hive、Spark 和 Flink 的基础。

---

## 遇到的问题

今天整体学习比较顺利，没有遇到较大的问题。

对于管道和重定向的使用还需要多练习，加深理解，提高命令组合使用能力。

---

## 明日学习计划

- Linux 用户管理
- 文件权限
- chmod
- chown
- 用户组
- sudo
- root 用户

进一步理解 Linux 权限管理机制。

---

## 学习时长

约 **2 小时**

---