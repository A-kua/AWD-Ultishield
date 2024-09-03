# AWD-Ultishield
AWD 最强之盾
# awd 最强通防

**本工具目的是终结所有的AWD比赛。**

如有需要，可以通过邮箱support@akua.fan联系。

## 特点

- 无 侵 入: 不修改任何文件
- 普    适: 可以防web可以防pwn
- 便    捷: 提供静态二进制，无需担心动态链接问题
- 无    敌: 可作用于子进程

### 环境需求

**仅**需要上传文件的权限，将本工具上传后，对其使用`chmod 777`

### 工具说明

由本工具所启动的进程，当他或他的子进程调用open(syscall) 打开路径中含有flag字样的文件时，其得到的fd将会被*重定向*到/home/akua_fake_flag

### 使用方法

你可以把本工具理解为sh。

只需要使用本工具执行原命令即可。

例如
```shell
java -jar cms.jar
```
使用本工具后，变为
```shell
./waf_iseal java -jar cms.jar
```

再如
```shell
./restart.sh
```
变为
```shell
./waf_iseal ./restart.sh
```
### 工具测试

下载本工具后，使用本工具启动sh/bash
```shell
./waf_iseal sh
```
随后执行诸如cat /flag等读取flag的指令

### 已验证的比赛

2024长城杯
