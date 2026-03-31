# IPSec Site-to-Site Mesh VPN Lab

## Overview | Aperçu

**EN:**  
This project demonstrates the implementation of secure site-to-site IPSec VPN tunnels between multiple locations using a mesh topology. It ensures encrypted communication, routing integration, and high availability across sites.

**FR :**  
Ce projet présente la mise en place de tunnels VPN IPSec site-à-site entre plusieurs sites avec une topologie maillée. Il permet d’assurer le chiffrement du trafic, l’intégration du routage et une communication sécurisée.

---

## Real-World Scenario | Mise en situation

**EN:**  
A company connects its branches (HQ, LAN, Montreal) over the Internet using IPSec tunnels to protect data and ensure secure communication.

**FR :**  
Une entreprise connecte ses sites (siège, LAN, Montréal) via Internet à l’aide de tunnels IPSec pour sécuriser les communications.

---

## Technologies

- IPSec VPN (Site-to-Site)
- ISAKMP / IKE (Phase 1)
- ESP (Phase 2)
- AES encryption
- SHA authentication
- Diffie-Hellman (Group 5)
- OSPF / Static routing
- Cisco IOS

---

## Network Architecture

- Toronto router (HQ)
- R_LAN router (Branch)
- Montreal router (Branch)
- ISP switch (untrusted network)
- End devices (PC_HQ, Admin_LAN, Mtl_admin)

---

## Configuration Steps

### Step 1 – Base Configuration

- IP addressing and routing (OSPF or static)
- Connectivity verification between all sites

### Step 2 – IPSec Tunnel (Toronto ↔ R_LAN)

- Encryption: AES-256  
- Hash: SHA-1  
- Authentication: Pre-shared key  
- DH Group: 5  
- Key: Georges123  

### Step 3 – IPSec Mesh (Toronto ↔ Montreal)

- Encryption: AES  
- Hash: SHA  
- Authentication: Pre-shared key  
- DH Group: 5  
- Key: Cisco111  

---

## Verification

- Ping between all sites  
- Traceroute validation  
- `show crypto isakmp sa`  
- `show crypto ipsec sa`  

---

## Results | Résultats

**EN:**  
- Secure communication between all sites  
- Encrypted traffic over IPSec tunnels  
- Mesh connectivity achieved  

**FR :**  
- Communication sécurisée entre tous les sites  
- Trafic chiffré via IPSec  
- Connectivité complète en maillage  

---

## Conclusion

**EN:**  
This project demonstrates how IPSec VPNs secure inter-site communication over public networks.

**FR :**  
Ce projet montre comment les VPN IPSec permettent de sécuriser les communications entre sites via Internet.
