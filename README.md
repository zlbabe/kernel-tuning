# Kernel tuning

The right kernel tuning to increase the performance of your server.

## HAProxy
```
# Increase source TCP port range.
net.ipv4.ip_local_port_range=1025 65000

# Increase the number of syn requests in the queue.
net.ipv4.tcp_max_syn_backlog=100000

# Increase the number incoming connections in the queue.
net.core.netdev_max_backlog=100000

# Increase number of incoming connections.
net.core.somaxconn=65000

# The first value: the minimum receive buffer for each TCP connection.
# The second value: the default receive buffer allocated for each TCP socket.
# The third value:  the maximum receive buffer that can be allocated for a TCP socket.
net.ipv4.tcp_rmem=4096 16060 64060

# The fist value: the minimum TCP send buffer space available for a single TCP socket
# The second value: the default send buffer space allowed for a single TCP socket
# The third value: the maximum TCP send buffer space
net.ipv4.tcp_wmem=4096 16384 262144

```

## License
The source code in this repo is licenced under the GPL 3
