
tcpdump 侦听tcp包，类似wireshark
iptables 防火墙工具，过滤数据包
过滤RST包  
    sudo iptables -I INPUT -p tcp --tcp-flags SYN,FIN,RST,URG,PSH RST -j DROP
    iptables -A OUTPUT -p tcp -dport 50000 --tcp-flags RST RST -j DROP
    -I 插入(insert)规则 -A 添加(append)规则 -D 删除(delete)规则
