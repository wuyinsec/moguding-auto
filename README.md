# 蘑菇钉自动打卡
![Go](https://github.com/wuyinsec/moguding-golang/workflows/Go/badge.svg)
![schedule-start](https://github.com/wuyinsec/moguding-golang/workflows/schedule-start/badge.svg)
![schedule-end](https://github.com/wuyinsec/moguding-golang/workflows/schedule-end/badge.svg)
[![GitHub language](https://img.shields.io/badge/language-golang-orange.svg)](https://golang.org/)
[![GitHub license](https://img.shields.io/github/license/ToWeLong/zhihu-hot-questions)](https://github.com/wuyinsec/moguding-golang/blob/main/LICENSE)

# 0x00 介绍

此项目由go语言完成，用于研究蘑菇钉/工学云打卡。

利用GitHub Action定时自动打卡。

# 0x01 使用

## 使用方法一：

首先找到`.env.example`文件，打开并按照模板将里面的要求替换成自己的信息，然后去掉文件们后缀`.example`，存储为`.env`文件即可。

~~这种方法仅限于本地或者部署在自己的服务器使用，请不要将有真实个人信息的文件放在github上，已经看到好些人这样了，重要的事情说三遍，这种方法仅限于本地或者部署在自己的服务器使用~~

**测试单个函数(去除cached)**

```bash
go test -count=1 -v -run ^TestWeek$ towelong/mogu/test
```



## 使用方法二：

使用GitHub的Secrets来传递参数，根据`.env.example`文件里的参数在Settings里的Secrets里面新建，value值就填自己的信息，这样就不会导致泄露

# 0x03 计划

## 完成

- [X] 自动签到
- [X] 周报自动编写
- [X] 日志记录
- [X] 打卡增加自定义备注

## TODO

- [ ] 增加详细使用教程

- [ ] 多账号

此项目改自[ToWeLong](https://github.com/ToWeLong/go-mogu)，欢迎大家继续完善

> 重要： 由于蘑菇钉最近更新了接口，导致之前的接口都不可用了，然后还新增了一个sign，也就是签名。
> 非常感谢 `@晓宇` 同学提供的sign算法

***此代码仅供学习，请在下载后24小时内删除，切勿用于违法用途，造成一切后果自行承担，与作者无关***
