# CVE-2018-6574 POC

## 相关链接

- https://nvd.nist.gov/vuln/detail/CVE-2018-6574
- http://blog.nsfocus.net/cve-2018-6574/
- https://github.com/neargle/CVE-2018-6574-POC

## 运行

```bash
go get github.com/hitwhfanke/CNNVD-201802-203
```

## 使用说明

payload 在: https://github.com/hitwhfanke/CNNVD-201802-203/blob/master/calc.c#L10

现在已经用 CGO 的特性支持了全平台，linux `go get` 之后会新建一个 `/tmp/go-rce-poc` 文件，MAC 和 Windows 还是老套的弹计算器。

*PS. Windows 的部分 GCC 可能没有 `--enable-plugin` 支持, 会爆 ` error: plugin support is disabled; configure with --enable-plugin`. 当前的 POC 需要 gcc 支持 `--enable-plugin`.*

## VERSION

- before 1.8.7
- before 1.9.4
- before Go 1.10rc2

## 致谢

KINGSABRI
