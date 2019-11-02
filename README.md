# zabbix-proxy-mysql-nginx
zabbix分布式监控

# 安装对应的agent
rpm -Uvh https://repo.zabbix.com/zabbix/4.0/rhel/7/x86_64/zabbix-release-4.0-1.el7.noarch.rpm  
yum install zabbix-agent -y  
systemctl start zabbix-agent  
systemctl enable zabbix-agent  


# 修改agentd.conf (使用默认的被动模式)
PidFile=/var/run/zabbix/zabbix_agentd.pid  
LogFile=/var/log/zabbix/zabbix_agentd.log  
LogFileSize=0  
Server=182.19.0.136  
Hostname=agent3  
Include=/etc/zabbix/zabbix_agentd.d/*.conf  

