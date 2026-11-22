# 00 — HOL Ortamına Erişim ve Kullanım

> VMware **Hands-on Labs (HOL)**, tarayıcıdan açılan, **tamamen kurulu** bir
> vSphere/VCF ortamıdır. Kendi bilgisayarına hiçbir şey kurmazsın — her şey
> bulutta çalışır ve lab bitince silinir. Ücretsizdir, sadece bir hesap
> gerekir.

---

## 1. Hesap aç (bir kez)

1. Tarayıcıda **https://labs.hol.vmware.com** adresine git.
2. Sağ üstten **Login / Sign Up** → ücretsiz bir **Broadcom (VMware) hesabı**
   oluştur (iş e-postanla önerilir).
3. E-postanı doğrula ve giriş yap.

> Sınıfça aynı anda açacaksınız; öğrenciler **eğitimden önce** hesabını
> açsın ki ilk gün vakit kaybı olmasın.

## 2. Lab bul ve başlat

1. Giriş yaptıktan sonra **Catalog** (Katalog) sayfasına gel.
2. Arama kutusuna lab **kodunu** yaz (ör. `HOL-2706-01`) ya da bu rehberdeki
   **hızlı linke** tıkla.
3. Lab kartında **Enroll** (kaydol) → sonra **Start / Launch** (başlat).
4. Ortam birkaç dakikada hazırlanır; **tarayıcı sekmesinde** açılır.

> Link açılmazsa (katalog güncellenmiş olabilir) koduyla ara:
> `https://labs.hol.vmware.com/HOL/catalog?search=<KOD>`

## 3. Lab ekranını tanı

Lab açıldığında ekran iki parçadır:

- **Sol/orta — Masaüstü (konsol):** İçinde Windows "Main Console" vardır;
  oradan vSphere Client (tarayıcı), PowerCLI, PuTTY gibi araçlara erişirsin.
- **Sağ — Lab Manual (rehber):** Adım adım İngilizce yönerge. **Modüllere**
  bölünmüştür (Module 1, Module 2 …). Bu rehberdeki Türkçe companion'ı
  **bunun yanında** kullan.

### İşine yarayacak düğmeler
| Düğme / işlev | Ne yapar |
|---|---|
| **Table of Contents / Modules** | Modüller arası geç; sadece ilgili modülü yapabilirsin |
| **Send Text** | Uzun komut/parolaları konsola **yapıştırır** (elle yazma) |
| **Fit to Window / Resolution** | Ekranı pencereye sığdır (görüntü taşıyorsa) |
| **Lab zamanlayıcı** | Üstte kalan süre; bitince **Extend** ile uzat |
| **End Lab** | Lab'ı bitir (ortam silinir — işin bitince) |

> **Kopyala-yapıştır:** Konsol içine doğrudan yapıştırma bazen çalışmaz;
> rehberdeki komutları **Send Text** ile gönder.

## 4. Süre ve kaydetme

- Her lab'ın bir **süre sınırı** vardır (genelde birkaç saat). Süre dolmadan
  **Extend** ile uzatabilirsin.
- **Ortam kalıcı değildir:** Lab'ı kapatınca/bittiğinde tüm değişiklikler
  **silinir**. Not alman gerekiyorsa ekran görüntüsü/kendi notuna al.
- Bir modülü yarıda bırakıp çıkarsan baştan başlaman gerekebilir; **modülü
  tek oturumda bitirmeye** çalış.

## 5. Modül mantığı (çok önemli)

Bir HOL lab'ı = birkaç **modül**. Her modülün başında seviyesi (Beginner /
Intermediate) ve süresi yazar. **Bütün lab'ı baştan sona yapmak zorunda
değilsin** — bu rehber her gün **hangi modülleri** yapacağını söyler.

## 6. İlk gün kontrol listesi (öğrenci)
- [ ] Broadcom/VMware hesabı açıldı, giriş yapıldı
- [ ] `HOL-2706-01` bulundu, **Enroll + Start** denendi, masaüstü geldi
- [ ] Sağdaki **Lab Manual** ve **Send Text** düğmesi görüldü
- [ ] vSphere Client açıldı (masaüstündeki tarayıcı kısayolundan)

Bu dördü çalışıyorsa hazırsın → **[Gün 1](01-gun-1.md)**.

## Sık sorunlar

| Belirti | Çözüm |
|---|---|
| Lab linki açılmıyor | Koduyla ara: `…/catalog?search=<KOD>`; katalog ID'si değişmiş olabilir |
| Konsola yazamıyorum / yapışmıyor | **Send Text** kullan; pencereye tıklayıp odakla |
| Ekran taşıyor / küçük | **Fit to Window** / çözünürlük ayarı |
| Süre doluyor | **Extend** ile uzat; modülü tek oturumda bitir |
| vSphere Client açılmıyor | Ortam tam hazır olmayabilir; 1-2 dk bekle, tarayıcı kısayolunu tekrar aç |
| "9.1 / VCF" görüyorum, kurs 8 | Normal — HOL güncel sürüm; kavramlar aynı (bkz. README sürüm notu) |
