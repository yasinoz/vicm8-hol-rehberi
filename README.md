# VMware vSphere ICM 8.0 — Türkçe HOL Lab Rehberi

Bu depo, **VMware vSphere: Install, Configure, Manage [V8]** (ICM 8.0) eğitimi
için hazırlanmış **Türkçe çalışma rehberidir**. Amaç: sıfırdan gelen bir
öğrencinin, VMware **Hands-on Labs (HOL)** ortamında 5 gün boyunca adım adım
pratik yapabilmesi — her şey Türkçe anlatılarak, HOL erişimi ve lab linkleri
dahil.

> Bu rehber resmi VMware kursunun **yerine geçmez**; onun **yanında** okunur.
> Adımlar ve açıklamalar özgün Türkçe'dir; VMware'in telifli PDF'leri ve resmi
> Lab Guide'ı çoğaltılmaz, onlara **yönlendirilir**.

---

## ⚠️ Önce oku — sürüm farkı (önemli)

VMware HOL kataloğu artık **VMware Cloud Foundation (VCF) 9.1** üzerine kurulu
(**HOL-27xx** serisi). Klasik "vSphere 8" HOL lab'ları emekliye ayrıldı.

Bunun pratik sonucu:
- HOL ortamında göreceğin arayüz **vSphere 9 / VCF 9.1**'dir; bu kursun konusu
  ise **vSphere 8**. **Kavramların neredeyse tamamı birebir aynıdır**, sadece
  bazı ekranlar bir sürüm daha yenidir. Fark olan yerleri rehberde
  **"8 ↔ 9.1 farkı"** notuyla işaretledik.
- HOL lab'ları "sıfırdan kur/yapılandır" tutorial'ı değil, **"ne yeni / deep
  dive"** odaklıdır. Bu yüzden ICM'in temel adımlarını (ESXi kurulumu, vCenter
  dağıtımı, sıfırdan vSwitch/datastore, ilk VM, vMotion, HA/DRS) **eğitmen
  canlı gösterir** ve bu rehber Türkçe olarak anlatır; öğrenci HOL'de pekiştirir.

Kısaca: **HOL = kavram pekiştirme + keşif**, **eğitmen lab'ı + bu rehber =
temelleri sıfırdan öğretme.**

Her günün **"Bölüm C — Eğitmen lab demosu"** kısmında bu temel adımlar **tam
adım adım** yazılıdır (ESXi kurulumu, vCenter'a host ekleme, vSwitch/vDS,
iSCSI/NFS datastore, VM/template/snapshot, vMotion/Storage vMotion, HA/DRS,
Lifecycle remediate) — eğitmen canlı uygular, öğrenci yanında takip eder.
Böylece rehber hem öğrenci (HOL) hem eğitmen (tam demo prosedürü) için
baştan sona yeterlidir.

---

## Nasıl kullanılır (öğrenci akışı)

1. **[HOL erişim rehberini](00-hol-erisim.md)** oku, hesabını aç, bir lab
   başlatmayı öğren.
2. O günün dosyasını aç (`01-gun-1.md` …). Her gün şu akıştadır:
   **kavram (Türkçe) → HOL lab'ı başlat → Türkçe adım/companion → doğrulama.**
3. HOL lab'ını başlat (aşağıdaki linkten), içindeki İngilizce rehberi
   takip ederken **bu dosyadaki Türkçe açıklamayı yanında tut**.
4. Takıldığın yerde dosyanın sonundaki **"Sık sorunlar"** tablosuna bak.

---

## 5 günlük program

| Gün | ICM 8 konusu | HOL lab(ları) | Dosya |
|---|---|---|---|
| **1** | Giriş, sanallaştırma, ESXi, vCenter'a bakış | HOL-2706-01 | [01-gun-1.md](01-gun-1.md) |
| **2** | vCenter, sanal ağlar, depolama (datastore/vSAN) | HOL-2706-02 · HOL-2734-01 | [02-gun-2.md](02-gun-2.md) |
| **3** | VM yönetimi (template/klon/snapshot/vMotion) + depolama derinleşme | HOL-2734-01 · HOL-2706-02 | [03-gun-3.md](03-gun-3.md) |
| **4** | Kaynak yönetimi, izleme, performans | HOL-2704-03 · HOL-2704-04 | [04-gun-4.md](04-gun-4.md) |
| **5** | Kümeler (HA/DRS), yaşam döngüsü + işletme | HOL-2704-01 · HOL-2711-02/03/06 | [05-gun-5.md](05-gun-5.md) |
| **+** | İleri / bonus (ICM dışı): Kubernetes, Automation, Operations what's new | HOL-2704-07 · HOL-2711-01/21 | [06-bonus-ileri.md](06-bonus-ileri.md) |

> 🖨️ **Yazdırılabilir tek sayfa çizelge:** [`cizelge.html`](cizelge.html) —
> tarayıcıda aç → **Ctrl+P** → A4 → PDF olarak kaydet ve öğrencilere dağıt.

---

## Lab envanteri (12 HOL rehberi) ve ICM ilgisi

Katalog: **https://labs.hol.vmware.com** · her lab'a koduyla ara:
`…/HOL/catalog?search=<KOD>`

| Kod | Konu | ICM 8 | Hızlı link |
|---|---|---|---|
| **HOL-2706-01-VCF-L** | What's New: Compute (vSphere) | ✅ çekirdek | [aç](https://labs.hol.vmware.com/HOL/catalog/lab/27714) |
| **HOL-2706-02-VCF-L** | vSphere 9.1 Deep Dive / Compute | ✅ çekirdek | [aç](https://labs.hol.vmware.com/HOL/catalog/lab/27670) |
| **HOL-2734-01-VCF-L** | vSAN 9.1 – Getting Started & Advanced | ✅ çekirdek (depolama) | [aç](https://labs.hol.vmware.com/HOL/catalog/lab/27712) |
| **HOL-2704-03-VCF-L** | vSphere Performance Improvements | ◑ izleme | [aç](https://labs.hol.vmware.com/HOL/catalog/lab/27694) |
| **HOL-2704-04-VCF-L** | Performance Benchmarking & Monitoring (ESXTOP) | ◑ izleme | [ara](https://labs.hol.vmware.com/HOL/catalog?search=HOL-2704-04) |
| **HOL-2704-01-VCF-L** | VCF Operations – Fleet Management | ✕ bonus | [aç](https://labs.hol.vmware.com/HOL/catalog/lab/27687) |
| **HOL-2711-02-VCF-L** | Getting Started with VCF Operations | ✕ bonus | [ara](https://labs.hol.vmware.com/HOL/catalog?search=HOL-2711-02) |
| **HOL-2711-03-VCF-L** | Monitoring – VCF Health & Diagnostics | ✕ bonus | [ara](https://labs.hol.vmware.com/HOL/catalog?search=HOL-2711-03) |
| **HOL-2711-06-VCF-L** | Troubleshooting Workloads & Infrastructure | ✕ bonus | [ara](https://labs.hol.vmware.com/HOL/catalog?search=HOL-2711-06) |
| **HOL-2711-01-VCF-L** | What's New: Operations | ✕ ileri | [ara](https://labs.hol.vmware.com/HOL/catalog?search=HOL-2711-01) |
| **HOL-2711-21-VCF-L** | Getting Started with VCF Automation | ✕ ileri | [ara](https://labs.hol.vmware.com/HOL/catalog?search=HOL-2711-21) |
| **HOL-2704-07-VCF-L** | vSphere Kubernetes Service (Supervisor) | ✕ ileri | [aç](https://labs.hol.vmware.com/HOL/catalog/lab/27680) |

> **Not:** Lab kodları/ID'leri katalogda zamanla değişebilir. Link açılmazsa
> koduyla ara: `https://labs.hol.vmware.com/HOL/catalog?search=<KOD>`.

---

## İçindekiler
- [00 — HOL ortamına erişim ve kullanım](00-hol-erisim.md)
- [01 — Gün 1: Giriş ve vSphere'e bakış](01-gun-1.md)
- [02 — Gün 2: vCenter, ağ ve depolama](02-gun-2.md)
- [03 — Gün 3: VM yönetimi ve depolama derinleşme](03-gun-3.md)
- [04 — Gün 4: Kaynak yönetimi, izleme, performans](04-gun-4.md)
- [05 — Gün 5: Kümeler, yaşam döngüsü ve işletme](05-gun-5.md)
- [06 — Bonus / ileri lab'lar](06-bonus-ileri.md)

## Resmi kaynaklar
- VMware Hands-on Labs: https://labs.hol.vmware.com
- HOL Docs: https://docs.hol.vmware.com
- Resmi kurs Lab Guide'ı (**EDU-EN-VSICM8-LAB**) ve eğitmen lab ortamı —
  eğitmen tarafından sağlanır (bu depoda **yer almaz**).

## Marka ve telif notu
VMware, vSphere, vCenter, ESXi, vSAN, Cloud Foundation ve ilgili işaretler
Broadcom/VMware'e aittir. Bu depo **eğitim amaçlı özgün Türkçe çalışma
materyalidir**; VMware'in Lab Guide'ı, HOL PDF'leri veya tescilli içeriği
çoğaltılmaz. Resmi adımlar için HOL ortamındaki yerleşik rehber ve eğitmenin
sağladığı resmi PDF'ler kullanılır.
