# Lab 16 – Extended ACLs

## Objective

Learn how Extended Access Control Lists (ACLs) provide granular traffic filtering based on source address, destination address, protocol, and port number. Configure an Extended ACL to block HTTP traffic while allowing ICMP traffic and verify operation through testing.

---

## Topology

A client PC connected to a web server through a router.

![Topology](topology.png)

---

## Network Configuration

### LAN Network

- Network: 192.168.10.0/24

### WAN Network

- Network: 200.1.1.0/24

### Devices

#### PC0

- IP Address: 192.168.10.10
- Subnet Mask: 255.255.255.0
- Default Gateway: 192.168.10.1

#### R0

- G0/0: 192.168.10.1
- G0/1: 200.1.1.1

#### Server0

- IP Address: 200.1.1.2
- Subnet Mask: 255.255.255.0
- Default Gateway: 200.1.1.1
- HTTP Service Enabled

---

## Device Configuration

### PC0 Configuration

![PC0 Configuration](pc0-ip-config.png)

### Server0 Configuration

![Server0 Configuration](server0-ip-config.png)

### Router Interface Verification

![Router Show IP Interface Brief](router-show-ip-interface-brief.png)

---

## Initial Connectivity Tests

### Successful Ping Before ACL

![Successful Ping Before ACL](successful-ping-before-acl.png)

### Successful HTTP Access Before ACL

![Successful HTTP Access Before ACL](successful-http-before-acl.png)

---

## Extended ACL Configuration

ACL 101 was created to block HTTP traffic destined for Server0 while allowing all other traffic.

### ACL Configuration

![Extended ACL Configuration](extended-acl-config.png)

ACL Entries:

```text
access-list 101 deny tcp any host 200.1.1.2 eq 80
access-list 101 permit ip any any
```

---

## ACL Application

The ACL was applied outbound on interface G0/1.

### ACL Applied To Interface

![ACL Applied To Interface](acl-applied-to-interface.png)

---

## Testing After ACL Deployment

### Successful Ping After ACL

ICMP traffic continued to function.

![Successful Ping After ACL](successful-ping-after-acl.png)

### Failed HTTP Access After ACL

HTTP traffic was successfully blocked.

![Failed HTTP Access After ACL](failed-http-after-acl.png)

---

## ACL Verification

ACL hit counters were examined using:

```bash
show access-lists
```

### ACL Statistics

![Show Access Lists](show-access-lists.png)

---

## ACL Removal

The ACL was removed from the interface.

```bash
interface g0/1
no ip access-group 101 out
```

---

## Connectivity Restoration

HTTP connectivity was restored after ACL removal.

### Successful HTTP Access After ACL Removal

![Successful HTTP Access After ACL Removal](successful-http-after-acl-removal.png)

---

## Key Takeaways

- Extended ACLs can filter traffic by protocol and port number.
- ACLs are processed sequentially from top to bottom.
- ACLs contain an implicit deny statement.
- HTTP uses TCP port 80.
- ICMP and HTTP can be treated differently by ACL rules.
- Extended ACLs provide more granular control than Standard ACLs.

---

## Summary

This lab demonstrated the implementation of an Extended ACL to selectively block HTTP traffic while allowing ICMP traffic. ACL functionality was verified using connectivity testing and ACL hit counters, illustrating how Extended ACLs provide precise traffic filtering capabilities.
