KMS
KMS激活服务，slmgr命令激活Windows系统、Office

激活步骤（管理员命令执行）
设置服务 slmgr -skms skms.netnr.eu.org
安装密钥 slmgr -ipk 版本对应秘钥
激活系统 slmgr -ato
可用服务
kms.cangshui.net
skms.netnr.eu.org 推荐使用，维护 CNAME 指向有效的服务
telnet skms.netnr.eu.org 1688 测试服务是否可用
安装服务（Windows）
vlmcs-Windows
安装服务（Linux）
# 一键安装脚本
wget --no-check-certificate https://github.com/teddysun/across/raw/master/kms.sh && chmod +x kms.sh && ./kms.sh

netstat -nxtlp | grep 1688 # 查看端口
/etc/init.d/kms status # 状态
/etc/init.d/kms start # 启动
/etc/init.d/kms stop # 停止
/etc/init.d/kms restart # 重启
./kms.sh uninstall # 卸载
https://teddysun.com/530.html
