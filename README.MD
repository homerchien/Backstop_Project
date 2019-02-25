# 自动化测试框架

[TOC]

## 1.  概述

> 本项目为 backstop 自动化测试项目,用于视觉回归测试

## 2. 项目结构&命名规范

```shell
├── README.MD							# README	                             
├── backstop_data                       
│	├── bitmaps_reference               # 存放baseline图片
│	├── bitmaps_test                    # 存放每次执行测试的图片（按时间生成子文件夹）
│	├── engine_scripts	                # 存放脚本文件（按engine进行区分）
│   └── html_report                     # 测试报告
└── backstop.json                       # 测试套
```


### 2.1 基本介绍

默认情况下，BackstopJS将backstop.json放在项目的根目录中。并且默认情况下，BackstopJS在调用时会查找此文件。

backstop.json为测试套，必须包含id，viewports，scenarios字段。通过配置backstop.json生成对应测试用例

- id - 使用id为截图名
- viewports - 配置执行用例时的设备大小
- scenarios - 测试用例的集合
[参考url](https://github.com/garris/BackstopJS#using-backstopjs)

## 3. backstop 安装

### 3.1 安装backstop

```shell
执行：
npm install -g backstopjs
```

### 3.2 用例执行

```bash
# 更新基线图片
backstop approve
# 执行用例
backstop test
```
[参考url](https://github.com/garris/BackstopJS#generating-test-bitmaps)

