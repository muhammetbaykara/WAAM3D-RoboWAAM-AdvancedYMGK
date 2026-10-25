# Kapsamlı SWOT Analizi ve Siber-Fiziksel Güvenlik Raporu: RoboWAAM® Advanced Robotik Tel Ark Eklemeli İmalat (WAAM) Sistemi

> **Yasal Uyarı:** Bu belge bir eğitim çıktısı ve teknik analiz çalışmasıdır; resmî denetim, uygunluk değerlendirmesi veya belgelendirme niteliği taşımaz ve CE/mevzuat uygunluğu garantisi vermez. Makineye ilişkin veriler kamuya açık üretici dokümantasyonuna dayanmakta olup, siber güvenlik ve emniyet kararları üreticinin resmi risk değerlendirmeleriyle doğrulanmalıdır.

---

## 1. Rapor Kapsamı ve Stratejik Arka Plan

Bu çalışma; WAAM3D tarafından geliştirilen büyük formatlı **RoboWAAM® Advanced** robotik tel ark eklemeli imalat (DED-Arc) sistemini, mekanik tasarım, fonksiyonel emniyet, endüstriyel siber güvenlik, pazar dinamikleri ve uluslararası yasal uyum eksenlerinde SWOT yöntemiyle ele alır. 

Sistem; 6+2 hareket ekseni, PTA güç kaynağı, otomatik inert atmosfer ($O_{2}$ kontrolü), duman yönetim sistemi ve `WAAMCtrl` işletim sistemi gibi gelişmiş özellikleriyle endüstriyel üretimde devrim niteliğinde avantajlar sunarken, aynı zamanda ağa bağlı dijital yapısı ve uzaktan erişim kabiliyetleri nedeniyle yeni nesil siber-fiziksel riskler barındırmaktadır.

---

## 2. Makine ve Üretici Profili

RoboWAAM, Cranfield Üniversitesi spin-off'u olan WAAM3D tarafından geliştirilen ve Singapur merkezli Accuron Technologies ortaklığıyla küresel ölçekte konumlandırılan endüstriyel bir eklemeli imalat hücresidir.

| Özellik / Alan | Teknik Detay | Kaynak |
| :--- | :--- | :--- |
| **Üretici & Konum** | WAAM3D Ltd, Milton Keynes (BK); Accuron Technologies (Çoğunluk hissedarı) | Basın, CB Insights |
| **Sistem Mimarisi** | RoboWAAM® Advanced (MKII); tek başına shopfloor (atölye) kurulumu; yalnız güç ve gaz bağlantısı gerektirir | Üretici Sayfası |
| **Yapı Hacmi & Yük** | 2 × 2 × 2 m nominal yapı hacmi; yüksek payload kapasitesi ve döner tabla entegrasyonu | Basın, Üretici |
| **Advanced Donanım** | 6+2 eksen robot, PTA/CMT güç kaynağı, global/lokal koruma, elektronik tel konumlama, duman tahliyesi, proses kamerası (60+ sensör) | Üretici Sayfası |
| **Yazılım Ekosistemi** | `WAAMPlanner` (takım yolu) → `WAAMSim` (çarpışma/simülasyon) → `WAAMKeys` (malzeme parametreleri) → `WAAMCtrl` (izleme, kontrol, dijital ikiz, sağlık-güvenlik yönetimi) | Üretici Sayfaları |
| **Saha Referansları** | 19. sistem satışı (Norveç - Industrial AM); ABD CCAM (Virginia) tesisi kurulumu; Malezya mutabakatı | 3printr, VoxelMatters |

---

## 3. Pazar Analizi

### 3.1 Pazar Hacmi ve Büyüme Dinamikleri
WAAM pazar büyüklüğü, analist firmalarının kapsam tanımlarına (yalnızca hücre/sistem, komple çözüm paketleri veya geniş ark kaynak ekipmanları) bağlı olarak farklılık gösterir:
* **The Business Research Company:** WAAM hücre pazarını 2025/2026 yıllarında ~0,60–0,68 milyar $ olarak değerlendirmekte; 2030 yılına kadar 1,09 milyar $'a ve yıllık %12,5–12,8 YBBH ile büyümesini öngörmektedir.
* **360iResearch (Ağustos 2026):** WAAM çözüm pazarını 2025'te 79,5 milyon $ olarak ölçmüş, 2032'de 150,4 milyon $'a (%9,52 YBBH) ulaşacağını öngörmüştür.
* **Değerlendirme:** RoboWAAM sınıfı entegre endüstriyel sistemler için 2030 yılı projeksiyonlarında 1 milyar $ eşiği ve çift haneli büyüme oranları sektörel standart kabul edilebilir.

### 3.2 Rekabet Ortamı
* **Lincoln Electric (ABD):** Güçlü kaynak ekipmanı ve tel tedarik zinciri kanalları; ordu ve havacılık için büyük ölçekli entegre çözümler.
* **Gefertec (Almanya):** Siemens Sinumerik kontrol altyapısına sahip CNC tabanlı hibrit sistemler (sertifikalı endüstriyel otomasyon avantajı).
* **MX3D (Hollanda) & Sciaky (EBAM):** Robotik WAAM ve elektron ışını tabanlı alternatif büyük formatlı DED çözümleri.

---

## 4. Uluslararası Standartlar ve Yasal Uyum Çerçevesi

RoboWAAM; robotik bir hücre, yüksek akımlı ark kaynağı, basınçlı gaz/inert atmosfer yönetimi ve bulut/ağ bağlantılı bir yazılım ekosistemi olması nedeniyle çok katmanlı standartlara tabidir:

| Düzenleme / Standart | Kapsam ve Odak | Mevcut Durum / Kanıt Eksikliği |
| :--- | :--- | :--- |
| **AB Makine Yönetmeliği (EU) 2023/1230** | 20 Ocak 2027 itibarıyla yürürlükte; Ek III gereğince kontrol sistemlerinin siber bütünlüğü ve manipülasyona karşı direnci. | Üretici bazlı uygunluk beyanı kamuya açık olarak doğrulanmamıştır. |
| **AB Siber Dayanıklılık Yasası (CRA) (EU) 2024/2847** | 11 Eylül 2026 itibarıyla zafiyet bildirim yükümlülükleri (24 saat) devreye girmiştir; dijital unsurlu ürünler için yaşam döngüsü güvenliği. | SBOM, VEX ve resmi PSIRT sayfaları kamu erişimine kapalıdır. |
| **ISO 10218-1 / -2 & ISO 12100** | Endüstriyel robot güvenliği, integrasyon kuralları ve makine risk değerlendirmesi. | Temel tasarım kriteri olmakla birlikte PLr/SIL değerleri dokümante edilmemiştir. |
| **ISO 13849-1 & IEC 62061** | Güvenlikle ilgili kontrol sistemlerinin güvenilirliği (Kategori / PL / SIL). | Emniyet fonksiyonlarının mimari bağımsızlığı doğrulanmaya muhtaçtır. |
| **IEC 62443 (3-2, 3-3, 4-1, 4-2)** | Endüstriyel otomasyon ve kontrol sistemleri siber güvenliği (Zone & Conduit, SL-T). | Resmi IEC 62443 sertifikasyonu veya değerlendirme raporu bulunmamaktadır. |
| **ISO/ASTM 52920 & AWS D20.1** | Metalik eklemeli imalat süreçleri ve tesis nitelik kazandırma ilkeleri. | `WAAMCtrl` denetim izleri temel oluşturur; standart eşlemesi belirsizdir. |

---

## 5. SWOT Matrisi (Özet)

| **S · GÜÇLÜ YÖNLER (Strengths)** | **W · ZAYIF YÖNLER (Weaknesses)** |
| :--- | :--- |
| • Uçtan uca entegre donanım-yazılım ekosistemi (`WAAMPlanner` $\rightarrow$ `WAAMCtrl`)<br>• 2×2×2 m yapı hacmi, 60+ sensör ile üstün süreç izleme<br>• Yerleşik duman tahliyesi ve otomatik $O_{2}$ inert atmosfer yönetimi<br>• Tam denetlenebilir kalite ve süreç kayıt altyapısı<br>• ~%80 oranında tescilli özgün tasarım bileşenleri<br>• Küresel referanslar (CCAM, Norveç) ve Accuron sermaye desteği | • İnternete açık ("dünyanın her yerinden") uzaktan erişim mimarisi belirsizliği ⚑<br>• Sağlık-güvenlik yönetiminin WAAMCtrl yazılımında konumlanması ve emniyet bağımsızlığının kanıtsızlığı ⚑<br>• Uzaktan güç kaynağı yönetimi ve CCTV entegrasyonunun yarattığı fiziksel risk yüzeyi ⚑<br>• SBOM, VEX, CVE geçmişi ve güvenlik şeffaflığının bulunmaması<br>• Tescilli yapı nedeniyle yama yönetiminde üreticiye bağımlılık |
| **O · FIRSATLAR (Opportunities)** | **T · TEHDİTLER (Threats)** |
| • Yıllık %10–13 büyüme gösteren küresel WAAM sistem pazarı<br>• CRA ve yeni Makine Yönetmeliği uyumu ile "Secure-by-Design" pazar farklılaşması<br>• ABD (CCAM) ve Asya-Pasifik (Malezya/Singapur) bölgesel genişleme hamleleri<br>• Kritik havacılık ve enerji yedek parça üretiminde tedarik zinciri egemenliği<br>• Yönetilen siber güvenlik, SBOM aboneliği ve dijital ikiz doğrulama katma değerli servisleri | • Robot denetleyici ve OT ağlarını hedef alan kritik CVE zafiyetleri (örn. CVSS 9.8 sınıfı) ⚑<br>• AB CRA 24 saatlik olay bildirim yükümlülükleri ve cezai yaptırım riski ⚑<br>• Siber müdahalenin ezilme, boğulma veya yangın gibi ölümcül fiziksel sonuçlar doğurması ($S=3$) ⚑<br>• Lincoln Electric ve Gefertec gibi güçlü alternatif rakip ekosistemler<br>• Nitelikli operatör açığı ve uzun sertifikasyon süreçleri |

> **Not:** ⚑ simgesi, şiddeti ölümcül ($S=3$) olan ve skor matrisinden bağımsız olarak en yüksek öncelikle ele alınması gereken siber-fiziksel güvenlik risklerini belirtir.

---

## 6. Ayrıntılı SWOT Analizi

### S · Güçlü Yönler (Strengths)
1. **Entegre Ekosistem Uyumu:** Takım yolundan robot koduna (`WAAMPlanner`), simülasyondan (`WAAMSim`) parametre yönetimine (`WAAMKeys`) ve gerçek zamanlı kontrole (`WAAMCtrl`) kadar kesintisiz veri akışı.
2. **Yüksek Teknik Kapasite:** Sınıfının en büyük yapı hacimlerinden biri (2×2×2 m), yüksek yük kapasitesi ve G-MAX süreciyle 15 kg/sa üzeri biriktirme hızı iddiası.
3. **Çevresel ve Fiziksel Koruma:** Otomatik inert gaz (argon) $O_{2}$ eşik koruması ve entegre duman filtrasyon sistemleri ile operatör sağlığına mimari düzeyde yaklaşım.

### W · Zayıf Yönler (Weaknesses)
1. **Uzaktan Erişim Belirsizliği ⚑:** `WAAMCtrl` sisteminin küresel ölçekte uzaktan erişilebilir olması, ancak kimlik doğrulama, tünelleme ve oturum kayıt mimarisinin yeterince şeffaf olmaması.
2. **Emniyet Bağımsızlığı Kanıtı Eksikliği ⚑:** Acil durdurma, kapı kilidi ve $O_{2}$ interlock gibi hayati emniyet fonksiyonlarının, ağa bağlı süreç yazılımından (`WAAMCtrl`) tamamen ayrı donanımsal emniyet röleleriyle çalışıp çalışmadığının belirsizliği.
3. **Zafiyet Şeffaflığı Yokluğu:** Kamuya açık bir SBOM, VEX dosyası veya PSIRT (Ürün Güvenliği Olay Müdahale Ekibi) bildirim portalının bulunmayışı.

### O · Fırsatlar (Opportunities)
1. **Regülasyon Odaklı Farklılaşma:** AB Siber Dayanıklılık Yasası (CRA) ve Makine Yönetmeliği geçiş sürecinde IEC 62443 uyumlu "Güvenli Tasarım" yaklaşımıyla pazar liderliği.
2. **Global Konumlanma:** ABD'de CCAM ve Asya-Pasifik'teki yeni Ar-Ge ve uygulama merkezi yatırımlarıyla bölgesel pazar payı artışı.

### T · Tehditler (Threats)
1. **Hedefli OT Saldırıları ⚑:** Endüstriyel robot denetleyicilerini hedef alan geçmiş zafiyet sınıfları (örn. Universal Robots / ABB RobotWare CVE örnekleri) benzeri tehditlerin RoboWAAM altyapısını etkileme potansiyeli.
2. **Mevzuat Uyumsuzluk Cezaları:** CRA kapsamında 11 Eylül 2026'da devreye giren bildirim zorunluluklarına uyulmaması durumunda yüksek cirosal cezai yaptırımlar.

---

## 7. Güvenlik Odaklı Derinleştirme (Labs 1–5 Sentezi)

### 7.1 Fonksiyonel Emniyet ve Siber Güvenlik Kesişimi
RoboWAAM analizinde karşılaşılan en kritik bulgu, normal süreç kontrolü ile insan güvenliğinin kesiştiği noktadır. 
* **Normal PLC vs. Safety PLC:** `WAAMCtrl` tarafından yönetilen süreç kontrol elektroniği, ark parametrelerini, tel beslemeyi ve gaz akışını yönetirken yüksek esneklik sunar; ancak arıza durumunda güvenli duruma geçişi garanti etmez. Emniyet kumandası ise çift kanal, çapraz karşılaştırma ve kendi kendine test mekanizmalarıyla yalnızca insanı korumak zorundadır.
* **Dijital Bağımlılıklar (D1–D7):** `WAAMCtrl` donanımı, uzaktan güç kaynağı yönetimi, $O_{2}$ sensör verilerinin ağ üzerinden aktarılması ve entegre CCTV kameraları doğrudan emniyet döngülerini beslemektedir. Kamera görüntüsüne dayanarak uzaktan "muhafazada kimse yok" varsayımı yapmak ölümcül sonuçlar doğurabilir.

### 7.2 IEC 62443 Zone & Conduit Mimarisi
Sistem bileşenleri risk profillerine göre altı bölgeye (Zone) ayrılmıştır:
* **Z1 (Emniyet):** Kapı kilidi, E-stop, $O_{2}$ interlock ve STO çıkışları (SL-T: 3). Dışarıya yalnızca durum bilgisi aktarır, asla dışarıdan komut almaz.
* **Z2 (Makine Kontrol Hücresi):** Süreç PLC, robot sürücüleri ve PTA/CMT güç kaynağı.
* **Z3 (Gözetim):** `WAAMCtrl` sunucusu ve Control Centre iş istasyonu.
* **Z4 (Mühendislik):** `WAAMPlanner` / `WAAMSim` istasyonları ve program aktarım ortamı.
* **Z5 (DMZ / Uzak Erişim):** Güvenli geçişin sağlandığı jump server ve VPN broker katmanı.
* **Z6 (Dış Ağ / İnternet):** Güvenilmez dış dünya.
* *Kritik Mimari Karar:* Doğrudan internet erişimi kaldırılmış; uzak erişim Z5 DMZ bölgesinde sonlandırılmış, MFA ve kişisel rol tabanlı hesaplar zorunlu kılınmıştır.

### 7.3 Tehdit Modellemesi ve Kritik Risk Senaryoları ($S=3$)
* **S1 - Uzaktan Hareket Enjeksiyonu (Skor: 12 - Yüksek / $S=3$):** İnternet üzerinden ele geçirilen WAAMCtrl oturumu ile, operatör muhafaza içindeyken robotun hareket ettirilmesi veya ark başlatılması. Sonuç: Ölümcül ezilme/çarpma.
* **S2 - $O_{2}$ Eşiği / Okumasının Sahtelenmesi (Skor: 6 - Orta / $S=3$):** Zararlı USB veya yetkisiz erişimle $O_{2}$ alarm eşiğinin maskelenmesi. Inert argon atmosferindeki muhafazanın kapı kilidinin açılmasıyla operatörün boğulması.
* **S3 - Süreç Parametresi Manipülasyonu (Skor: 12 - Yüksek):** Akım, tel hızı ve gaz akışı sınırlarının aşılarak yangın, sıcak parça sıçraması ve yapısal kusur üretilmesi.

### 7.4 Güvenli Uzak Erişim Gereksinimleri (R-01 — R-08)
Lab 4 kapsamında tanımlanan doğrulanabilir gereksinimler şunlardır:
* **R-01:** Emniyet fonksiyonları, `WAAMCtrl` ve ağ kullanılabilirliğinden tamamen bağımsız çalışmalıdır.
* **R-02:** Hiçbir ağ yolu emniyet fonksiyonunu bypass edemez, susturamaz veya parametre değiştiremez.
* **R-03:** Tehlikeli hareket ve ark başlatma, muhafaza kapalı/kilitli olmaksızın uzaktan kabul edilemez.
* **R-05:** "Muhafazada kimse yok" bilgisi CCTV kameralarına değil, yerel emniyet sensörlerine dayanmalıdır.

### 7.5 SBOM, CVE ve Yama Yönetimi Karar Akışı
* **Etkilenme Değerlendirmesi:** Kontrol elektroniği firmware kütüphanesinde (örn. Sürüm 2.4, CVSS 9.8) kritik bir zafiyet tespiti durumunda, SBOM ve üretici VEX bildirimi talep edilir.
* **Üretim Durdurma Stratejisi:** WAAM süreçleri saatler/günler sürdüğü için toptan acil durdurma malzemenin hurdaya çıkmasına yol açabilir. İlk 0–4 saat içinde uzaktan erişim kapatılarak (varsayılan kapalı) ulaşılabilirlik sıfırlanır; mevcut build güvenli kesme noktasına kadar tamamlanır.
* **Test ve Validasyon:** Yama asla doğrudan canlı sistemde uygulanmaz. Sırasıyla; üretici onaylı imaj, yedekleme noktası, `WAAMSim` dijital ikiz ortamı, yüksüz hava koşusu (dry-run) ve kupon numune build testlerinden geçirilir. Emniyet yazılımı imzası değiştiği takdirde ISO 13849-1 uyarınca tam yeniden validasyon zorunludur.

---
*Bu rapor, endüstriyel siber-fiziksel sistem güvenliği prensipleri gözetilerek akademik ve teknik değerlendirme amacıyla hazırlanmıştır.*
