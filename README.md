For pedagogical use only

# server

Start it using:

```
$ docker run -p 2222:22 -ti jordi/sshd
root@c6c3fa946666:/# service ssh start
 * Starting OpenBSD Secure Shell server sshd        [ OK ]
```

Configure root 
```
root@c6c3fa946666:/# cd
root@c6c3fa946666:~# cd .ssh
root@c6c3fa946666:~/.ssh# cat > authorized_keys
ssh-rsa AAAA...
^D
```

# client

```
$ docker run -ti jordi/ssh
ssh -i privatekeyfilename root@localhost -p 2222
```