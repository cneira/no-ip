*For SmartOS /opt/ is used as /lib is a read only filesystem.*
https://help.joyent.com/hc/en-us/articles/226687187-Read-only-file-systems-on-SmartOS-Instances


1. make
2. pfexec make install
2. pfexec mkdir -p /opt/lib/svc/method/
3. pfexec cp svc-noip2 /opt/lib/svc/method/
4. pfexec chmod +x /opt/lib/svc/method/svc-noip2
5. pfexec svccfg import solaris-noip2.xml
6. pfexec chmod 777 /usr/local/etc/no-ip2.conf
7. svcadm enable noip2


