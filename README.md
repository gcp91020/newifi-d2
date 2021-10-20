```
cat /etc/hotplug.d/iface/20-firewall
[ "$ACTION" = "ifup" -a "$INTERFACE" = "wireguard" ] && {
    ip route add 192.168.128.0/24 via 192.168.125.253
}

[ "$ACTION" = "ifup" -a "$INTERFACE" = "eth0" ] && {
  ip route add 192.168.120.0/24 via 192.168.128.249
  ip route add 192.168.120.0/24 via 192.168.128.249
}
```
