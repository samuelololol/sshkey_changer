# sshkey_changer

A tool to deploy ssh public/private key to multiple hosts


# HOWTO

1. Edit config

## config.ini sample
```
[hosts]
hosts=host1_tag, host2_tag

[host1_tag]
ip=           #hostname or ip
port=         #ssh port
account=      #account
password=     #password
key_path=     #id_pub file's fullpath
ssh-copy-id=  #whether to exec ssh-copy-id to this target or not

[host2_tag]
ip=192.168.1.2
port=22
account=guest1
password=guest_password
key_path=/home/guest1/.ssh/id_rsa
ssh-copy-id=yes
```

2. Create key

```
$ ./keygen
```

3. Deploy

```
$ ./deploy
```
