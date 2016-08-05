---
title: CMakeLists.txt文件
date: 2016-08-05 13:24:18
tags: c
---

- project 指定工程名称
- set 设置变量
- add_executable 添加工程的源文件。
- aux\_source\_directory(. XXX) 指定当前目录为资源目录，命名为XXX
- add\_library(MathFunctions ${DIR\_LIB_SRCS}) 用指定源文件产生库，命名为MathFunctions。
- add_subdirectory(math) 添加子目录math
- target\_link\_libraries(Demo MathFunctions) 向工程Demo中添加链接库MathFunctions
- link_directories 指定链接库目录