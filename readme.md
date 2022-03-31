# throttle cpu
该脚本用于在 Mac 上限制相关进程的最大 CPU 使用率，防止 CPU 过热，阻碍正常开发流程（比如 McAFee 的 VShieldScan 常常搞个 CPU 占用 100%+ 以上）。

# 使用示例
```bash
# 下载脚本到 /usr/bin/throttlecpu
curl https://raw.githubusercontent.com/Tzxhy/mac-throttle/master/throttlecpu -o /usr/bin/throttlecpu && chmod +x /usr/bin/throttlecpu
# 打印帮助信息
throttlecpu -h
# 限制 VShieldScanManager 进程占用最大为1
throttlecpu
# 限制 PROCESS 进程占用最大为 MAX
throttlecpu $PROCESS $MAX
```

依赖 cputhrottle，在脚本执行时，如果本地没有相关依赖，将自动下载。

