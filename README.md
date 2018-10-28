# High_Performance_Homework
- 极路由刷机，仓库提供了镜像
- Yah3c的安装，需要在Openwrt下安装python
- ipv6的支持
- 修改 /etc/config/dhcp

```
config dhcp 'wan'
        option interface 'wan'
        option ignore '1'
        option dhcpv6 'disabled'
        option ndp 'relay'
        option ra 'relay'
        option master '1'

config dhcp 'wan6'
        option dhcpv6 'relay'
        option ra 'relay'
        option ndp 'relay'
        option master '1'

config dhcp 'lan'
        option interface 'lan'
        option start '100'
        option limit '150'
        option leasetime '12h'
        option dhcpv6 'relay'
        option ra 'relay'
        option ndp 'relay'
```