# Authentication Logs

CentOS `/var/log/secure` valid login example.

```shell
Dec  6 12:00:00 <HOSTNAME> sshd[1509387]: Accepted password for root from <CONNECTING HOST> port 31273 ssh2
Dec  6 12:00:00 <HOSTNAME> sshd[1509387]: pam_unix(sshd:session): session opened for user root by (uid=0)

```

Ubuntu `/var/log/auth.log` valid login example.

```shell
Dec  6 12:00:00 <HOSTNAME> sshd[1146601]: Accepted password for root from <CONNECTING HOST> port 1181 ssh2
Dec  6 12:00:00 <HOSTNAME> sshd[1146601]: pam_unix(sshd:session): session opened for user root by (uid=0)

To Be able to find specific commands in the logs use the following command. It shows all of the parts in the auth.log that have root in the system. 
```
grep "root" less /var/log/auth.log
```

As you can see they are the same.
