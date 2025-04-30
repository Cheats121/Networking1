# Networking1
Basic Networking (Switch + 2 PCs)
-------------------------------------------------
# Lab 1: VLANs & Subnetting

### Overview
In this lab you configured basic IPv4 addressing, subnet masks, and VLANs to segment traffic between four PCs and a switch.

### Topology
- **PC1 (Dug)**: 192.168.1.1/25  
- **PC2 (Lemelo)**: 192.168.1.2/25  
- **PC3 (Amba)**: 192.168.1.129/25  
- **PC4 (Tukum)**: 192.168.1.130/25  
- **Switch**: two VLANs (IDs 1 & 2)

### Tasks & Results
1. **IP Assignment & Ping Tests**  
   - Verified host-to-host connectivity within each /25 subnet.  
   - Cross‐subnet pings failed due to missing gateway.

2. **Subnet Mask Change**  
   - Modified mask on Dug/Lemelo to the other /25; confirmed intra‐VLAN comms.

3. **VLAN Configuration**  
   - Created VLAN 1 for PC1/PC2, VLAN 2 for PC3/PC4 on switch.  
   - Traffic isolated: PC1↔PC2 OK, PC3↔PC4 OK, cross‐VLAN blocked.

4. **Wireshark Capture**  
   - Captured ICMP on a switch (no broadcast to non‐participating VLAN).

### Lessons Learned
- How /25 masks carve two subnets.
- VLANs enforce layer-2 isolation.
- Difference between switches vs. hubs in packet visibility.
