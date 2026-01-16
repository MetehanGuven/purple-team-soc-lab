# SOC Lab Notları

## 🌐 Network Ayarları (✅ Tamamlandı)
- **MacBook IP**: 192.168.1.2 (Splunk SIEM)
- **Windows IP**: 192.168.1.102 (Target/Victim)
- **Kali IP**: 192.168.1.21 (Attacker)
- **Subnet**: 192.168.1.0/24
- **Network Mode**: VMware Bridged

## ✅ Tamamlanan Adımlar

### Windows VM Kurulumu
- [x] Windows 10 Enterprise VM import edildi
- [x] Network: Bridged mode yapılandırıldı
- [x] IP: 192.168.1.102 (DHCP)
- [x] Windows Firewall kapatıldı (lab için)
- [x] PowerShell execution policy: Unrestricted
- [x] RDP aktif edildi (port 3389)
- [x] Windows Defender geçici kapatıldı
- [x] Windows audit logging aktif edildi
- [x] Event log boyutları artırıldı

### Kali Linux Kurulumu
- [x] Network ayarı düzeltildi (NAT → Bridged)
- [x] IP: 192.168.1.21
- [x] Connectivity test: ✅ Başarılı
- [x] Ping testleri: MacBook ve Windows'a erişim OK

### Network Connectivity Tests
```bash
# Kali → Windows
ping 192.168.1.102 ✅

# Kali → MacBook  
ping 192.168.1.2 ✅

# Windows → Kali
ping 192.168.1.21 ✅
```

## 📋 Sonraki Adımlar (Yarın)

### Splunk Kurulumu
- [ ] MacBook'ta Splunk zaten var (kontrol edilecek)
- [ ] Splunk receiving port aç (9997)
- [ ] Windows'a Universal Forwarder kur
- [ ] Windows loglarını Splunk'a gönder
- [ ] Splunk'ta "windows" index'i oluştur

### Sysmon Kurulumu (Windows)
- [ ] Sysmon indir
- [ ] SwiftOnSecurity config dosyası kullan
- [ ] Sysmon'u kur ve başlat
- [ ] Splunk'ta Sysmon loglarını yapılandır

### İlk Saldırı Senaryosu
- [ ] RDP Brute Force (Hydra)
- [ ] Splunk'ta detection rule yaz
- [ ] Alert oluştur
- [ ] Screenshot'lar al

## 🔧 Troubleshooting Notları
- Windows Firewall kapatıldı → ping çalıştı
- Kali network mode Bridged'e alınca aynı subnet'e girdi
- RDP port 3389 açık ve erişilebilir

## 🎯 Proje Hedefi
Purple Team SOC Lab: Gerçek dünya saldırılarını simüle et ve Splunk ile tespit et.

---
**Son Güncelleme**: 2026-01-17
**Durum**: Network kurulumu tamamlandı, Splunk aşamasına hazır
