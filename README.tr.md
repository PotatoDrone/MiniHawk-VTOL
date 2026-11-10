<!-- MiniHawk-VTOL README.tr.md - Metin görüntüleyicinizde/düzenleyicinizde sözcük kaydırmayı etkinleştirin -->
<img src="MiniHawkIso.png" width="400" />

# MiniHawk-VTOL <a name="head-brief"></a>

> Bu dosya, [İngilizce README’nin](README.md) Türkçe çevirisidir. Özgün metindeki tarihler, sürüm notları ve teknik değerler korunmuştur.

MiniHawk VTOL, dikey kalkış ve iniş yapabilen, 3B baskıyla üretilmiş bir trikopter/sabit kanat hibrit hava aracıdır. Önceki tasarım olan [OrangeHawk VTOL](https://diydrones.com/profiles/blogs/the-orange-hawk-tricopter-flying-wing-vtol-uav) gibi MiniHawk da R/C, FPV ve İHA deneyleri için tasarlanmıştır. Mekanik tasarım dosyaları, montaj talimatları ve yapılandırma ayarları bu depoda sunulmaktadır.  

> **⚠️OKUYUN - PROJENİN KARARLILIĞI VE YENİ SÜRÜM⚠️ - 18 MART 2022: Büyük olasılıkla bu projeye [How NOT to Flight Test a VTOL UAV](https://www.youtube.com/watch?v=FYqH4kHllrU) veya başka bir YouTube videosundaki bağlantıdan ulaştınız. Bu projeyi yapmayı denemek istiyorsanız, başlayın! Bu yazı yazılırken bu depodaki tüm STL dosyaları, bu metnin solundaki _Version 2.0 - Hotfix and 2.1 Preview_ zip dosyası ve Hackaday.io sayfasına en son yüklenen dosyalar "güvenlidir". Önceden bazı tasarım kusurları (eski motor yatırma gondolu tasarımı) vardı; ancak bu sorunlar yalnızca 23 Şubat düzeltmesinden önceki Sürüm 2.0 STL dosyalarında bulunuyor. Yineleyeyim: buradaki _master_ dalında bulunan her şey montaj için güvenli olmalı ve 2022 yılının büyük bölümünde değiştirilmeyecektir.**
> 
> **Bununla birlikte, yakında™ yeni bir sürüm, Sürüm 2.1 geliyor. Ancak şu aşamada bu sonraki sürüm mevcut STL dosyalarının hiçbirini değiştirmeyecek. Dolayısıyla STL dosyalarını rahatça kullanabilirsiniz; her şey çalışıyor ve çok iyi uçuyor. Hava aracı tasarımına ilişkin hiçbir değişiklik bu yılın sonlarına veya gelecek yılın başlarına kadar yayımlanmayacak. V2.1 ile bazı ek STL dosyaları/özellikler eklenecek; bunun dışında yapılanlar sunumu iyileştirmek veya belgeleri yeniden yazmak olacak. Birkaç aydır Sürüm 2.1 ön sürümünde takılı kaldım; bu yüzden bu README’nin montaj talimatları gibi bazı bölümleri yeniden yazılıyor, Parça Ağacı Şeması gibi eklemeler yapılıyor. Şu anda projeyi yapmak isteyenlere önerilerim şunlar:**
> 
> - Güncellenmiş montaj talimatları için [Development Dalındaki Montaj Talimatlarına](https://github.com/StephenCarlson/MiniHawk-VTOL/tree/development#build-sequence-) bakın.
> - Yeni montaj talimatı görsellerinin tümü için [Development Dalındaki Belgeler Klasörünü](https://github.com/StephenCarlson/MiniHawk-VTOL/tree/development/doc-Documentation) inceleyin; bunların çoğu güncellenmiş montaj talimatlarına henüz eklenmedi veya orada kullanılmıyor.
> - Animasyonlu montaj adımlarını görmek için [MiniHawk-VTOL Assembly in 100 Seconds](https://www.youtube.com/watch?v=nICNlJhoEvw) videosunu izleyin.
> - [Aşağıdaki Eski Montaj Talimatlarıyla](https://github.com/StephenCarlson/MiniHawk-VTOL#build-sequence-) karşılaştırın. Eski Sürüm 1.0’a ait görseller ve adımlar göreceksiniz; aradan geçen 1.5 yılda kaldırılmış veya yeniden tasarlanmış özellikleri dikkate almayın.
> 
> **Dağınıklık için kusura bakmayın, umarım yardımcı olur. Zaman buldukça bu projeyi tanıtmaktan ve geliştirmekten keyif alıyorum. Sorularınız olursa bana bildirin; montajın keyfini çıkarın! -Steve**


**Kilometre Taşları**
| Tarih | Olay |
| -------------- | ------------------------------- |
| 15 Eki 2020 | İlk Yayımlanış (v1.0) |
| 2 Eki 2021 | Sürüm 2 (v2.0, MH7_ öneki) |
| ön sürüm | Sürüm 2.1 |
| 2023 1. çeyrek | Sürüm 2.2 |

Hackaday proje sayfası: [HACKADAY.IO Sayfası](https://hackaday.io/project/175286-minihawk-vtol)  

MiniHawk tasarım ayrıntıları ve özellikleri burada tartışılıyor: [RCGroups VTOL Forum Konusu](https://www.rcgroups.com/forums/showthread.php?3986653-MiniHawk-VTOL-A-3D-Printed-Tricopter-Tilt-Rotor-Fixed-Wing-Plank)  

Topluluk üyelerinin öne çıkan MiniHawk-VTOL yapımları: [RCGroups 3B Baskı Forum Konusu](https://www.rcgroups.com/forums/showthread.php?3750791-KatanaGuy-s-MiniHawk-VTOL)

Montaja eşlik eden video serisi: [YouTube Oynatma Listesi](https://www.youtube.com/playlist?list=PLEMjH2uELUcYI_DS1zthgjE4Su79LeA_G)  

Betaflight VTOL aygıt yazılımı derlemesi: [vtol-motor-mix](https://github.com/StephenCarlson/betaflight/tree/vtol-motor-mix)  

# İçindekiler
1. [Giriş](#head-brief)  
  1.1 [Açıklama](#head-description)  
  1.2 [Bu Depo Nasıl Kullanılır](#head-usage)  
  1.3 [Notlar / SSS](#head-faqs)  
  1.4 [Teknik Özellikler](#head-metrics)  
2. [Montaj Bilgileri](#build-brief)  
  2.1 [Önerilen Aletler](#build-tools)  
  2.2 [Bileşenler ve Elektronik](#build-components)  
  2.3 [Gövde Parça Listesi](#build-airframeparts)  
3. [Montaj Adımları](#buildseq-brief)  
  3.1 [Bölüm 1 - Gövde Yapıları](#buildseq-part1)  
  3.2 [Bölüm 2 - Bağlantı Mekanizmaları ve Servolar](#buildseq-part2)  
  3.3 [Bölüm 3 - Elektronik ve Son İşlemler](#buildseq-part3)  
4. [Uçuş Testleri](#flight-brief)  
5. [3B Baskı Kılavuzu](#3dprinting-brief)  
6. [ArduPlane](#arduplane-brief)  
  6.1 [R/C Kumanda Yapılandırması](#arduplane-controlsconfig)  
  6.2 [Uçuş Kontrolcüsü Bağlantıları](#arduplane-connections)  
  6.3 [Parametreler](#arduplane-parameters)  
  6.4 [Notlar](#arduplane-remarks)  
8. [Lisans](#license-brief)  

## Açıklama <a name="head-description"></a>
MiniHawk, 3B baskıyla üretilen bir VTOL hava aracıdır. Basılabilirlik gözetilerek tasarlanmıştır ve topluluğa deneyler ve geliştirmeler için ortak, erişilebilir bir VTOL test platformu sunmayı amaçlar. Araç, itki için üç (3) fırçasız DC motor kullanır. Öndeki iki motor ileri uçuş ve sapma (yaw) kontrolü için yatırılır; arkadaki motor sabittir ve yalnızca havada asılı kalmak için kullanılır. Öndeki motorları yatırmak ve kanattaki elevon kumanda yüzeylerini kontrol etmek için dört (4) servo kullanılır. Gövde, aviyonikleri ve bataryayı içeren bir merkez gövdeye ve gondollara ve servolara uzanan iç kanallara sahip, "plank" tipi bir kanattan oluşur. İki dikey stabilize yüzeyi hafif yönelme kararlılığı sağlar.  

## Bu Depo Nasıl Kullanılır <a name="head-usage"></a>
Bu proje, geleneksel olarak bir yazılım deposu sitesi olan GitHub’da barındırılıyor. Bununla birlikte bu yapı, MiniHawk-VTOL gibi bir donanım projesi için de uygundur; bazı özellikleri özellikle işe yarar:
- Her parça dosyasının geçmişine erişilebilir; eski bir sürüme ihtiyacınız varsa, depoyu "klonladıysanız" çevrimdışıyken bile erişebilirsiniz. (Dikkat: depoyu klonlamak yüzlerce MB indirmek demektir.)
- [Sürümler ve Yayımlar](https://github.com/StephenCarlson/MiniHawk-VTOL/releases), bir yazılım projesinde olduğu gibi yayımlanır. Buna kilometre taşlarının belirlenmesi ve sonraki sürümlerin planlanması da dahildir; böylece topluluk sırada ne olduğunu öğrenir. Yayımlar, tasarımın kararlı ve geniş dağıtıma uygun olduğu bir andaki proje durumunu temsil eden, zip arşivine yerleştirilmiş temel dosyaların derlenmiş kümesidir.
- [Issues](https://github.com/StephenCarlson/MiniHawk-VTOL/issues) sekmesi, topluluğun tasarımı iyileştirmek için geri bildirim veya katkı sunarak tasarımın gelişimine katılmasını sağlar.
- [Discussions](https://github.com/StephenCarlson/MiniHawk-VTOL/discussions) sekmesi, proje hakkında iletişim kurulabilecek bir başka yerdir.

Barındırma ortamını açıklamış olsam da GitHub hesabı açmanız veya projeye katılmanız gerekmez; büyük olasılıkla yalnızca STL dosyalarını indirip uçağı yapmak istiyorsunuz. Yapmanız gerekenler şunlar:
- Bu web sayfasının sağ üst bölümündeki [En Son Sürüm](https://github.com/StephenCarlson/MiniHawk-VTOL/releases/latest) bağlantısına tıklayın. Bu sizi tasarımın en son kararlı sürümüne götürür.
- Sürümdeki yenilikleri veya dikkate değer noktaları anlamak için açıklamayı okuyun. Ardından Assets bölümünde `MiniHawk-VTOL-x.x.x.zip` adlı .zip dosyasını bulun; buradaki ‘x’ler sürüm numaralarıdır. `Source Code` indirmelerini atlayın: bunlar GitHub tarafından otomatik oluşturulur ve projenin tüm içeriğini kapsar; gerçekten tamamını istemiyorsanız muhtemelen aradığınız bunlar değildir.
- Arşivi açıp dosyaları inceleyin. Okuduğunuz bu README’nin bir kopyası README.md dosyasında bulunur ve herhangi bir metin düzenleyiciyle açılabilmelidir.
- Aşağıdaki [Montaj Adımlarını](#buildseq-brief) izleyin. Bu sayfayı yazdırmak veya PDF olarak kaydetmek mümkün olmalıdır. Kodla aranız iyiyse, metnin tamamının Markdown ile yazıldığını ve tercih ettiğiniz metin düzenleyicide veya Markdown işleyicisinde görüntülenebilmesi gerektiğini de belirtelim.

## Notlar / SSS <a name="head-faqs"></a>
- Gövde tamamen 3B baskıyla üretildiğinden, tamamlanmış araç orta derecede ağırdır; bu özellikle havada asılı kalma uçuşunda dezavantajdır. Bu nedenle ilave ağırlık eklerken ölçülü ve dikkatli olun. Standart PLA ve 0.4mm nozulla önerilen baskı ayarlarında yalnızca gövde 460g’ın biraz üzerindedir; tamamlanmış aracın toplam uçuş ağırlığı ise 1000g ile 1200g arasındadır.  
- Bu projede kullanılan parçalar, yarış dronu ve R/C uçak pazarlarında yaygın olarak bulunur. 2207, 2306 veya benzeri standart motorlar kullanılabilir. Gondol tasarımı, motor çanının çapını en fazla 29mm ile sınırlar; ancak bu, daha katı gereksinimleri olan önceki tasarım sürümlerine göre daha esnektir. Küresel mafsallı bağlantı muhtemelen kullanılan en özel parçadır; Dubro #181, Dubro #190 ve hatta Dubro #367 uygun seçeneklerdir.
- Aracın aerodinamiği ve kararlılığı hâlâ analiz edilmektedir ve değiştirilebilir. Aerodinamik analiz için kullanılan CFD konumları/senaryoları bağımsız inceleme için dahil edilmiştir.  
- Bu tasarımın Sürüm 2’sinden itibaren proje dosyaları "MH7" önekini taşır; çünkü bu, MiniHawk VTOL tasarımının 7. iç revizyonudur. Depoda bazı eski "MH5" parçaları kalmış olabilir; bunlar eski sürümlerdendir. Ayrıca "MH#" öneki rastlantısaldır ve bu araçta MH45’i kullanılan MH kanat profili serisiyle karıştırılmamalıdır. Genel olarak bu tasarımın ve yayımlanacak revizyonlarının doğru adı "MiniHawk-VTOL"dur.
- Bu araç Autodesk Inventor Professional 2019 ile tasarlandı. Oluşturulmuş STL dosyaları açık erişimle sunulsa da bu yazı yazılırken araca ait katı model ve montaj kaynak dosyaları paylaşılmamaktadır; bir kopya edinmek veya geliştirmeyi sürdürmek için benimle iletişime geçin. Küçük bir kolaylık olarak, kapak gibi bazı parçaların STEP/STP sürümleri topluluğun türev tasarımları için dahil edilmiştir.
- Her parçanın bazı çeşitleri vardır; örneğin burnun NACA havalandırma kanallı ve kanalsız sürümleri bulunur. Kanat ucu yüzeyi (winglet), "normal" veya GPS ya da başka cihazlar için oyuklu olarak sunulur. Kapağın, Foxeer -Nano kamera biçimini (15mm genişlik) destekleyen ve AKK Infinite DVR gibi bir video vericisi için 30.5mm montaj ızgarası olan bir FPV çeşidi vardır. Tüm parça seçenekleri ve çeşitleri aşağıdaki [Parça Ağacı Şemasında](#build-airframeparts) ayrıntılı olarak verilmiştir.

## Teknik Özellikler <a name="head-metrics"></a>
| Açıklama | Değer |
| -------------------------- | --------------------------- |
| Kanat açıklığı | 800mm |
| Kanat alanı | 15.6dm^2 |
| Açıklık oranı | 4.1 |
| Kanat profili (kök ve uç) | [MH45][1] |
| Uzunluk | 520mm |
| Rotor yerleşimi | 315mm çaplı çember |
| Lityum polimer batarya | 4s, 1300-1500mAh (~160g) |
| Motorlar (ön) | 2207 veya 2306 2300-2600kV |
| Motor (arka) | 2207 veya 2306 ~2000kV |
| Servolar | HS-65HB/MG veya eşdeğeri |
| Uçuş kontrolcüsü (boyut) | 30.50mm ile 16.0mm arası montaj ızgarası |
| Pervaneler (ön) | 5050 ile ~5249 arası |
| Pervane (arka) | 6030 ile ~5249 arası |
| Toplam uçuş ağırlığı | PLA ile 1000g ile ~1200g arası |

[1]: <https://www.mh-aerotools.de/airfoils/mh45koo.htm> "Martin Hepperle’nin MH45 Kanat Profili"

# MiniHawk Montaj Parça Listesi ve Aletler <a name="build-brief"></a>
## Önerilen Aletler ve Ekipman <a name="build-tools"></a>
 - Baskı hacmi 23.1x210.7x150mm’den büyük bir FDM/FFF 3B yazıcı (330mm veya daha fazla baskı yüksekliği, burun ve kanatların bölünmeden tek parça basılmasına olanak tanır.)
 - Elektronik işler için lehim istasyonu, ilgili aletler ve malzemeler
 - El aletleri: pense, yan keski, zımpara, maket bıçağı/neşter, el matkabı vb.
 - Yapıştırıcılar ve sarf malzemeleri: siyanoakrilat yapıştırıcı, sıcak silikon tabancası, bant

## Bileşenler ve Elektronik <a name="build-components"></a>
| Adet | Parça açıklaması | Notlar |
| ----- | ------------------------------------------------------ | ---------------------------------------------------- |
| 1 | Uçuş kontrolcüsü (3 motor, 4 servo çıkışı) | mRo PixRacer Pro, Matek F405-WING veya F765-WING |
| - | Pitot probu, GPS, telemetri radyoları, FPV kamera+VTx vb. | İlave temel aviyonikler |
| 1 | Uçuş kontrolcüsüne entegre değilse servo beslemesi için UBEC | Castle Creations 10 Amp Ayarlanabilir BEC |
| 1 | R/C alıcı, 8+ kanal, SBUS veya PPM çıkışı |  |
| 3 | ESC (4s, 40A veya üzeri) | EMAX Formula Series 32Bit 45A ESC |
| 2 | 2207 veya 2306 ~2500KV BLDC motor (dış çap < 29mm) | T-Motor VELOX V2 2207 2550Kv (Not 1) |
| 1 | 2207 veya 2306 ~2000KV BLDC motor | T-Motor VELOX V2 2306 1950Kv (Not 2) |
| 1 | 4s1300 lityum polimer batarya (60C veya üzeri) | RDQ 14.8V 4S 1300mAh 100C |
| 1 | Kablolu XT60 konektör veya eşdeğeri |  |
| 2 | HS-65HB servo (veya eşdeğeri) | Elevon servoları, bkz. (Not 3). |
| 2 | HS-5065MG servo (veya eşdeğeri) | Motor yatırma servoları, bkz. (Not 4). |
| 1 | Karbon fiber ana kiriş, uzunluk<640mm, dış çap<=6.5mm | Kanatları güçlendirmek için; yuvarlak veya kare |
| 6 | (isteğe bağlı) Du-Bro SKU#118 küçük naylon menteşe | Elevon takviyesi, bkz. (Not 5). |
| - | M2 veya M3 montaj elemanları (somunlar, cıvatalar, yükselticiler) | Uçuş kontrolcüsü ve tablaların montajı için. |
| 4 | 6 inç servo uzatma kablosu | (Not 6) |
| 1 | Erkek-erkek servo uzatma kablosu | Uçuş kontrolcüsü ile alıcı arasındaki PPM/SBUS bağlantısı. |
| 4 | 2-56 bağlantı çatalı (clevis) (Not 7) | Dört (4) servo kolu bağlantısı. |
| 2 | 2-56 dişli bağlantı çubuğu, uzunluk>=52mm | Elevon itme çubukları; dişli uçtan 45mm mesafede L büküm. |
| 2 | (isteğe bağlı) Du-Bro SKU#855 E/Z Links 0.72 (2-56) klips | L bükümleri sabitlemek için; yerine Z büküm yapılabilir. |
| 2 | 1/16 inç 2-56 küresel mafsal ve kuplör çifti | Dubro #181 veya Dubro #190, bkz. (Not 8). |
| 2 | 2-56 tam dişli çubuk, uzunluk=70mm | Uç1=(2-56 bağlantı çatalı), Uç2=(2-56 küresel mafsal kuplörü) |
| 2 | 2-56 düz çubuk, uzunluk=40mm | (Not 9) |
| 4 | (isteğe bağlı) 3mm cıvata veya mil, uzunluk=44mm | Yatırma kollarında bilyalı rulman kullanmak isterseniz. |
| 4 | (isteğe bağlı) 3x6x2.5mm bilyalı rulman | Yaygın adı MR63ZZ; yatırma kolu destekleri için. |
| 2 | (isteğe bağlı) WS2812 5050 SMD (veya eşdeğer adreslenebilir LED) | Emaye tel ile lehimlenir, kanat uçlarına yerleştirilir. |
| - | M4 veya M5 pervane somunları | Gerekirse standart pervane somunlarının yerine kullanılır. |
| 1 | 50xx pervane, saat yönünde dönüş | Sol/iskele tarafı pervanesi, 5 inç |
| 1 | 50xx pervane, saat yönünün tersine dönüş | Sağ/sancak tarafı pervanesi, 5 inç |
| 1 | 50xx veya 60xx pervane, saat yönünün tersine dönüş | Kuyruk pervanesi, Dalprop Foldable F6 6048 üç palalı |
| 1 | Cırt cırtlı batarya kayışı |  |
| 1 | (isteğe bağlı) Batarya gerilim izleyicisi / sesli alarm | Uçuş kontrolcüsünde bulunmuyorsa kullanılmak üzere. |

> Not 1: Ön motorların dış çapı en fazla 29mm olmalı; 5 inç pervaneyle (tam gazda) 500g ile 800g arasında statik itki ve (yarım gazda) ~20m/s hatve hızı üretebilmelidir.  
> Not 2: Kuyruk motorunun dış çapı 30mm veya daha fazla olabilir; en fazla 6 inç pervaneyle (tam gazda) 700g ile 1000g arasında statik itki üretebilmelidir.  
> Not 3: Servo yuvaları en fazla 26mm genişlik, montaj kulaklarının altından servo tabanına 17.5mm, çıkış milinin üstünden servo tabanına 32mm ve 12mm kalınlık için tasarlanmıştır. Çoğu "Sub-Micro" servoya uymalıdır.  
> Not 4: Yuva ölçüleri yukarıdakiyle aynıdır; ancak bu servolar çok ağır zorlanacakları için oldukça sağlam olmalıdır. Aksi hâlde metal dişli olmayan servolarınızın dişlilerini sık sık sıyırmayı göze alın.  
> Not 5: Kullanılmayabilir; ancak elevonlardaki 3B baskı esnek menteşe sonunda bozulacaktır; uygun biçimde onarın. Dubro #118 pakette 6 adet, Dubro #119 ise pakette 15 adettir.  
> Not 6: Alternatif olarak servo kablolarını kesip, biraz pay bırakarak uçuş kontrolcüsüne ulaşacak uzunlukta ara uzatma kabloları lehimleyin.  
> Not 7: Çatallar ve çubuklar set olarak alınabilir; örneğin Du-Bro #185, çatalları takılı 5 çubuktan oluşan bir settir.  
> Not 8: Küresel mafsal saplamasının diş ölçüsü 1/16 inç / 62.5mil / 1.59mm olmalıdır. Bu parçanın daha yaygın bir çeşidinde küresel başlığın saplaması 2-56 (86mil) diş ölçüsündedir; bu biraz büyük olsa da gondol motor yatırma yatağına uyarlanabilmelidir. Yalnızca metrik bağlantı elemanları sipariş edebiliyorsanız 2mm diş ölçüsü uygun olmalıdır. Burada kastedilen, küresel mafsal saplamasının diş ölçüsüdür; bu saplama, dişli bir çubuğu tutan küresel mafsal yuvasına/kuplörüne bağlanır ve çubuk da servo koluna uzanır. Servo kolu ile küresel mafsal yuvası/kuplörü arasındaki bu bağlantı çubuğu herhangi bir ölçüde olabilir; ancak burada 2-56 olduğu varsayılmıştır.
> Not 9: Çap=[1.83mm ile 1.87mm arası]; artan 2-56 servo itme çubuğu parçalarından yapılır. Dişsiz düz çubuk kullanın; gondola sıkı geçme yapmak için yalnızca bir ucunu hafifçe pürüzlendirin/tırtıllayın.  

## Gövde Parçaları <a name="build-airframeparts"></a>

```
MiniHawk-VTOL Sürüm 2.1 Hava Aracı
|-- Gövde  
|   |-- Kuyruk Takımı/Kuyruk
|   |   |-- Baskı Seçeneği 1: Tek Parça - Bölünmemiştir; ancak katmanlar en yüksek dayanım için hizalanmamıştır
|   |   |   |-- MH7_Empennage-Full.stl
|   |   |
|   |   |-- Baskı Seçeneği 2: Dayanım için hizalanmış baskı katmanlarıyla iki parçaya bölünmüş
|   |       |-- Baskı Seçeneği 2a: Modele Dahil Baskı Destekleri
|   |       |   |-- MH7_Empennage-PrintSupports.stl
|   |       |
|   |       |-- Baskı Seçeneği 2b: Modele Dahil Baskı Destekleri Yok, yalın parça
|   |           |-- MH7_Empennage.stl
|   |
|   |-- Burun
|   |   |-- Baskı Seçeneği 1: Tam Burun - Bölünmemiş
|   |   |   |-- MH7_Nose.stl
|   |   |
|   |   |-- Baskı Seçeneği 2: İki Parçalı Burun
|   |       |-- MH7_Nose_A.stl
|   |       |-- MH7_Nose_B.stl
|   |
|   |-- Aviyonik (Uçuş Kontrolcüsü) Tablası
|   |   |-- Parça Çeşidi: Katı Tabla, Titreşim Sönümlemesiz
|   |   |   |-- MH7_AvionicsTray.stl
|   |   |
|   |   |-- Parça Çeşidi: Yaprak Yaylı Esnek Mekanizmalı Titreşim Sönümleyen Sürüm
|   |       |-- MH7_AvionicsTray2.stl
|   |
|   |-- Batarya Tablası
|       |-- MH7_BatteryTray.stl
|
|-- Kapak
|   |-- Parça Çeşidi: 16mm Boyutlu FPV Kamera ve VTx Desteği
|   |   |-- Baskı Seçeneği 1: Uzun Eksen Boyunca Simetrik Yarım (YAPILACAK: -Full hâline geri döndürülmeli)
|   |   |   |-- MH7_Hatch-FPV-16mm.stl
|   |   |
|   |   |-- Baskı Seçeneği 2: Daha düzgün baskı için iki parçaya bölünmüş
|   |       |-- MH7_Hatch-FPV-16mm_a.stl
|   |       |-- MH7_Hatch-FPV-16mm_b.stl
|   |
|   |-- Parça Çeşidi: NACA Kanallı Havalandırma
|   |   |-- Baskı Seçeneği 1: Tamamı; kendiniz bölün
|   |   |   |-- MH7_Hatch-Vented.stl
|   |   |
|   |   |-- Baskı Seçeneği 2: Daha düzgün baskı için iki parçaya bölünmüş
|   |       |-- MH7_Hatch-Vented_a.stl
|   |       |-- MH7_Hatch-Vented_b.stl
|   |
|   |-- Kilitleme Mandalı Mekanizması
|       |-- MH7_Hatch_LockingLatch.stl
|       |-- 1.85mm Çelik Pim, Uzunluk=30mm
|
|-- Sol Kanat  
|   |-- Parça Çeşidi: Yalın Kanat
|   |   |-- Baskı Seçeneği 1: Kanadın Tamamı
|   |   |   |-- MH7_WingLeft.stl
|   |   |
|   |   |-- Baskı Seçeneği 2: Daha küçük yazıcılar için iki parçaya bölünmüş
|   |       |-- MH7_WingLeft_A.stl
|   |       |-- MH7_WingLeft_B.stl
|   |
|   |-- Parça Çeşidi: Güneş Panelli Kanat
|   |   |-- Baskı Seçeneği 1: Kanadın Tamamı
|   |   |   |-- MH7_WingLeft-Solar.stl
|   |   |
|   |   |-- Baskı Seçeneği 2: Daha küçük yazıcılar için iki parçaya bölünmüş
|   |       |-- MH7_WingLeft_A.stl
|   |       |-- MH7_WingLeft_B.stl
|   |
|   |-- Elevon Kumanda Yekesi
|       |-- MH7_ControlHorn.stl
|
|-- Sol Dikey Stabilize  
|   |-- MH7_FinLeft_Lower.stl  
|   |-- MH7_FinLeft_Upper.stl  
|
|-- Sol Gondol
|   |-- Parça Çeşidi: Bilyalı Rulmanlı Sürüm
|   |   |-- MH7_Nacelle_A-Bearing.stl
|   |   |-- MH7_Nacelle_B-Bearing.stl
|   |
|   |-- Parça Çeşidi: Bilyalı Rulmansız Sürüm
|   |   |-- MH7_Nacelle_A-NoBearing.stl
|   |   |-- MH7_Nacelle_B-NoBearing.stl
|   |
|   |-- Motor Yatırma Yatağı
|       |-- Parça Çeşidi: Bilyalı Rulmanlı Sürüm
|       |   |-- MH7_TiltMount_A-Bearing.stl
|       |   |-- 3mm Mil veya Dişli Cıvata, Uzunluk=44mm
|       |
|       |-- Parça Çeşidi: Bilyalı Rulmansız Sürüm
|       |   |-- MH7_TiltMount_A-NoBearing.stl
|       |   |-- 1.85mm Çelik Pim, Uzunluk=40mm
|       |
|       |-- MH7_TiltMount_B.stl
|       |-- BLDC Motor
|    
|-- Sol Kanat Ucu Yüzeyi
|   |-- Parça Çeşidi: Yalın Kanat Ucu Yüzeyi
|   |   |-- MH7_WingletLeft.stl
|   |
|   |-- Parça Çeşidi: GPS Yuvası
|       |-- MH7_WingletLeft-GPS.stl
|
|-- Sağ {Kanat, Dikey Stabilize, Gondol, Motor Yatırma Yatağı, Kanat Ucu Yüzeyi} 
|   |-- Simetrik parçaların her birinin sağ taraf sürümünü oluşturmak için parçayı dilimleyici yazılımınızda aynalamanız yeterlidir. 
        Lütfen _çok dikkatli_ olun! Özellikle gondol parçaları olmak üzere tüm parçaların nasıl birleştiğini anladığınızdan emin olun: 
        Gondolun _A parçası her zaman uçağın merkez gövdesine yakındır; _B parçası ise dış tarafta, 
        servolarla hizalı ve merkez gövdeden uzaktadır. Hiçbir ikisi aynı olmayan dört ayrı gondol parçası basmalısınız: 
        Aynalanmamış birer _A ve _B parçası ve aynalanmış birer _A ve _B parçası.

Yardımcı Düzenekler ve Parçalar
|-- Ağırlık ve Denge Destek Sehpası
|   |-- Gondol Destek Kirişi
|   |   |-- MH7_WeightBalanceStand_Beam.stl
|   |   |-- MH7_WeightBalanceStand_Support.stl
|   |   |-- İki adet 1.85mm Çelik Pim, Her Biri Uzunluk=50mm
|   |
|   |-- Kuyruk Takımı Destek Ayağı
|       |-- MH7_WeightBalanceStand_Foot.stl
|       |-- MH7_WeightBalanceStand_Support.stl (Yapıştırdıktan sonra üçgen bir duruş oluşturmak için bacakları sıcak suyla bükün)
|       |-- 1.85mm Çelik Pim, Uzunluk=50mm
|
|-- Topluluk Değişiklikleri için Kapağın STEP/STP Sürümü
    |-- MH7_Hatch_RELEASED.stp
```


# Montaj Sırası <a name="buildseq-brief"></a>
Aşağıdaki talimatlarda, yukarıda listelenen gövde parçalarının tamamının basılmış olduğu varsayılır. Her parça için tipik dilimleyici ayarlarının ayrıntıları için [3B Baskı Kılavuzu Bölümüne](#3dprinting-brief) bakın. Ayrıca deponun [3mf-Implementations](/3mf-Implementations) klasöründe 3MF üretim dosyaları bulunur; ancak baskı ayarlarının sizin yazıcınıza doğru aktarılıp aktarılmayacağı biraz şansa bağlıdır.

[Figure-1]: </doc-Documentation/Figure-1.png> "Şekil 1 - Menteşe Pimi Boşluğu" 
[Figure-2]: </doc-Documentation/Figure-2.png> "Şekil 2 - Elevon Hareket Yarıkları"
[Figure-3]: </doc-Documentation/Figure-3.png> "Şekil 3 - Kapak Parçalarının Yapıştırılması"
[Figure-4]: </doc-Documentation/Figure-4.png> "Şekil 4 - Kuyruk Takımı Yarılarının Yapıştırılması"
[Figure-5]: </doc-Documentation/Figure-5.png> "Şekil 5 - Elevon Kumanda Yekesi Montajı"
[Figure-6]: </doc-Documentation/Figure-6.png> "Şekil 6 - Kuyruk Takımı/Kuyruk Montajı"
[Figure-7]: </doc-Documentation/Figure-7.png> "Şekil 7 - Gondol Yarılarının Yapıştırılması"
[Figure-8]: </doc-Documentation/Figure-8.png> "Şekil 8 - Kanat Montajı"
[Figure-9]: </doc-Documentation/Figure-9.png> "Şekil 9 - Gondol Yuvasının Son İşlemleri"
[Figure-10]: </doc-Documentation/Figure-10.png> "Şekil 10 - Mil ve Cıvata Deliğinin Raybalanması"
[Figure-11]: </doc-Documentation/Figure-11.png> "Şekil 11 - Gondol Montajı"
[Figure-12]: </doc-Documentation/Figure-12.png> "Şekil 12 - Dikey Stabilize Montajı"
[Figure-13]: </doc-Documentation/Figure-13.png> "Şekil 13 - Strake Montajı"
[Figure-14]: </doc-Documentation/Figure-14.png> "Şekil 14 - Bağlantı Mekanizmaları ve Hareketler"
[Figure-15]: </doc-Documentation/Figure-15.png> "Şekil 15 - Pervane Dönüş Yönleri"
[Figure-16]: </doc-Documentation/Figure-16.png> "Şekil 16 - Kütle Merkezi"

## Bölüm 1 - Gövde Yapıları ve Motor Yatağı/Yatırma Mekanizmasının Montajı <a name="buildseq-part1"></a>
1. 3B baskı parçalarının tamamını temizleyin; tüm kenar tutunma (brim) ve destek malzemelerini kaldırın. Çapakları ve kusurları giderin. Her kanatta, menteşe piminin oturabilmesi için menteşe takviye yuvalarındaki ipliklenmeleri veya fazla ekstrüzyonu dikkatlice kazıyın. [Şekil 1][Figure-1] Pitot probu kanalında ve diğer küçük ayrıntılarda da giderilmesi gereken ipliklenmeler olabilir.  

2. Gerekirse elevonları dikkatlice keserek serbestleştirin (**UYARI!** Yüzeyin sapabilmesi için yalnızca iki uçtaki yarıkları kesin; elevonun tamamını KESİP ÇIKARMAYIN). [Şekil 2][Figure-2] Esnek menteşe oluşana kadar her yüzeyi hafifçe yukarı aşağı hareket ettirin. Başlamak için en iyi yol, kumanda yüzeyine basıncı eşit dağıtacak sert ve düz bir nesne kullanarak elevonları aşağıya (burun aşağı kumandası verir gibi) bükmektir. Yalnızca güvenli bulduğunuz kadar ilerleyin, ardından yönü tersine çevirin. Menteşeyi +/- 30 derece hareket edene kadar nazikçe çalıştırmaya devam edin. PLA veya şekil değiştirdikçe sertleşen başka bir malzemeyle bastıysanız, takviye bandı veya parçaları takılana kadar menteşeyi tekrar tekrar hareket ettirmeyin; ancak bunlar takıldıktan sonra düzgün hareket edene kadar alıştırmaya devam edin.  

<!-- Bunu okuyorsanız: GitHub, düzgün satır ve aralıklara sahip bir tabloya resim yerleştirmeyi gerçekten zorlaştırıyor. -->
<!-- Aşağıdaki HTML, Aralık 2021 itibarıyla görselleri GitHub’da düzgün gösteriyor; diğer Markdown işleyicilerinde çalışmayabilir. -->
<table style="width:100%">
  <tr>
    <td><figure>
      <img src="/doc-Documentation/Figure-1.png" alt="Şekil 1" height="240" width="auto"><br>
      <figcaption>Şekil 1. Menteşe Pimi Boşluğu</figcaption></figure></td>
    <td><figure>
      <img src="/doc-Documentation/Figure-2.png" alt="Şekil 2" height="240" width="auto"><br>
      <figcaption>Şekil 2. Elevon Hareket Yarıkları</figcaption></figure></td>
  </tr>
</table> 

3. Kanopi/kapak parçalarını ince/orta kıvamlı siyanoakrilat ile birbirine yapıştırın ve kürlenmesi için kenara alın. [Şekil 3][Figure-3]  

4. Kuyruk takımı yarılarını siyanoakrilat kullanarak birbirine yapıştırın. (Tek parçalı -Full sürümünü bastıysanız bu adımı atlayın.) Kürlenmesi için kenara alın. [Şekil 4][Figure-4]  

<table style="width:100%">
  <tr>
    <td><figure>
      <img src="/doc-Documentation/Figure-3.png" alt="Şekil 3" height="240" width="auto"><br>
      <figcaption>Şekil 3. Kapak Parçalarının Yapıştırılması</figcaption></figure></td>
    <td><figure>
      <img src="/doc-Documentation/Figure-4.png" alt="Şekil 4" height="240" width="auto"><br>
      <figcaption>Şekil 4. Kuyruk Takımı Yarılarının Yapıştırılması</figcaption></figure></td>
  </tr>
</table> 

5. Kumanda yekelerini elevonlara sıkı geçme takarak uyumu deneyin. Yeke üstten yerleştirilir ve elevondan geçer; deliği menteşe hattının altında ortalanmış, elevon servo bağlantısıyla aynı hizada olmalıdır. Parçalar elevonun üst yüzeyiyle büyük ölçüde aynı hizada olmalı, yüzeyin üzerinde yaklaşık 0.5mm çıkıntı yapmalıdır. Geçme sıkı olmalıdır; ancak yekeyi fazla zorlamayın, baskı katmanlarını ayırıp hasara neden olabilirsiniz. Çok sıkıysa elevondaki yarıkta bulunan çapakları veya fazla ekstrüzyonu dikkatlice kazıyın ya da yekeyi zımparalayarak inceltin. Kumanda yekelerini (2) siyanoakrilat kullanarak her elevona (sol ve sağ kanat) yapıştırın. [Şekil 5][Figure-5]  

6. Du-Bro naylon mini menteşe parçalarını (kanat başına 3 adet, Du-Bro SKU#118) her elevon menteşesi boyunca bulunan yuvalara yapıştırın. Sıcak silikon veya siyanoakrilat işe yaramalıdır. 3M™ Transpore™ cerrahi bant da uygun bir menteşe takviyesidir ve şimdi veya montajın ilerleyen aşamalarında uygulanabilir.  

7. Yapıştırılmış kuyruk takımının/kuyruğun birleşme yüzeyini pürüzsüz ve düz olana kadar hafifçe zımparalayın. Gövdeye/burna deneme montajı yaparak yüzeylerin düzgün oturduğunu doğrulayın, ardından siyanoakrilat kullanarak gövdeye/burna yapıştırın. Kürlenmesi için kenara alın. [Şekil 6][Figure-6]  

<table style="width:100%">
  <tr>
    <td><figure>
      <img src="/doc-Documentation/Figure-5.png" alt="Şekil 5" height="240" width="auto"><br>
      <figcaption>Şekil 5. Elevon Kumanda Yekesi Montajı (Üstten yarığa yerleştirin)</figcaption></figure></td>
    <td><figure>
      <img src="/doc-Documentation/Figure-6.png" alt="Şekil 6" height="240" width="auto"><br>
      <figcaption>Şekil 6. Kuyruk Takımı/Kuyruk Montajı</figcaption></figure></td>
  </tr>
</table> 

8. Gondol çiftlerinin yarılarını birbirine yapıştırın; **burada dikkatli olun!** Her gondol bir `_A` ve bir `_B` parçasından oluşur. Toplam dört gondol parçası olmalı ve her biri farklı olmalıdır: aynalanmamış bir `_A` ve `_B` ile aynalanmış bir `_A` ve `_B`. `_A` parçasında saplama kolu için oyuk yoktur; `_B` parçasında vardır. `_A` parçaları her zaman uçağın merkez gövdesine en yakında, `_B` parçaları ise her zaman dışta ve servolarla hizalıdır. Parçaları siyanoakrilat kullanarak mümkün olduğunca dikkatli ve hassas biçimde birbirine yapıştırın. Kürlenmesi için kenara alın. [Şekil 7][Figure-7]  

9. Tamamlanmış gövdedeki her iki kanat kökü birleşme yüzeyini düz ve pürüzsüz olana kadar hafifçe zımparalayın. Karbon fiber ana kirişi deneyerek takın ve her iki kanattaki kiriş kanalında herhangi bir kusura takılmadığını doğrulayın. Kusur varsa yaratıcı çözümler kullanın; genellikle kirişle biraz kuvvetlice yoklamak, 3B baskı kanala zarar vermeden bunları temizler. Kiriş, kiriş kanalını (7mm iç çap) tamamen doldurmuyorsa, örneğin karbon kiriş 5mm yuvarlak boruysa, sıkı oturması için bir şim veya başka dolgu uygulayın; örneğin kirişin uçlarına ve merkez gövde boşluğuna çıktığı orta bölge yakınına bant sarın. Hizalamayı sağlamak için kiriş takılıyken her iki kanadı ilgili yüzeyde deneyerek düzgün bir birleşme olduğunu doğrulayın. Kirişi sol ve sağ kanatlara eşit miktarda girecek şekilde ortalayın. (Desteklenen en uzun kiriş 640mm’dir. Ortalandığı sürece daha kısa kiriş de uygundur.) Kanatları çıkarın. İsterseniz bu aşamada kirişi gövdeye yapıştırabilirsiniz. (Örneğin uçak tamamen hasar görüp kiriş sağlam kalırsa, sonradan yeniden kullanmayı planlıyorsanız kirişi yapıştırıcı olmadan takabilirsiniz.) Sol veya sağ kanadı siyanoakrilatla gövdeye yapıştırın (ikisini aynı anda takmak önerilmez). Kürlenmesi için kenara alın. İlk kanat kürlendikten sonra ikinci kanadı yapıştırıp kürlenmesi için kenara alın. [Şekil 8][Figure-8]  

<table style="width:100%">
  <tr>
    <td><figure>
      <img src="/doc-Documentation/Figure-7.png" alt="Şekil 7" height="240" width="auto"><br>
      <figcaption>Şekil 7. Gondol Yarılarının Yapıştırılması</figcaption></figure></td>
    <td><figure>
      <img src="/doc-Documentation/Figure-8.png" alt="Şekil 8" height="240" width="auto"><br>
      <figcaption>Şekil 8. Kanat Montajı</figcaption></figure></td>
  </tr>
</table> 

10. Her motor yatağını (yatırma yatağı/podu), ilgili tamamlanmış gondolda deneyin. Motor yatağının öne doğru tamamen yaslanabilmesi ve yukarı doğru 90 dereceden fazla dönebilmesi için gerektiği kadar zımparalayın veya keserek düzeltin. [Şekil 9][Figure-9]  

11. (Bilyalı rulmansız gondol sürümü) Her gondolda ilgili motor yatağı hizalanmış ve yerindeyken, 1.58mm (1/16 inç, 62.5mil) matkap ucuyla raybalayın (deliği ölçüsüne getirin). (Bu, takılacak menteşe çubuğunun çapının %85 ile %90’ı olmalıdır. Burada menteşe çubuğunun çapı 1.84mm veya 72mil’dir.) Motor yatağı ile gondolu birlikte tutun. Bir menteşe çubuğu parçasının ucunu taşlama veya zımpara taşıyla sivrilterek son hassas raybalama aletine dönüştürün. Bu doğaçlama aletle her gondol-yatak çiftinin deliğini nihai 1.84mm (72mil) çapa getirin. [Şekil 10][Figure-10]  

<table style="width:100%">
  <tr>
    <td><figure>
      <img src="/doc-Documentation/Figure-9.png" alt="Şekil 9" height="240" width="auto"><br>
      <figcaption>Şekil 9. Gondol Yuvasının Son İşlemleri</figcaption></figure></td>
    <td><figure>
      <img src="/doc-Documentation/Figure-10.png" alt="Şekil 10" height="240" width="auto"><br>
      <figcaption>Şekil 10. Mil ve Cıvata Deliğinin Raybalanması</figcaption></figure></td>
  </tr>
</table> 

12. (Bilyalı rulmanlı gondol sürümü) Yukarıdaki rulmansız gondol tasarımına ilişkin adımları izleyin; ancak mil deliğini raybalamak için 3.00mm (7/64 inç, 118mil) matkap ucu kullanın. Mekanik sürtünme ilişkisi tersinedir: motor yatırma yatağı, içine yerleştirilen mile sıkı geçmeyle tutunur; gondolun çatal/kollarındaki bilyalı rulmanlar ise düzgün dönme arayüzünü sağlar. Rulmanları yuvalarına sıkı geçmeyle yerleştirin; yalnızca uygunsa hafif ısı kullanın. Rulmanları da tutan ve iki rulmandan herhangi birinin yerinden çıkmasını önleyen bir mil sabitleme çözümü geliştirin. Gondolun "çatallarına" bası uygulayan bir çözümden kaçının; bu, sıkışmaya ve sürtünmeye yol açar.  

13. (Bilyalı rulmansız gondol sürümü) Her motor yatağını ilgili gondoldan çıkarın ve yalnızca motor yatağının deliğini bir üst matkap ucu ölçüsüne genişletin; menteşe çubuğu çapının %107’sini aşmayın. Böylece dıştaki gondol kolu metal mili sıkı geçmeyle tutarken, içteki motor yatağı plastik-metal temasında düzgünce dönebilir. Delik fazla büyük olursa aşırı boşluk ve olası tıkırtı, fazla küçük olursa sıkışma oluşur. 1.84mm menteşe çubuğu çapı için 1.95mm (77mil, 5/64 inç) uygundur.  

14. (Bilyalı rulmansız gondol sürümü) Menteşe çubuğu parçalarını en fazla 40mm uzunluğunda kesin. İsterseniz bir veya iki ucunu pürüzlendirin/tırtıllayın. Her menteşe çubuğunu ilgili motor yatağından geçirerek gondola sıkı geçmeyle takın. Her motor yatağının serbestçe ve menteşede çok az boşlukla dönebildiğini doğrulayın.  

15. Önerilen 1/16 küresel başlı saplamayı kullanıyorsanız, her motor yatağındaki bağlantı montaj deliğini 1.19mm (3/64 inç, 47mil) çapa raybalayın. Bu delik, 2-56 (1.84mm, 72mil) gibi daha büyük dişli bir küresel saplama için de genişletilebilir; bu durumda dikkatli değerlendirme yapın. Raybalanmış delik, takılacak dişli küresel mafsalın dış diş çapının yaklaşık %80’i olmalıdır. Dişli küresel mafsalı bağlantı montaj deliğine takın. Motor yatağı, en fazla 8mm dişli küresel saplama cıvatası giriş derinliğine dayanabilir.  

16. Her gondolu ilgili kanada yapıştırın; küresel mafsalın ilgili servo bağlantı yarığı/yuvasıyla hizalanması gerektiğine dikkat edin. Siyanoakrilat PLA’da çok iyi çalışır; ancak burası uçağın daha yüksek yük taşıyan yapılarından biri olduğundan epoksi de bir seçenektir. Yapıştırıcı kürlenirken hizalamayı doğrulayın ve konumu ince ayarlayın. [Şekil 11][Figure-11]  

17. Dikey stabilizelerin alt ve üst parçalarını birbirine yapıştırın. [Şekil 13][Figure-13] (Alt parçaya bazen "Strake" denir.) Her iki dikey stabilizeyi ilgili kanada yapıştırın. [Şekil 12][Figure-12] Siyanoakrilat yeterli olmalıdır.  

<table style="width:100%">
  <tr>
    <td><figure>
      <img src="/doc-Documentation/Figure-11.png" alt="Şekil 11" height="240" width="auto"><br>
      <figcaption>Şekil 11. Gondol Montajı</figcaption></figure></td>
    <td><figure>
      <img src="/doc-Documentation/Figure-12.png" alt="Şekil 12" height="240" width="auto"><br>
      <figcaption>Şekil 12. Dikey Stabilize Montajı</figcaption></figure></td>
  </tr>
  <tr>
    <td><figure>
      <img src="/doc-Documentation/Figure-13.png" alt="Şekil 13" height="240" width="auto"><br>
      <figcaption>Şekil 13. Strake Montajı</figcaption></figure></td>
    <td><figure>
      <img src="/doc-Documentation/Figure-14.png" alt="Şekil 14" height="240" width="auto"><br>
      <figcaption>Şekil 14. Bağlantı Mekanizmaları ve Hareketler</figcaption></figure></td>
  </tr>
</table> 

## Bölüm 2 - Bağlantı Mekanizmaları ve Bileşen Montajı <a name="buildseq-part2"></a>
1. Öndeki iki motoru ilgili motor yataklarına takın. Motor kablolarındaki ısıyla daralan makaron kabloların hareketini engelleyebilir veya sıkıştırabilir; gerekirse bunu düzeltin. Motorları, her motorla birlikte gelmesi gereken M3 dişli cıvata takımıyla monte edin. Montaj cıvatalarının motorun endüvi/stator bölümüne fazla uzanmamasına dikkat edin. Her motorun serbestçe döndüğünü ve sağlam sabitlendiğini doğrulayın. Kabloları kanattan geçirip ana bölmeye yönlendirin ve motor yatağı ileri uçuş ile askıda kalma eğimleri arasında dönerken kabloların uzama-toplanma davranışını deneyin. Her motora, standart 5 inç pervaneyi döndürebilmesi için beraberinde gelmesi gereken pervane göbeği bağlantı takımını takın.  

2. Arka motor, motorla birlikte gelen M3 dişli cıvatalarla kuyruğa takılmalıdır. Motor kablolarını istediğiniz kablo kanalından ana bölmeye geçirin. (Tercih edilen/geleneksel kanal sol/iskele tarafındaki kanaldır; böylece sağ/sancak kanalı antenler ve LED kabloları için ayrılır.) Motorun serbestçe döndüğünü ve sağlam sabitlendiğini doğrulayın. Standart 6 inç pervaneyi döndürebilmesi için motorla birlikte gelmesi gereken pervane göbeği bağlantı takımını takın. Pervanenin dikey stabilizelere değmediğini doğrulayın; gerekirse uçlarını kısaltın veya 5 inç pervaneye geçin.  

3. Motor yatağı yatırma servoları standart R/C PWM sinyaliyle 1000us, 1500us ve 2000us darbe genişlikleri uygulanarak denenmeli ve ortalanmalıdır. Delik-merkez mesafesi 19.3mm (0.76 inç) olan bir servo kolu takın. Bu değer kritiktir: öndeki motor yataklarının yatırma bağlantılarının davranışı kolayca değiştirilemez ve bundan kısa bir kol, motorun havada asılı kalma ve karşı tork (sapma) kontrolü için gereken açıya ulaşamamasına yol açar. Daha uzun bir kol ise bağlantı yuvasına/yarığına sığmaz. 19.3mm’ye olabildiğince yakın bir kol takılıyken servoyu yuvasında deneyin ve 1000us ile 2000us darbe genişlikleri arasında kolun rahatça yuvaya/yarığa toplandığını ve o noktadan yaklaşık 90 ile 95 derece kadar tam hareket ettiğini doğrulayın. Servo kolunun yivli mile en uygun takılma konumunu belirleyip kolu cıvatayla sabitleyin. [Şekil 14][Figure-14]  

4. Her elevon servosu için yukarıdaki işlemi yineleyin; ancak delik-merkez mesafesi yaklaşık 9.5mm (3/8 inç) olan bir servo kolu kullanın. Bu uzunluk biraz daha fazla veya az olabilir; bunun etkisi elevon kumanda hareketini artırmak veya azaltmaktır. Yiv sayısı tek olan servolarda (örneğin Hitec HS-65HB’nin 25 dişli B1 yivi), en iyi ortalanmış ve simetrik çözümü bulmak için servoyu 1500us darbe genişliğinde ortalayın ve 4 kollu çıkış kolunu her 90 derecelik konumda sırayla takarak en dik/ortalanmış konumu bulun; ardından gereksiz 3 kolu kesin.  

5. Servo kollarına bağlanan çatalların rahatça takılabildiğini ve serbestçe dönebildiğini doğrulayın. Her servo kolunun deliğini raybalamak gerekebilir; 1.59mm (1/16 inç, 62mil) yaygın bir ölçüdür.  

6. Servo kablolarını her kanadın altındaki kanallardan ana bölmeye yönlendirin. Tüm servoların 6 inç (~150mm) bağlantı kablosu olduğu varsayılırsa elevon servolarının kablolarında biraz pay kalır; yatırma servolarının kabloları ise ana bölmeye ancak ulaşır. Servo uzatmaları eklenebilir, servo kablosu bir parça 3 telli servo kablosuyla uzatılabilir veya istenirse 3 pinli servo konektörleri çıkarılıp daha sonra doğrudan lehim yapılabilir.  

7. Servo kablolaması herhangi bir yöntemle tamamlandıktan sonra servoları sıcak silikon kullanarak gövdeye yapıştırın. Kullanılan baskı malzemesine bağlı olarak gövdede yapıştırma noktalarında şekil değişimi veya erime görülebileceğini unutmayın. (Bunun servoları takmak için pek de iyi bir yöntem olmadığını kabul ediyorum; muhtemelen ileride değiştirilecek. Kusura bakmayın.) Servoların gövdeden ayrılmadan tam tork üretebildiğini doğrulayın. Servo montajında çift taraflı bant gibi alternatifler de denenebilir; ancak siyanoakrilat veya epoksi kullanılması önerilmez.  

8. Kullanılan iki adet 2-56 bağlantı çubuğunun dişli ucundan 45mm mesafede L büküm yaparak elevon kumanda çubuklarını oluşturun. Her bükümde tutucu Du-Bro E/Z Links 0.72 (2-56) klipsini deneyin; gerektiği kadar bükümü düzeltip fazlalığı hizalı kesin. Alternatif olarak geleneksel Z büküm yapılarak tutucu klips gereksinimi ortadan kaldırılabilir. Her elevonun kumanda çubuğunu elevon yekesine, çatalı da ilgili servo koluna takın. Servo 1500us ile ortalanmışken elevon yüzeyle aynı hizada olana kadar gerekirse çatalı çıkarın, çevirin ve yeniden takın.  

9. Yatırma kumanda çubuğu çiftini oluşturmak için tam dişli 2-56 çubuktan 70mm uzunluğunda iki (2) parça kesin. (Bu çubuklara L veya Z büküm YAPMAYIN.) Naylon küresel mafsal kuplörlerine kolayca vidalanabilmeleri için kesilen uçları taşlama veya zımpara taşıyla düzeltin. Küresel mafsal kuplörlerini ve bağlantı çatallarını vidalayın; her birini ilgili servo koluna veya küresel mafsal başlığına takın. Yatırılabilir motor yatağı tamamen öne yaslanıp gondola bastırılırken, servo sıkışma veya temas olmadan üst ölü noktaya (kolun yuvaya/yarığa toplandığı konum) olabildiğince yaklaşacak şekilde gerektiğinde bağlantıyı çıkarıp çevirerek yeniden takın. Daha önce belirtildiği gibi çatal, servo kolunun en uç deliğine, 19.3mm kol mesafesine takılmalıdır. Servo kolunun, çatal kola çarpmadan tamamen toplanabilmesi için bu çubuğu hafifçe bükmek gerekebilir. Motor yatağı toplandığında servo aşırı zorlanıyorsa gerekli ayarı yapın. **UYARI!** Çatal servo koluna sıkışmışken servonun zorlanmasına izin verilirse servo büyük olasılıkla H köprüsü sürücüsünün veya servo motorunun yanmasıyla arızalanır. Dikkatli olun ve servoları zorlamayın.  

10. Yukarıdaki adımlarda son montaj sırasında servoların beslenip komuta edildiği varsayılmıştı; ancak eksiksiz olması için bu adımda servoların hareket edebildiği ve zorlanmadığı doğrulanır. Her servoya 1000us-1500us-2000us uygulayın; elevon veya motor yatağındaki sapmayı gözlemleyip aşırı sıkışma veya zorlanma olmadığını doğrulayın. Her motor yatağında, servoya ileri uçuş ile askıda kalma konumları arasında hareket komutu verilirken motoru öne doğru hafifçe çekerek (yaklaşık 300 gram kuvvet) ileri uçuştaki yükü taklit edin. Hareket düzgün olmalı, donma/duraklama olmamalıdır. Elevonlar, kumanda yüzeyine hafif yük uygulanırken tam hareket aralığını tamamlamalıdır.

## Bölüm 3 - Elektronik ve Son Yapılandırma <a name="buildseq-part3"></a>
1. Uçuş kontrolcüsünün lehim işlerini gerektiği gibi yapın. Bu genellikle servolardan ve ESC’lerden gelen 3 pinli servo konektörlerini bağlamak için pin başlıklarının lehimlenmesi demektir. Bir batarya bağlantı kablosu (XT60 veya tercih ettiğiniz tür) lehimleyin. Uçuş kontrolcüsünü besleyin; doğru açıldığını ve iletişim kurduğunu doğrulayın. Varsayılan (muhtemelen multikopter) aygıt yazılımı sonraki birkaç adım için yeterlidir; uçuş kontrolcüsünün çıkışları yapılandırılana kadar servoların uçuş kontrolcüsüne **BAĞLANMAMASI GEREKTİĞİNİ** unutmayın.  

2. Batarya ve uçuş kontrolcüsü tablalarını ana bölmeye sabitleyin. Bu işlem M3 bağlantı elemanları, bol sıcak silikon ve gerekirse biraz raybalamayla yapılabilir. Batarya tablası kalıcı monte edilebilir; ancak uçuş kontrolcüsünü takıp çıkarmak için tablasının altına erişmek gerektiğinden uçuş kontrolcüsü tablasını çıkarılabilir tutun. Ayrıca ["Yaprak Yaylı" Uçuş Kontrolcüsü Tablasını](/stl-SourceFiles/MH7_ControllerTray2.stl) kullanıyorsanız uçuş kontrolcüsünün takılacağı yerin altına yaklaşık 30g ile 40g arasında balast ağırlığı eklenmelidir. Kendinden yapışkanlı kurşun ağırlıklar iyi çalışır. Balastın amacı, titreşim aktarım fonksiyonunun köşe frekansını yaklaşık 20 Hz’in çok altına indirmektir. Esnek "Yaprak Yay" mekanizmasının olduğu gibi kullanıldığında harmonik titreşim modları gösterebileceğini de unutmayın; örneğin zikzak kıvrımlarının arasına sıcak silikon enjekte ederek viskoelastik bir sönümleme çözümü geliştirmek gerekebilir.  

3. BLDC motor kablolarını ilgili ESC’ye lehimleyin veya isterseniz mermi tip konektör ya da başka bir bağlantı kullanın. ESC güç bağlantılarını doğrudan uçuş kontrolcüsünün güç dağıtım bölgesine veya tercih ettiğiniz ara bağlantılara lehimleyin. Pervaneleri motorlardan çıkarın. Uçuş kontrolcüsünü "Smoke Stopper" ya da akım sınırlı bir güç kaynağı kullanarak dikkatlice açın ve güç sisteminin doğru kablolandığını doğrulayın. ESC’leri doğru dönüş yönüne programlayın: sol/iskele motoru saat yönünde (CW), sağ/sancak motoru saat yönünün tersine (CCW). (ESC programlamak için BLHeli Passthru modu kullanılıyorsa ESC’ler uçuş kontrolcüsünün herhangi bir çıkışına bağlanabilir.) Arka motor teknik olarak iki yönde de dönebilir; ancak saat yönünün tersini (CCW) **kuvvetle** öneriyorum. Bu, kendini sıkan bir yapılandırmadır; dolayısıyla normal çalışmada kendi kendine gevşemesi pek olası değildir. Ayrıca multikopter dışındaki pervanelerin çoğuna olanak tanır (çoğu pervane CCW’dir) ve gelecekte PID profilleri ile kontrol şemalarının simetrik biçimde paylaşılmasını sağlayacak tutarlı bir uygulama oluşturur. [Şekil 15][Figure-15]
 > Pervane dönüş yönleri hakkında kısa not: Ön motorların belirtilen saat yönü ve saat yönünün tersi dönüşlere sahip olmasının nedeni, araç ileri uçuşta giderken aniden havada asılı kalma komutu verildiğinde ilerleyen palın/pallerin mümkün olduğunca yanda (kanat ucuna doğru), gerileyen palın ise ana gövdeye daha yakın bulunmasını sağlamaktır. Bu, geçiş sırasında daha iyi yatış kontrolü sağlamalıdır. Bu koşulda her rotorun etkin kaldırma merkezini biraz daha dışarı yerleştirmek, biraz daha uzun moment kolu sayesinde PID kontrol çabasının sınırlar içinde kalmasını ve bir miktar azalmasını daha olası kılar. Bu aynı zamanda, öndeki ilerleyen pallerin dönüş yayının dış tarafında bulunduğu tipik dört rotorlu yapılandırmaya da uyar.  

4. Bu aşamada uçuş kontrolcüsünü, trikopter VTOL sabit kanatlı bir aracı kontrol etmek için gereken aygıt yazılımı veya ayarlarla yapılandırın. Aşağıdaki [ArduPlane Ayarlarına](#arduplane-brief) bakın. Servo ve ESC konektörlerini gereken pinlere takın. R/C alıcıyı yerleştirin ve gerektiği şekilde uçuş kontrolcüsüne bağlayın. Uçuş kontrolcüsünü tablasına takın ve tablayı ana bölmeye sabitleyin. Araca güç verin; uçuş kontrolcüsünün yöneliminin doğru olduğunu, servolara doğru komut verildiğini ve kumanda yüzeylerinin doğru yönde tepki ürettiğini doğrulayın. Uçuş kontrolcüsü yapılandırma aracında (ArduPilot Mission Planner veya eşdeğeri) servo çıkışlarını gerektiği gibi ters çevirin ve trimleyin.  

5. (İsteğe bağlı) SMD5050 veya daha küçük kılıfta olmaları koşuluyla her kanat ucuna WS2812 LED takılabilir. Kablolar doğrudan kılıfın lehim pedlerine lehimlenir, ardından LED her uçtaki ışık yuvasına yerleştirilir.  

6. ESC’leri bant veya çift taraflı yapışkan pedlerle ana bölmenin yan duvarlarına yerleştirin. Fazla kabloları toplayın ve ana bölmenin içini genel olarak düzenleyin. Bataryayı cırt cırtlı kayış, bant veya başka yöntemlerle sabitleyin.  

7. Pervaneleri ilgili motorlara yeniden takın. Yukarıdaki Adım 3’te ve [Şekil 15][Figure-15]’te açıklandığı gibi dönüş yönlerinin doğru olduğunu doğrulayın. Dikey stabilizelere temas etmesini önlemek için gerekliyse arka pervanenin uçları biraz kısaltılmış olmalıdır.  

8. Uçağın kütle merkezinin kanat hücum kenarından 28mm geride olması amaçlanmıştır. Bu, yakındaki tabla montaj deliklerinin 2mm önündedir. Burnun yakınında kanatların altındaki dokunarak hissedilen "hedef" çıkıntılarının merkezleri 28mm konumundadır. Bu temel bir ölçüdür; kütle merkezi bu noktadan en fazla 2mm veya 3mm geriye kaydırılabilir, ancak bu kararlılık riskini artırır. Nötr nokta yaklaşık burada bulunduğundan ağırlık merkezi ~33mm’nin gerisindeyken uçak statik olarak kararlı UÇMAZ. Kütle merkezi kanat hücum kenarından 26mm ile 30mm geride olmalıdır. Burada açıklandığı şekilde ağırlık ve denge sehpası ile dijital terazi kullanın: [Issue #12](https://github.com/StephenCarlson/MiniHawk-VTOL/issues/12#issuecomment-828814266). Bu araç hem sabit kanatlı hem de multikopter olduğundan, burada belirtilen kütle merkezi sabit kanat uçuşu içindir. Tüm kütle merkezi ölçümleri motorlar ileri uçuş konumuna yatırılmış, pervaneler takılı ve kapak sabitlenmişken yapılmalıdır. Doğru dengeyi sağlamak için bataryayı öne veya arkaya kaydırın ya da gerekirse burun ucunun içine balast ekleyin. [Şekil 16][Figure-16]  

9. Aracı uçuşa hazır hâle getirmek için gereken diğer işlemleri yapın. Çıkartma, boya veya ısıyla uygulanan kaplama seçenekler arasındadır. Aracın toplam uçuş ağırlığı yaklaşık 1000 gram ile 1200 gram arasında olmalıdır; standart PLA ile basılmış 3B baskı gövde tek başına yaklaşık 460 gram gelir.  

<table style="width:100%">
  <tr>
    <td><figure>
      <img src="/doc-Documentation/Figure-15.png" alt="Şekil 15" height="240" width="auto"><br>
      <figcaption>Şekil 15. Pervane Dönüş Yönleri</figcaption></figure></td>
    <td><figure>
      <img src="/doc-Documentation/Figure-16.png" alt="Şekil 16" height="240" width="auto"><br>
      <figcaption>Şekil 16. Kütle Merkezi</figcaption></figure></td>
  </tr>
</table> 

# Uçuş Testleri <a name="flight-brief"></a>
Bu aracın uçuş ayarlarına sıfırdan başlama yaklaşımı kabaca şu adım sırasını izler:
1. Havada asılı kalma uçuşu için PID değerlerini belirleyin. Bu, bir test sehpası kurulumu ve yatış (roll), yunuslama (pitch), sapma (yaw) eksenlerinin ayrı ayrı yalıtılmasıyla yapılabilir. Askıda kalmadan ileri uçuşa ve ters yöndeki geçişler için kazanç çizelgelemesi de yunuslama ekseni yalıtılmış bir düzenekte yapılabilir; ancak eşdeğer bağıl rüzgâr üretilmiyorsa ileri uçuşa yaklaşan açılarda bunun geçerliliği azalır. (ArduPlane bu hesabı kendi içinde yapar; VTOL’ü başka uçuş yazılımı altyapılarına uygulamak, Kazanç Çizelgeleme Tablosu geliştirmeyi gerektirebilir.)  

2. Serbest kısa askıda kalma denemeleri ve sabit konumda askıda kalma gösterilene kadar PID ayarını sürdürün. Konum tutma davranışlarını ayarlayın ve otonom dönüş ve iniş (Return-to-Land) işlevini gösterin. Bozucu etkilere karşı sağlam toparlanma ve kararlılığı doğrulayın. Rüzgâra dönme davranışını tatmin edici olana kadar ayarlayın.  

3. Uçağın ağırlık ve dengesini doğrulayın (kanat hücum kenarından 26mm ile 30mm). Seyir hızında (19 m/s) yunuslamanın statik olarak kararlı olduğunu doğrulayın. Uçağın yönelme açısından da kararlı olduğunu (statik olarak rüzgâra yöneldiğini) doğrulayın. 19 m/s hızda yatay süzülme sağlamak için elevonların yunuslama trimini ayarlayın.  

4. Kumanda yüzeyi sapmalarının hem pilot girdileri hem de uçağın hareket ve duruşuna karşı otopilotun stabilizasyon tepkileri için doğru olduğunu doğrulayın. Gerekirse ileri uçuş PID değerlerini önemli ölçüde azaltın. Uçağı elle atarak ileri uçuşa geçirin ve kontrol edilebilir ve kararlı olduğunu doğrulayın. Kumanda hareketleri çok büyükse kontrollerin çok hassas ve hızlı olabileceğine dikkat edin. Sabit kanat uçuşundan askıda kalmaya geçin ve güvenli biçimde inin.  

5. Önceki adımdan sonra uçak hâlâ sağlam ve çalışır durumdaysa ileri uçuş için uygun PID değerlerine ulaşmak üzere AUTOTUNE veya eşdeğerini uygulayın. Rota noktası izleme davranışlarını ayarlayın ve tutarlı seyrüseferi gösterin. Uygunsa sabit kanat uçuşundan başlayan otonom inişi gösterin.  

6. Askıda kalma modunda en az 50 metreye tırmanın ve ileri uçuşa VTOL geçişlerini deneyin. Araç tutarlı biçimde ileri uçuşa geçene kadar geçiş davranışını ayarlayın. Geçişler hem pilotlu hem de otonom durumda aynı görünmelidir.
> Araç, burun yukarı duruşla (pozitif hücum açısıyla) askıda kalacak şekilde tasarlanmıştır. Bunun nedeni, burun yatay konuma indirildiğinde itki vektörünün araca başlangıçta ileri hareket kazandırmasıdır. İleri yönde bir hareket başladıktan sonra motorlar 50/50 ara konuma yatırılır ve aracın hızlanmasına izin verilir. Ardından motorlar tam ileri uçuş konumuna indirilir.
8. İleri ve ters geçiş davranışlarıyla, kalkıştan inişe kadar tamamen otonom görevleri gösterin.

# 3B Baskı Kılavuzu <a name="3dprinting-brief"></a>
Diğer 3B baskı R/C uçakların aksine MiniHawk’ta nervür veya boyuna takviye gibi iç yapılar açıkça tanımlanmamıştır; yalnızca uçağın dış yüzey geometrisi, bölmeleri, kablo kanalları ve montaj noktaları tanımlıdır. İç yapı, hacim tanımını 3B baskıya dönüştüren dilimleyici yazılımında seçilen dolgu desenine bırakılmıştır. İlerideki bir revizyonda iç yapılar açıkça tanımlanabilir; bunun dışında kullanılacak dolgu desenini belirlemek yapımcıya aittir. Aşağıdaki bölümler, her gövde parça grubu için önerilen ayarları verir (3MF dosyalarındaki ayarlarla eşleşir).

| Parametre | Sol ve Sağ Kanatlar | Burun | Kuyruk Takımı | Kapak | Gondollar | Motor Yatırma Yatakları |
| --------------------------- | -------------------------------- | ------------------------- | ------------------------- | ------------------------- | --------------------------- | --------------------------- |
| Katman Yüksekliği (LayerHeight) | 0.2mm | 0.2mm | 0.2mm | 0.2mm | 0.2mm | 0.2mm |
| Duvar Kalınlığı (WallThickness) | 0.4mm | 0.4mm | 0.4mm | 0.4mm | 0.8mm | 0.8mm |
| Üst Kalınlık (TopThickness) | 0.2mm | 0.2mm | 0.2mm | 0.2mm | 0.6mm | 0.6mm |
| Alt Kalınlık (BottomThickness) | 0.2mm | 0.2mm | 0.2mm | 0.2mm | 0.6mm | 0.6mm |
| Üst/Alt Ana Desen (TopBottomMainPattern) | Çizgiler (Lines) | Eşmerkezli (Concentric) | Çizgiler (Lines) | Çizgiler (Lines) | Çizgiler (Lines) | Çizgiler (Lines) |
| İlk Alt Katman Deseni (InitialBottomLayerPattern) | Eşmerkezli (Concentric) | Eşmerkezli (Concentric) | Eşmerkezli (Concentric) | Eşmerkezli (Concentric) | Çizgiler (Lines) | Çizgiler (Lines) |
| Duvar Arası Boşlukları Doldur (FillGapsBetweenWalls) | Hiçbir yerde (Nowhere) | Hiçbir yerde (Nowhere) | Hiçbir yerde (Nowhere) | Hiçbir yerde (Nowhere) | Her yerde (Everywhere) | Her yerde (Everywhere) |
| Z Dikişi Hizalama (Z-SeamAlignment) | Kullanıcı tanımlı (UserSpecified) (Not 1) | En keskin köşe, dikişi gizle (SharpestCorner,HideSeam) | En keskin köşe, dikişi gizle (SharpestCorner,HideSeam) | En keskin köşe, dikişi gizle (SharpestCorner,HideSeam) | En keskin köşe, dikişi göster (SharpestCorner,ExposeSeam) | En keskin köşe, dikişi göster (SharpestCorner,ExposeSeam) |
| Dolgu Yoğunluğu (InfillDensity) | 5.00% | 10.00% | 10.00% | 10.00% | 20.00% | 30.00% |
| Dolgu Deseni (InfillPattern) | Kübik (Cubic) | Kübik (Cubic) | Kübik (Cubic) | Kübik (Cubic) | Kübik (Cubic) | Kübik (Cubic) |
| Dolgu Çizgi Yönleri (InfillLineDirections) | 90deg | 0deg | 0deg (Not 2) | 90deg | 0deg | 0deg |
| Destek Oluştur (GenerateSupport) | Hiçbir yerde (Nowhere) | Hiçbir yerde (Nowhere) | Hiçbir yerde (Nowhere) | Hiçbir yerde (Nowhere) | Evet (Yes) | Hiçbir yerde (Nowhere) |
| Destek Yerleşimi (SupportPlacement) |  |  |  |  | Baskı tablasına temas eden (TouchingBuildPlate) |  |
| Destek Çıkıntı Açısı (SupportOverhangAngle) |  |  |  |  | 70deg |  |
> Not 1: Kanadın firar kenarında oluşacak şekilde zorlanır.  
> Not 2: En iyi yapı için X yönünde hafifçe kaydırılmıştır.  

MH7_ControlHornSet ve MH7_TraySet için %100 dolu veya tercih ettiğiniz şekilde baskı yapın. Mümkünse bu parçalar lazerle kesilebilir.


# ArduPlane Ayarları <a name="arduplane-brief"></a>
MiniHawk-VTOL başlangıçta BetaFlight aviyonik ekosistemi kullanılarak geliştirilmiş olsa da mevcut tasarım için önerilen ekosistem ArduPilot’tur. Bu bölüm, v2.0.0 öncesinde burada bulunan özgün Betaflight kurulum talimatlarının yerini alır. Eski Betaflight kurulum talimatları README.md dosyasının revizyon geçmişinde bulunabilir.

## R/C Kumanda Yapılandırması (Mode 2 Kumanda) <a name="arduplane-controlsconfig"></a>
| R/C Kanalı | Açıklama | 1000us | 1500us | 2000us | Notlar |
| ------------- | --------------------- | ---------------- | ------------ | ------------------------- | ---------------------------------------------------------------- |
| CH 1 | Yatış (Roll) | Sola yatış | Ortalanmış | Sağa yatış |  |
| CH 2 | Yunuslama (Pitch) | Burun yukarı | Nötr | Burun aşağı |  |
| CH 3 | Gaz/Kolektif | Rölanti | %50 itki | %100 itki | QSTABILIZE ile QLOITER/QHOVER arasında geçiş yaparken dikkatli olun |
| CH 4 | Yön dümeni | Sola sapma | Nötr | Sağa sapma |  |
| CH 5 | Uçuş modu seçimi | FBWA | QSTABILIZE | AUTO/RTL/AUTOTUNE | 3 konumlu anahtar; 2000us, ikinci bir R/C anahtarı karıştırılarak elde edilir |
| CH 6 | MANUAL zorlaması | Devre dışı | --- | MANUAL modu ETKİN! | RC6_OPTION=51, elle atarak ileri uçuşa geçmek için kullanışlıdır |
| CH 7 | Motorları etkinleştirme (Arming) anahtarı | Devre dışı | --- | MOTORLAR ETKİN! | RC7_OPTION=41, ArduPilot motor etkinleştirme/devre dışı bırakma anahtarı |
| CH 8 | Anlık anahtar | Devre dışı | --- | OSD, ters uçuş modu vb. | OSD ekranları arasında geçiş, ters uçuş (RC8_OPTION=43), diğer çeşitli kullanımlar |

MANUAL modunun yönetilmesi gerçekten zordur ve yalnızca nadiren kullanılmalıdır. Yukarıda, örneğin VTOL askıda kalma ve ileri geçiş aşamalarını atlayıp uçağı elle atmak istediğinizde, motorlar etkinleştirilirken ArduPlane VTOL durum makinesini ileri uçuşta kalmaya zorlayan bir tür "hile" olarak dahil edilmiştir. Önce CH 5 uçuş modu seçim anahtarıyla uçağı FBWA’ya alın, ardından MANUAL zorlama anahtarını yalnızca bir an açıp yeniden devre dışı bırakın (uçuş modu, uçuş modu anahtarında ayarlanan FBWA’ya döner). Aksi hâlde yalnızca FBWA seçip motorları etkinleştirirseniz uçak, üç motorun da askıda kalma koşulunda döndüğü ArduPlane VTOL ileri geçiş davranışına hemen geri döner.

## Uçuş Kontrolcüsü Bağlantıları <a name="arduplane-connections"></a>
Aşağıdaki tablo mRobotics PixRacer Pro için geçerlidir. Başka bir ArduPlane uyumlu uçuş kontrolcüsü kullanılıyorsa ona uyarlanmalıdır.

| Pin # | Bağlanan Bileşen |
| ------- | --------------------- |
| S1 | Sağ motor ESC’si |
| S2 | Sol motor ESC’si |
| S3 | BAĞLANTI YOK (BEC) |
| S4 | Arka/kuyruk motoru ESC’si |
| S5 | Sol yatırma servosu |
| S6 | Sağ yatırma servosu |
| S7 | Sol elevon servosu |
| S8 | Sağ elevon servosu |

## ArduPlane Parametreleri <a name="arduplane-parameters"></a>
Aşağıdaki parametre dosyası, mRo PixRacer Pro uçuş kontrolcüsü kullanan tipik bir MiniHawk-VTOL’deki ayarları temsil eder. Temel ayarlar Matek F405-WING veya benzeri herhangi bir ArduPlane uyumlu uçuş kontrolcüsüne uygulanabilmelidir; ancak bazı uyarlamalar gerekecektir. **UYARI!** Modern ESC protokolleri (OneShot veya DShot gibi), yanlışlıkla servo bağlandığında servolarla uyumlu çalışmaz. En iyi durumda servo paketi süzer; ancak bazı durumlarda servo yanar. Servoları ESC çıkışlarına takmayın!

mRo PixRacer Pro: [ArduPlane_MiniHawk_mRo_PixRacerPro.param](/cfg-Config/ArduPlane_MiniHawk_mRo_PixRacerPro.param)

Yukarıdaki parametre dosyasında 1100’den fazla parametre bulunur; temel parametrelerden bazıları aşağıda incelenmiştir:
```
| Parametre,Değer | Notlar |
| ---------------------- | ---------------------------------------------------------- |
| ARSPD_FBW_MAX,32       | Tam gazda yaklaşık 32 ile 34 m/s kısa süreli azami hız |
| ARSPD_FBW_MIN,17       | Tipik bir MiniHawk-VTOL için perdövites yaklaşık 15 m/s’dedir |
| ARSPD_RATIO,1.9936     | Uçağınız için kalibre edildiğinden emin olun |
| ARSPD_TUBE_ORDER,0     | Otomatik (3) olabilir; ancak elle ayarlamak daha iyidir |
| ARSPD_TYPE,1           | MS4525D0 basınç sensörü; gerektiği gibi ayarlayın |
| ARSPD_USE,1            | Uçağı sentetik hız yerine pitot probunu kullanmaya zorlayın |
| AUTOTUNE_LEVEL,7       | MiniHawk-VTOL için en iyi sonuç 7 veya 8 ile alınır |
| EK2_ENABLE,0           | EKF3 tercih edilerek EKF2 devre dışı bırakılmıştır |
| EK3_ENABLE,1           | Tasarımın uçuş testlerinin çoğunda EKF3 kullanıldı |
| FLTMODE_CH,5           | Uçuş modu kanalı |
| FLTMODE1,5             | FBWA, 3 konumlu anahtarın "Aşağı" konumu |
| FLTMODE2,19            | QLOITER, 3 konumlu anahtarın "Orta" konumu |
| FLTMODE3,17            | QSTABILIZE, 3 konumlu anahtarın "Yukarı" konumu |
| FLTMODE4,17            |                                                            |
| FLTMODE5,17            |                                                            |
| FLTMODE6,10            | AUTO, 3 konumlu anahtarı geçersiz kılan 2. R/C anahtarı |
| FS_LONG_ACTN,1         | Geliştirmede kullanılan arıza emniyeti ayarları |
| FS_LONG_TIMEOUT,3      |                                                            |
| FS_SHORT_ACTN,1        |                                                            |
| FS_SHORT_TIMEOUT,1     |                                                            |
| KFF_RDDRMIX,0          | Olası tüm yön dümeni karıştırmalarını kaldırın |
| LIM_PITCH_MAX,2000     | Yunuslama ve yatış açısı sınırları |
| LIM_PITCH_MIN,-2500    |                                                            |
| LIM_ROLL_CD,5500       |                                                            |
| MIXING_GAIN,0.5        | Elevon kumanda çubuğu karıştırması; buradaki değer varsayılan olmalı |
| NAVL1_PERIOD,11        | Daha atak seyrüsefer mümkündür; 11 ile 14 arası denendi |
| PTCH_RATE_D,0          | Yunuslama PID’leri; bu değerler düşüktür, AUTOTUNE artıracaktır |
| PTCH_RATE_FF,0.345     |                                                            |
| PTCH_RATE_FLTD,4       |                                                            |
| PTCH_RATE_FLTE,7       |                                                            |
| PTCH_RATE_FLTT,1.5     |                                                            |
| PTCH_RATE_I,0.15       |                                                            |
| PTCH_RATE_IMAX,0.666   |                                                            |
| PTCH_RATE_P,0.04       |                                                            |
| PTCH_RATE_SMAX,150     |                                                            |
| PTCH2SRV_RLL,1         |                                                            |
| PTCH2SRV_RMAX_DN,90    |                                                            |
| PTCH2SRV_RMAX_UP,90    |                                                            |
| PTCH2SRV_TCONST,0.4    |                                                            |
| Q_A_ACCEL_P_MAX,110000 | Geliştirmede kullanılan VTOL yatış/yunuslama/sapma açısal ivmeleri |
| Q_A_ACCEL_R_MAX,110000 |                                                            |
| Q_A_ACCEL_Y_MAX,27000  |                                                            |
| Q_A_RAT_PIT_D,0.0005   | VTOL yunuslama PID’leri |
| Q_A_RAT_PIT_FF,0       |                                                            |
| Q_A_RAT_PIT_FLTD,15    |                                                            |
| Q_A_RAT_PIT_FLTE,0     |                                                            |
| Q_A_RAT_PIT_FLTT,20    |                                                            |
| Q_A_RAT_PIT_I,0.15     |                                                            |
| Q_A_RAT_PIT_IMAX,0.5   |                                                            |
| Q_A_RAT_PIT_P,0.15     |                                                            |
| Q_A_RAT_PIT_SMAX,0     |                                                            |
| Q_A_RAT_RLL_D,0.003    | VTOL yatış PID’leri |
| Q_A_RAT_RLL_FF,0       |                                                            |
| Q_A_RAT_RLL_FLTD,15    |                                                            |
| Q_A_RAT_RLL_FLTE,0     |                                                            |
| Q_A_RAT_RLL_FLTT,20    |                                                            |
| Q_A_RAT_RLL_I,0.25     |                                                            |
| Q_A_RAT_RLL_IMAX,0.5   |                                                            |
| Q_A_RAT_RLL_P,0.45     |                                                            |
| Q_A_RAT_RLL_SMAX,0     |                                                            |
| Q_A_RAT_YAW_D,0.02     | VTOL sapma PID’leri |
| Q_A_RAT_YAW_FF,0.1     |                                                            |
| Q_A_RAT_YAW_FLTD,0     |                                                            |
| Q_A_RAT_YAW_FLTE,10    |                                                            |
| Q_A_RAT_YAW_FLTT,20    |                                                            |
| Q_A_RAT_YAW_I,0.1      |                                                            |
| Q_A_RAT_YAW_IMAX,0.5   |                                                            |
| Q_A_RAT_YAW_P,0.6      |                                                            |
| Q_A_RAT_YAW_SMAX,0     |                                                            |
| Q_ANGLE_MAX,3000       | VTOL yunuslama ve yatış açısı sınırları |
| Q_ASSIST_ALT,0         | Mümkün olduğunda VTOL yardımını devre dışı bırakın |
| Q_ASSIST_ANGLE,0       |                                                            |
| Q_ASSIST_DELAY,0.5     |                                                            |
| Q_ASSIST_SPEED,0       |                                                            |
| Q_AUTOTUNE_AGGR,0.1    | Geliştirmede kullanılan VTOL Autotune ayarları |
| Q_AUTOTUNE_AXES,2      |                                                            |
| Q_AUTOTUNE_MIN_D,0.001 |                                                            |
| Q_ENABLE,1             | MiniHawk-VTOL için VTOL elbette etkindir |
| Q_FRAME_CLASS,7        | Trikopter yapılandırması |
| Q_FW_LND_APR_RAD,85    | Sabit kanattan VTOL’e geçiş eşiği için 85 metre |
| Q_M_HOVER_LEARN,2      | Askıda kalma gaz hedef değerinin öğrenilmesi |
| Q_M_PWM_TYPE,4         | DShot 150 yeterlidir ve parazite dayanıklıdır |
| Q_M_SPIN_ARM,0.05      | Motorlar etkinleştirildiğinde %5 gaz |
| Q_M_SPIN_MAX,1         | %100 gaz; en yüksek ESC devir komutu |
| Q_M_SPIN_MIN,0.1       | En düşük ESC devri için %10 gaz |
| Q_M_SPOOL_TIME,0.5     | 500ms devre çıkma süresi |
| Q_M_THST_EXPO,0.25     | Gaz üstel eğri ayarı (Expo) |
| Q_M_YAW_HEADROOM,50    | 50us sapma kontrol payı |
| Q_M_YAW_SV_ANGLE,12    | Sapma eğim açısı için "12" derece |
| Q_OPTIONS,1056         | Motorlar devre dışıyken sapma hareketine izin ver; QRTL davranışı |
| Q_RC_SPEED,490         | 490 Hz motor güncellemeleri |
| Q_RTL_ALT,40           | VTOL’de RTL davranışları |
| Q_RTL_MODE,1           |                                                            |
| Q_TILT_MASK,3          | Hangi motorların yatırıldığı |
| Q_TILT_MAX,55          | AirspeedWait etkinken geçiş açısı |
| Q_TILT_RATE_DN,15      | Yukarı/aşağı yatırma hızları |
| Q_TILT_RATE_UP,75      |                                                            |
| Q_TILT_TYPE,2          | Vektörlü sapma yatırma türü |
| Q_TILT_YAW_ANGLE,14    | "14" derece VTOL askıda kalma konumu |
| Q_TRANS_FAIL,0         | Geçiş zaman aşımı devre dışıdır |
| Q_TRANSITION_MS,1000   | Geçiş sonrası bekleme süresi |
| Q_TRIM_PITCH,9         | İleri uçuş ve askıda kalma duruşları arasındaki yunuslama farkı |
| Q_WVANE_GAIN,0.4       | Bu tasarım için 0.4 iyi bir değerdir |
| RC7_OPTION,41          | Motor etkinleştirme anahtarı; uçuşta/askıda kalmada motorları devre dışı bırakır! |
| RCMAP_PITCH,2          | Yatış/Yunuslama/Gaz/Sapma (AETR) kumanda sıralaması |
| RCMAP_ROLL,1           |                                                            |
| RCMAP_THROTTLE,3       |                                                            |
| RCMAP_YAW,4            |                                                            |
| RLL_RATE_D,0           | Yatış PID’leri; bu değerler düşüktür, AUTOTUNE artıracaktır |
| RLL_RATE_FF,0.345      |                                                            |
| RLL_RATE_FLTD,4        |                                                            |
| RLL_RATE_FLTE,7        |                                                            |
| RLL_RATE_FLTT,3        |                                                            |
| RLL_RATE_I,0.15        |                                                            |
| RLL_RATE_IMAX,0.666    |                                                            |
| RLL_RATE_P,0.08        |                                                            |
| RLL_RATE_SMAX,150      |                                                            |
| RLL2SRV_RMAX,90        |                                                            |
| RLL2SRV_TCONST,0.4     |                                                            |
| RTL_AUTOLAND,2         | RTL’de sabit kanattan VTOL inişine geçiş davranışı |
| RUDD_DT_GAIN,3         | Ön motorlarda çok hafif diferansiyel itki karıştırması |
| SCALING_SPEED,15       | Varsayılan değer 15 m/s olmalıdır |
| SCHED_LOOP_RATE,300    | Geliştirmede 300 Hz kullanıldı |
| SERVO1_FUNCTION,33     | Sağ BLDC motor |
| SERVO2_FUNCTION,34     | Sol BLDC motor |
| SERVO3_FUNCTION,0      | Bağlantı yok; mRo PixRacer Pro’da 5V BEC buraya bağlanır |
| SERVO4_FUNCTION,36     | Arka BLDC motor |
| SERVO5_FUNCTION,75     | Sol yatırma servosu |
| SERVO5_MAX,1800        | MAX ve MIN değerleri elle kalibre edilir; 1920/1080’e yakındır |
| SERVO5_MIN,1200        | Buradaki 1200/1800 değerleri yeni montajlarda hasarı önlemek içindir |
| SERVO5_REVERSED,0      | Sol yatırma normal dönüş yönündedir |
| SERVO6_FUNCTION,76     | Sağ yatırma servosu |
| SERVO6_MAX,1800        |                                                            |
| SERVO6_MIN,1200        |                                                            |
| SERVO6_REVERSED,1      | Sağ yatırma ters dönüş yönündedir |
| SERVO7_FUNCTION,77     | Sol elevon servosu |
| SERVO7_REVERSED,1      | Sol elevon ters dönüş yönündedir |
| SERVO8_FUNCTION,78     | Sağ elevon servosu |
| SERVO8_REVERSED,0      | Sağ elevon normal dönüş yönündedir |
| STAB_PITCH_DOWN,2      | Varsayılan 2 olmalıdır; sıfır gazdaki yunuslama davranışı |
| STALL_PREVENTION,0     | Etkinleştirilebilir; geliştirme sırasında devre dışıydı |
| STICK_MIXING,1         | Otonom modlarda pilot girdilerinin nasıl birleştirildiği |
| TECS_PTCH_FF_V0,19     | 19 m/s seyir |
| TRIM_ARSPD_CM,1900     | 19 m/s seyir |
| TRIM_PITCH_CD,350      | Yatay uçuş yunuslama açısı ile tabla açısı arasındaki fark |
| TRIM_THROTTLE,55       | 19 m/s seyir için tipik gaz değeri |
| WP_LOITER_RAD,60       | Loiter için tipik yarıçap 60 metre |
| WP_RADIUS,40           | Tipik rota noktası yarıçapı 40 metre |
```


## Notlar: <a name="arduplane-remarks"></a>
MiniHawk-VTOL Sürüm 2’nin geliştirilmesinde ArduPlane v4.1.0 ve v4.2.0dev kullanılmıştır. ArduPlane, bu tasarım gibi bir trikopter tiltrotoru varsayılan olarak destekler; VTOL davranışlarını etkinleştirmek için yalnızca parametrelerin ayarlanması gerekir.

Bu aygıt yazılımı sürümünde VTOL uçuş davranışlarının ele alınışında sezgisel olmayan bazı yönler vardır. En rahatsız edici olanı, hem pilotlu hem de otonom uçuşta VTOL uçuş durumunun doğrudan kontrol edilememesidir. VTOL durum makinesi, ileri uçuş durumuna doğrudan komut vermek yerine sabit kanat uçuşuna ileri VTOL geçişini yürütmek için bir hava hızı tahmini (sentetik veya pitot probuyla ölçülmüş) ister. Bu, insan pilotu geçiş sürecinde yalnızca söz sahibi katılımcılardan biri yapar; yatırılabilir rotorların ne zaman tamamen öne yatırılabileceğini ve arka motorun ne zaman duracağını kazanılan hava hızı belirler. Geliştiricilerin yaklaşımı askıda kalmayı varsayılan geri dönüş durumu kabul eder; belirli bir sürede hava hızı kazanılamaması, `Q_TRANS_FAIL` üzerinden arıza emniyeti olarak süreci askıda kalmaya geri döndürür. Bu geçiş başarısızlığı zaman aşımı devre dışı bırakılırsa AirspeedWait durumu sürer ve araç trikopter ile sabit kanat uçuşunun yarı yarıya karışımı hâlinde süresiz uçar. MiniHawk-VTOL gibi yüksek güçlü ve çok hızlı bir tasarımda, zaman aşımının aracı bu karma davranışta bırakmak veya geçiş başarısızlığı zamanlayıcısı kullanılıyorsa çok uzak mesafe ve yüksek irtifada sınırlı bataryayla askıda kalmaya geçirmek yerine ileri uçuşu zorlaması daha mantıklı olurdu; ancak bu başka bir günün pull request konusu. Bu nedenle, aygıt yazılımının mevcut durumu için bu davranışı ve neden karma modda takılı kaldığını bilmek gerekir.

İleri VTOL geçiş davranışının başka bir sonucu da motorlar devre dışıyken ileri uçuş modu (örneğin FBWA) seçildiğinde rotorlar öne yatmasına rağmen, motorlar etkinleştirildiği anda aracın AirspeedWait durumuna geçmesi; ön rotorların yukarı yatıp arka rotorun dönmeye başlamasıdır. Gaz ayarı görünüşe göre askıda kalma ile ileri uçuş için hava hızı bekleme arasındaki karışımı belirler. Ancak geleneksel sabit kanatlı bir uçak gibi elle atış yapmaya çalışıyorsanız daha iyi çözüm, bir anlığına MANUAL moduna geçmektir. Bu, VTOL durum makinesini AirspeedWait durumunun ötesine zorlar; FWBA modunda motorları etkinleştirmenize, ön rotorların ileri konumda kalmasına ve elle atış sırasında elevon stabilizasyonu ile yataylama desteğinden yararlanmanıza olanak tanır. Stabilizasyon ve yataylama olmadan tamamen MANUAL bir elle atış amaçlamıyorsanız, MANUAL modundan FBWA’ya geri dönmeyi unutmayın.

Pilot kontrolünde sabit kanat uçuşundan askıda kalmaya geçişler genellikle yumuşaktır. Ancak otonom modlarda, askıda kalmaya ters VTOL geçişinde aracın önce burnunu aşağı düşürüp sonra sert biçimde yukarı çektiği bilinen bir sorun vardır. Negatif g yükü veya ani sarsıntı parçaların ayrılmasına neden olabilecekse bu, araç için tehlikeli olabilir. Sorun muhtemelen TECS ayar parametrelerindedir veya 4.1 ya da 4.2 aygıt yazılımına özgüdür.


# Lisans <a name="license-brief"></a>
Bu çalışma Creative Commons Atıf-GayriTicari-AynıLisanslaPaylaş 4.0 Uluslararası Lisansı ile lisanslanmıştır. Lisansın bir kopyasını görmek için http://creativecommons.org/licenses/by-nc-sa/4.0/ adresini ziyaret edin veya Creative Commons, PO Box 1866, Mountain View, CA 94042, USA adresine mektup gönderin.  

Burada sunulan Ardupilot ve Betaflight yazılım yapılandırma metin dosyaları muhtemelen GPL-3.0 kapsamındadır; bu yazı yazılırken her iki proje de GPL-3.0 ile lisanslanmıştır.  

MiniHawk VTOL - Tasarım, Belgeler, Görseller ve diğer tüm Tasarım Çalışmaları; Steve Carlson tarafından  
[https://github.com/StephenCarlson/MiniHawk-VTOL](https://github.com/StephenCarlson/MiniHawk-VTOL)
