If you use a domain that ends .local then the mdns doesn't like it this can be fix by changing the order in the 
```
/etc/nsswitch.conf
```

resolver issue can happen when the order is wrong.

Original
hosts:          files mdns4_minimal [NOTFOUND=return] dns

Fixed
hosts:          files dns mdns4_minimal [NOTFOUND=return]
