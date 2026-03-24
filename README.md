# Secure Multi-Site Enterprise Network Design with IPsec VPN and HSRP

## 📌 Proje Özeti / Project Overview

Bu projede Cisco Packet Tracer kullanılarak İstanbul (Merkez) ve Ankara (Şube) arasında güvenli ve yüksek erişilebilir bir kurumsal ağ tasarlanmıştır. 

A multi-site enterprise network topology has been designed and implemented using Cisco Packet Tracer. The project simulates secure and redundant communication between a headquarters (Istanbul) and a branch office (Ankara).

---

## 🧱 Kullanılan Teknolojiler / Technologies Used

- VLAN (Data & Voice Segmentation)
- Inter-VLAN Routing (Router-on-a-Stick)
- HSRP (Hot Standby Router Protocol)
- IPsec Site-to-Site VPN
- NAT (PAT)
- DHCP
- ACL (Access Control Lists)
- SSH (Secure Remote Access)

---

## 🗺️ Topoloji / Network Topology

![Topology](https://github.com/mertroot/secure-multisite-network/blob/main/secure-multisite-network/Topoloji.png)

---

## ⚙️ Yapılandırma Detayları / Configuration Details

### 🔹 VLAN ve Segmentasyon
- VLAN 10 → Data
- VLAN 20 → Voice
- VLAN 50 → Ankara LAN
- Broadcast domain küçültülerek performans ve güvenlik artırıldı

---

### 🔹 Inter-VLAN Routing
- Router-on-a-Stick kullanıldı
- Subinterface yapılandırmaları ile VLAN'lar arası iletişim sağlandı

---

### 🔹 HSRP (High Availability)
- İstanbul tarafında iki router ile redundancy sağlandı
- Virtual Gateway: `192.168.10.1`
- Active/Standby yapısı ile kesintisiz erişim

---

### 🔹 DHCP
- Ankara tarafında DHCP server ile dinamik IP dağıtımı yapıldı
- Client cihazlar otomatik IP aldı

---

### 🔹 NAT (PAT)
- İç ağdan dış ağa erişim için NAT overload yapılandırıldı
- Private IP → Public IP dönüşümü sağlandı

---

### 🔹 IPsec VPN
- İstanbul ve Ankara arasında site-to-site VPN kuruldu
- Trafik şifrelenerek güvenli iletişim sağlandı

---

### 🔹 ACL (Security)
- ICMP (ping) trafiği kısıtlandı
- Sadece SSH (port 22) erişimine izin verildi
- Güvenli erişim politikası uygulandı

---

### 🔹 SSH (Secure Access)
- Router üzerinde SSH aktif edildi
- Sadece yetkili kullanıcı erişimi sağlandı

---

## 🧪 Test Senaryoları / Testing

- ✔ VLAN’lar arası iletişim test edildi
- ✔ DHCP IP dağıtımı doğrulandı
- ✔ HSRP failover test edildi
- ✔ VPN üzerinden şubeler arası iletişim sağlandı
- ✔ SSH erişimi başarılı
- ❌ ICMP erişimi bilinçli olarak engellendi

---

## 📁 Proje Dosyaları / Project Files

- `network.pkt` → Packet Tracer dosyası
- `topology.png` → Ağ topolojisi
- `docs/` → Proje dokümantasyonu

---

## 🎯 Amaç / Purpose

Bu proje, gerçek dünyadaki kurumsal ağ tasarımını simüle ederek:
- Güvenli iletişim (VPN)
- Yüksek erişilebilirlik (HSRP)
- Ağ segmentasyonu (VLAN)
- Erişim kontrolü (ACL)

gibi konularda pratik deneyim kazandırmayı amaçlamaktadır.

