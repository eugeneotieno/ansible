# ansible

> A little drop everyday, fills the cup eventually!

## Ping servers
```
ansible all -m ping
```

## More commands
```
ansible all -m gather_facts
ansible all -m dnf -a update_cache=true --become --ask-become-pass
ansible all -m dnf -a "name=* state=latest"  --become --ask-become-pass
ansible all -m gather_facts --limit 192.168.66.14 | grep ansible_distribution
```