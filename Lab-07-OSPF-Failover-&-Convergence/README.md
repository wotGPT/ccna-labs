# Lab 7 – OSPF Failover & Convergence

## Objective

Demonstrate OSPF route convergence by intentionally failing a WAN link and observing how OSPF automatically recalculates routes and restores connectivity through an alternate path.

---

## Topology

Three routers connected in a triangle topology with OSPF running on all router links.

![Topology](topology.png)

---

## Network Configuration

### Network A

- PC0: 192.168.1.10 /24
- Default Gateway: 192.168.1.1

### Network B

- PC1: 192.168.2.10 /24
- Default Gateway: 192.168.2.1

### WAN Networks

- R0 ↔ R1: 10.0.0.0/30
- R0 ↔ R2: 10.0.0.4/30
- R1 ↔ R2: 10.0.0.8/30

---

## PC Configuration

### PC0

![PC0 Configuration](pc0-ip-config.png)

### PC1

![PC1 Configuration](pc1-ip-config.png)

---

## OSPF Neighbor Relationships Before Failure

### R0

![R0 OSPF Neighbors](r0-ospf-neighbors-before-failure.png)

### R1

![R1 OSPF Neighbors](r1-ospf-neighbors-before-failure.png)

### R2

![R2 OSPF Neighbors](r2-ospf-neighbors-before-failure.png)

---

## Routing Tables Before Failure

### R0

![R0 Routing Table](r0-routing-table-before-failure.png)

### R1

![R1 Routing Table](r1-routing-table-before-failure.png)

### R2

![R2 Routing Table](r2-routing-table-before-failure.png)

---

## Simulating a WAN Link Failure

The direct WAN connection between R0 and R1 was intentionally disabled.

### Link Failure Configuration

![Link Failure](link-failure-config.png)

---

## OSPF Neighbor Relationships After Failure

### R0

![R0 OSPF Neighbors After Failure](r0-ospf-neighbors-after-failure.png)

### R1

![R1 OSPF Neighbors After Failure](r1-ospf-neighbors-after-failure.png)

### R2

![R2 OSPF Neighbors After Failure](r2-ospf-neighbors-after-failure.png)

---

## Routing Tables After Failure

### R0

![R0 Routing Table After Failure](r0-routing-table-after-failure.png)

### R1

![R1 Routing Table After Failure](r1-routing-table-after-failure.png)

### R2

![R2 Routing Table After Failure](r2-routing-table-after-failure.png)

---

## Connectivity Verification

Even after the primary WAN link failed, OSPF successfully recalculated routes and maintained connectivity through the alternate path.

![Successful Ping After Failure](successful-ping-after-failure.png)

---

## Link Restoration

The failed WAN link was restored and OSPF re-established normal neighbor relationships.

![Link Restored](link-restored.png)

---

## Key Takeaways

- OSPF dynamically adapts to topology changes
- Multiple paths provide network redundancy
- OSPF recalculates routes automatically during failures
- Route convergence allows communication to continue after outages
- Dynamic routing protocols reduce administrative overhead compared to static routes

---

## Summary

This lab demonstrated OSPF convergence and failover behavior in a multi-router environment. By intentionally failing a WAN connection, OSPF automatically selected an alternate path and restored connectivity without requiring manual route changes.
