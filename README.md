# ZJL 免流防跳脚本
**整合 tiny 和 clnc 的免流防跳**

****
### ZJL核心使用选项（不带参数）:

```txt
-o 或 --open                   开启免流
-c 或 --close                  关闭免流
-d 或 --display                显示界面
-i 或 --info                   显示信息
-h 或 --help                   查看帮助
-v 或 --version                查看版本

最多只支持三个有效选项:
	-o 和 -c 二选一 不可同时选择
	-h 和 -v 只可单独使用 例: ZJL -h
```

### 注意事项:
```txt
1. 不支持纯CNS
2. 不支持tiny模式里有一个接口 然后自动获取验证的那种模式
3. 不支持ipv6免流

4. 如果删除了MLbox 将不支持检测HTTP和HTTPS联网 以及检测UDP联网
5. 如果删除了busybox并且手机没有安装busybox的话 将不支持显示运行中的模式名 以及显示已用流量
6. 如果手机不支持iptables的multiport模块 本机和共享的放行端口将会放行不了端口范围

7. tiny模式的uid写0 3003 3004之一 不然会没网
8. 本机成功代理了UDP的话 共享UDP放行将无效
9. 如果开了免流后手机有什么奇怪的毛病的话 试试防跳放行IPv6
10. 安卓11用tiny可能会没网
11. 如果装了面具的话 可以直接防跳配置 [开机自启] 填面具 跟刷模块效果一样的自启
```

### 2.0 Beta28 更新日志:
```txt
1. 修复华为手机读取手机信息错误
2. 修复配置里等号和所填的有空格导致读取失败
3. 修复部分系统显示运行中的模式名错误
4. 修复部分系统开机自启无效 我加了几秒的延时
5. 修复开机自启更改路径后导致自启失效

6. 升级本机[共享TCP端口]和[共享UDP端口]功能 可以放行端口范围

7. 更改面具版的防跳路径到 /data/ZJL2.0_magisk 可以避免挂载问题
```

****



[源码 脚本 面具模块 百度云链接](https://pan.baidu.com/s/1r-yhDXQWouOQHT6XSQJ__Q "ZJL") 旧版本有残缺 少了些 当时没保留下来 太久了 不过新版本都有
