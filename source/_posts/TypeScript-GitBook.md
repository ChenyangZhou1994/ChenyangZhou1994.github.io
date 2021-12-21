---
title: TypeScript-GitBook
top: false
cover: false
toc: true
mathjax: true
date: 2021-11-20 20:51:30
password:
summary:
tags: TypeScript
categories: Web前端
---

# TypeScript - GitBook

## 1.TypeScript环境搭建

### 1.1 安装Node.js

推荐使用nvm对Node.js进行管理。

Windows 10：

- NVM for Windows [传送门](https://github.com/coreybutler/nvm-windows/releases)

Linux [传送门](https://github.com/nvm-sh/nvm#installing-and-updating)

```shell
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
```

```shell
wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
```

使用cURL和 Wget 命令都可以。

修改环境变量 - (`~/.bash_profile`, `~/.zshrc`, `~/.profile`, or `~/.bashrc`).

```shell
export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"
[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" # This loads nvm
```

macOS Monterey version 12.10.1 使用brew进行安装

```shell
brew install nvm
```

安装Node.js：

```shell
nvm install v17.1.0
```

检查安装是否成功：(无报错即创建成功)

```shell
node -v
```

### 1.2 安装TypeScript

```shell
npm install -g typescript
```

检查是否安装成功：(无报错即创建成功)

```she
tsc -v
```

### 1.3 使用tsc对ts文件进行编译

以macOS为例

- 创建ts文件 - touch 01_hello.ts

  - 编辑内容并保存 -  console.log('Hello TS');

- 使用tsc编译ts文件

  ```she
  tsc 01_hello.ts
  ```

  运行结果：

  ![1.3-fig1](/Users/crius/Desktop/ChenyangZhou1994.github.io/source/imgs/typescript/ts-1.3-fig1.jpg)

## 2. 基本类型

### 2.1 类型声明

```typescript
//声明一个a变量，指定为number
let a: number;
//a只能被赋值数字类型
a = 10
a = 1.1
a = '1.5' //报错
//声明一个b变量，指定为string
let b: string;
b = '1.5'
b = 1.5 //报错
//声明变量直接赋值
let c: boolean = true;
c = 123 //报错

//指定参数和返回值类型
function sum(a: number, b: number) : number {
    return a + b;
}

sum(123, 456)
sum(123, '456') //报错
```

### 2.2 基础类型

|  类型   |    例子    |   描述   |
| :-----: | :--------: | :------: |
| number  | 1, -1, 1.5 | 任意数字 |
| string  |            |          |
| boolean |            |          |
| 字面量  |            |          |
|   any   |            |          |
| unknown |            |          |
|  Void   |            |          |
|  Never  |            |          |
| Object  |            |          |
|  Array  |            |          |
|  Tuple  |            |          |
|  Enum   |            |          |



