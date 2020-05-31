# Computer Networks
### (17 / 02 / 2020)
Ağ: Bigisayarların tekli bir iletişim teknelojisi kullanarak bağlayan sisteme denir.

internet : ağlara bağlı bilgisayarlae arasında trafik iletmek üzere yapılandırılmış yönlendiriciler tarafından bağlanan ağlar kümesi
veri alışverişi: ortam veri kodlaması
paket iletimi : network üzerinden veri alışverişi
internet working : ağların bir kümesi üzerinden çalışan evrensel bir servistir
network uygulaması : internet kullanan programlar bu gruptadır


## Patlayıcı Büyüme
yeni fenomen: günlük aktivitelerimizin önemli bir parçasını ağlar oluşturur
 - iş yeri
 - ev
 - hükümet
 - eğitim

## Global internet Büyüyor
 - Başlangıçta birkaç düzine alana sahip araştırma projesi
 - Bugün dünya çapında milyonlarca bilgisayar ve binlerce ağ

## İNTERNET
* Arpanet  isimli projeden gelişmiştir
 - merkezi sistemden dağıtık sisteme doğru temel değişiklikler meydana geldi
 - güvenlik ve sağlamlık gibi çeşitli özellikler eklendi
 - birden çok bağlantı
 - dağıtılmış yönlendirme
* ETHERNET yerel ağı daha makul ve kullanılabilir yapar
* ICP / IP protokolü internet üzerinden çalışma sağlayan Arpanet'ten sonra gelişmiştir geçiş 1983 yılında gerçekleşmiştir
* exponential büyüme - her 18 ayda 2 ye katlanır

## Ekonomiye Etkisi
* internet tarafından çok büyük bir endüstri kuruldu
  -  ağ donanımı
  - bilgisayarlar
  - yazılım
* şirketler planlama uygulama yönetim ve geliştirme konularında birlikte çalışmalıdırlar

## Karmaşıklık
* Bilgisayar Ağları Karmaşıktır
  - birçok farklı donanım teknelojisi içerir
  - birçok farklı yazılım teknolojisi içerir
  - tüm bunların internet üzerinden bağlanması
* altta yatan bir teori yok
* terminoloji kafa karıştırıcı olabiliyor
  - TLA lar
  - endüstri teknolojiden yararlanarak terminolojiyi yeniden tanımlar ve değştirir
  - yeni terimler her zaman geliştirilir

## Soyutlmalar ve kavramlar
* karmaşıklığı çözmek için soyutlamalara ve kavramlara konsantre olacak
* Örnekler
  - ağ üzerindeki veri tyransferinin detaylarından ziyade ağdaki kablolamanınn nasıl yapıldığına ilgileneceğiz
  - sıkışıklığın tanımı ve kavramını yapıp sıkışıklığın çözme tekniklerini konuşacağız

## Tarihi motivasyon
* İlk bilgisayarlar pahalıydı
  - Geniş Alan
  - Merkezileştirilmiş
* programların koşması oldukça fazla zaman alıyordu
* bilgisayarları istediğimiz her yere koyamıyorduk

## ARPA ( Advanced Research Projects Agency )
* araştırmacıları bilgisayarlara bağlamak için başlangıçta bir proje olarak geliştirildi
* Yeni teknolojilere adapte oldu
  - paket anahtarlama
  - internet working
* Sonuçta pahalı kaynaklara uzaktan erişebilmek için bir sistem elde edilmiş oldu

## Paket Anahtarlama
* Veri küçük ve birbirinden bağımsız parçalar halinde gönderilir
  - kaynak giden mesajları paketlere böler
  - hedef orjinal veriyi yeniden birleştirir
* Her paket bağımsız olarak haraket eder
  - her paket hedefe teslim için gereken veriyi içerir
  - bu paketler farklı yollar izleyebilirler
  - kaybolursa yeniden iletilebilir

## İnternet Üzerinden Çalışma
* birbirinden farklı teknolojileri içeren birçok networkü barındırır
* her durum için tek bir uygun teknoloji yoktur
* internetworking bazen teknolojilerin ağlarını yönlendiricilerle birleştirir
* Sonuçta detayları görülmeyen bir sanal ağı elde edilir. İşte buna İNTERNET denir

************************************************
ARPA'net 1960ların sonunda ortaya çıktı ( 1969 )
Modern internetin Ortaya Çıkış Tarihi 1982 dir
TCP / IP 1978 yılında bulundu
( ÖNEMLİ )
************************************************

## İnternetin gözlenmesi
* 2 tane aracımız var
  - ping = gönderilen mesajların uzak bilgisayar tarafından yargılanmasıdır
  - traceroute = uzaktaki bilgisayara giden yolu bildirir

## PİNG
* uzaktaki bilgisayara gönderilir
* hedef bilgisayar echo paketi ile cevap verir
* yerel bilgisayar aldığı cevabı raporlar

## TRACEROUTE
* bir paket dizisinin hedefe doğru olan yol boyunca gönderilmesidir
  - herbir ardışık paket yol boyunca bir sonraki rooter ı tanımlar
  - genişletilmiş yüzük araması algoritmasını kullanır paketlerin listesini raporlar

### (24 / 02 / 2020) 


## Ağ haberleşmesi

* veri bir noktadan bir noktaya transfer olurken ağın kendisini bu durumdan haberi yoktur 
* Ağın kendisi ne gönderilen datayı üretir ne de gönderilen datadan haberi vcardır
* bütün veri işleme işlemi uygulama pogramı tarafından gerçekleştirilir
  - ağın iki ucundaki kullanıcılar ağı sadece veri alışverişinde (mesaj değiş tokuşunda) bulunmak için kullanılır
  - böyle bir veri tabanı istemcisi merkez veri tabanına erişir
  - istemci (remoor computer -uzak bilgisayar-) tarafındaki uygulama veri tabanı ( server ) bilgisayarındaki koşan uygulamaya bir istek gönderir 
  - Yanlızca bu iki uygulama mesajların formatını ve anlamını anlar

## istemci sunucu mimarisi

* nasıl oluyor da bu kadar büyük bir internet yapısında iki program birbirini bulabiliyor
* internet basit bir mekanizma kullanır 
  - bir uygulama ilk olarak koşar ve iğer uygulamanın ona bağlantı kurmasını bekler
  - ikinci uygulama birinci uygulamanın nerede olduğunu bilmek zorundadır
* işte bu yapı istemi sunucu mimarisi olarak bilinir
* bağlantı için bekleyen program server olarak adlandırılır ve başlangıçta bağlantıyı oluşturacak program ise client olarak isimlendirilir. 
* internette bir konum bilgisayar ve uygulama çiftlerinin kimlikleri yardımı ile belirlenir.
* çiftlerden biri olan bilgisayar serverin koştuğu makinayı tanımlarken çiftin diğer tarafı olan uygulama bir bilgisayarda koşan özel bir uygulama programıdır
* ağ yazılımı her bir ismin ilgili karşılığı olan ikili sayıya otomtik olarak dönüştüren bir yazılım barındırır. insanoğlu bu yapıyı sağlayabilmek amacı ile alfabetik rotasyonları kullanılır
* ağ ikili sistemleri anlayabilir ancak insan anlayamaz


## iletişim paradikması

* çoğu internet uygulaması haberleşirken benzer bir işlem sırasını takip eder
  - sunucu uygulaması başlangıçta koşar ve client dan kendisine bir bağlantı bekler
  - client sunucunun lokasyonunu belirleyerek server a bağlantı kurar ve haberleşme isteğinde bulunur 
  - client ve server mesaj alışverişini gerçekleştirir 
  - veri gönderme işlemini tamamladıktan sonra hem client hem de serverhaberleşmenin bittiğine dair "end of file" isimli bir mesaj göncerilir.

## bir uygulama programı arayüzü örneği
* şimdiye kadar biz iki uygulama programı arasındaki etkileşim haberrleşmeden bahsettik
* şimdi bitaz daha işlerin içeriğine inelim
* bilgisayar bilimcileri uygullama programcısına olanaklar sağayan bir dizi işlevi tanımlamak amacı ile API ( application program interface ) adı verilen terimi kullanır
* bir api her bir işlev için gerekli olan argümanları tanımlar 

 * bit ağ uygulaması global ingetrnet üzerinden çalışan bit uygulama olarak yaratılabilir ki burada adını api olarak  
 * tanımladığımız yüksek eviye fonksiyonlar kullanılır
 * api temel olarak 7 kısımdan oluşur. ( slayt 8 )
 * api ticari uygulamalar iile birilkte çalışabiliecek bir uygulamayı oluşturabilecek kadar yeterlidir.

### ( slayt 2-a yı bitirdik )

### ( 2-z yi atladık )

### ( ch - 3 )

## temel fikir

* veri enerji şeklinde kodlanır ve enerji gönderilir.
* hedefte enerji tekrardan veriye dönüştürülür.
* enerji elektrik, ışık, radyo dalgası , ses vb biçimde olabilir.
* enerjinir her bir formu iletişim için farklı özellikler ve gereksinimler içerir.

## iletişim ortamı

* iletilen enerji iletişim ortamlarının biri üzerinden taşınır
* gönderici veriyi enerji şeklinde kodlar enerji ortam üzerinden gönedririlir
  - veri kodlaması için özel bir donanım gerektirir.
  - iletişim ortamına bağlantı kuracak bir bağlantı da gerektirir.
* ortam bakır cam hava olabilir...

## bakır tel

coaxial tablo performansı artırabilmek için "kalkan" içerir ( ch 3 slayt 6 )


## cam fiber

* ince cam fiberler ışık şeklinde kodlanmış datayı taşır
* plastik kaplama kırılmadan fiberin bükülmesine olanak sağlar
* fiber etkili bir iletişim için iç ortamda ışığın yansıyabilmesi amacı ile oldukça düzgün tasarlanmıştır
* şık veren diot veya lazer fiberin içerisine ışık gönderir
* diğer uçtaki ışık duyarlı alıcı ışığı tekrardan veriye dönüştürür

## radyo dalgaları

* veri adyo dalgaları kullanarak iletilir
* enerji bakır veya camdan ziyade hava içinden gönderilir
* radyo tv ve cep telefonları buna örnek olarak gösterilebilir.
* radyo dalgaları duvarın içerisiden geçebilir.
* uzak mesafe veya kısa mesafe habrleşmede kulllanılabilir
* uuzak mesafe haberleşme uydular yardımı ile gerçekleşir.
* kısa mesafe haberleşmede ise kablosuz bilgisayar ağları örnek olarak verilebilir.

## mikrodalgalar

* yüksek binalara monte edilen antenler aracılığı ile iletilir.

## infrared dalgalar

* infrare ışığı veriyi havanın içinde taşır
* odanınn içerisinde yayılabilir
* yüzeylerden sekebilir ancak duvarlardan geçemez
* gündelik hayatta çok fazla yardımı oluyor

## lazer

* mikrodalgadan daha hızlıdır
* her uçta br lazer gönderici ve bir ışık duyarlı alıcı kullanır
* tipik olarak binalar arasında bir nokgtadan bir noktaya transfer için kullanılır
* hava koşullrından olumsuz etkilenir

* bakır kablo eski ve yaygın bir teknolojidir, sağlan ve ucuzdur fakat maximum transfer hızı sınırlıdır
labaratuar ortamında bakır kablo maximum 95mb/s dir

## fiber:
* yüksek hızlıdır
* elektromanyetik bozulmaya göre daha dayanıklıdır
* daha uzak mesafeleri kapsar
* tek bir fiber kabloya ihtiyaç varü
* daha pahalı vedaha hassas 
* radyo ve mikrodalga fiziksel bir bağlantoya ihtiyaç duymaz
* radyo ve infrared mobil bağlantılar için kullanılabilir
* lazer de fiziksel bir bağlantıya ihtiyaç duymaz


### ktu deki yapıya bakmak gerekirse

* bakır ya da fiber uzun mesafeler için
* binalar arası fiber
* bina içi bakır 


### ( chapter 4 )

## bit bazında veri aktarımı

* veri iletiminin gereksinimleri
  - bitler enerji ile şifrelenir
  - enerji ortam üzerinden iletilir
  - enerji bite dönüştürülür 

* enerji elektrik radio infrared olabilir
* gönderici ve alıcı kodlama tekniği ve iletişim zamanlaması konularında uzlaşmalıdır 

## asenkron iletişim

* asenkronun bir tanımı da :gönderici ve alıcı her bir verinin iletiminde açıkça koordine olmazlar
  - gönderici iletimler arasında keyfi bir süre bekleyebilir.
  - örnek olarak asenktron cihaza klavye verilebilir. fakat gönderilecek veri olmayabilir.
* asenkron iletişimde verinin nerede başlayıp nerede bittiği hakkında açıkça bir bilgi yoktur.

## bitleri gönderirken elektrik akımının kullanılması

* temel fikir şudur ki lojik 1 ve lojik 0 a karşılık gelen voltaj değerlerinin kullanılması.
* yaygın bir kodlama tekniğii lojik 1 için negatif lojik 0 için pozitif voltajı kullanır.
* aşağıdaki şekilde gönderici hatta lojik 0 için pozitif voltaj lojik 1 için pozitif voltaj koyar.


gönderici ilk biti (1 {1 0 0 1}) negatif  kodlar ve alıcıya doğru biti iletir

## iletişim zamanlaması

* kodlama şeması aşağıda birkaç tane cevaplanmamış soru geride bırakmıştır
   - her bir bit için voltaj uzunluğu ne kadar olacak
   - bir sonraki bit ne kadar zaman sonra başlayacak
   - gönderici ve alıcı bu zmanlama konusunda nasıl uzlaşacaklar
* standartlar iletişim sistemlerinin işleyişini belirler
   - farklı satıcılardan elde edilen cihazların hepsi birlikte çalışabilecek şekilde standartlara uymalıdır.
   - Organizasyon örnekleri :
    -> ITU
    -> EIA
    -> IEEE

## RS-232

*Bakır kablolar üzerinden karakterlerin gönderimi için kullanılan standardtır.
*EIA tarafından üretilmiştir.
*Tam adı RS-232-C
*Seri asenkron iletişiim sağlar.
  - seri -> Bitler kodlanır ve herbiri bir birim zamanda iletilir.
  - asenkron -> Karakterler herhangi bir zamanda gönderilebilir ve bitler senkronize değildir.

### (02-03-2020)

#### ( chapter 4 sayfa 9 )

## RS-232 Detayları

* Standartın özellikleri
  - bağlantı 50 feet den düşük olmalı
  - verileri ifade eden voltaj seviyesi +15v ile -15v arasındadır
  - veri, toprak, ve diğer uçların toplamı ile 25 bacaktan oluşur
  - örnek olarak terminal ile modem arasında gönderilecek olan karakterleri belirler
* gönderici kabloyu asla 0v da bırakmaz; hatta veri olmadığında ( idle )  negatif voltaj ( 1 ) koyar

## asenkron karakterlerin tanımlanması
* göndeici yeni bir karakterin başlayacağını 0 göndererek belirtir.
  - alıcı yeni bir karakterin başlayacağını bu şekilde tespit edebilir
  - fazladan 0 bilgisi startbiti olarak adlandırılır
* gönderici hattı boşta bırakmalıdır ki alıcı yeni karakterin başlangıç yerini tesit edebilsin
  - gönderici her bir karakterden sonra bir adet 1 gönderir
  - bu ekstra 1 bitine stop biti denir
* böylece 7 bitle temsil edilen bir karakter için hatta gönderilmesi gereken bir sayısı 9 dur

## RS-232 terminolojisi
 - negatif voltaj 1
 - pozitif voltaj 0

## Zamanlama
* gönderici ve alıcı her bitin zamanlanması noktasında uzlaşmalıdır
* bu uzlaşma transmission rate adını verdiğimiz iiletim hızını seçerek gerçekleştirir
  - bu iletişim hızı bit per second olarak ölçülür
  - start bitinin alıcı tarafından tespiti akabinde arkasından gelecek diğer bitlerin geleceğni gösterir
* donanım genellikle bit hızlarını eşleştirecek şekilde configure edilebilir
  - swifty ayarları
  - yazılım
* oto deteciton

## iletim hızlarının ölçülmesi
* baud rate terimi saniye başına değişen sinyal sayısını ifade eder
* bits per second saniye başına gönderilen bit sayısını ifade eder
* RS-232 de her bir sinyal değişimi 1 bite karşılık gelir bu sebeple baud rate ile bits per second birbirine eşittir
* eğer her bir sinyal değişimi birden fazla bite karşılık gelirse bu durumda bits per second baud rate den büyük olduğu anlamına gelir

## Çerçeveleme
* start ve stop bitleri her bir karakterin çerçevesini gösterir
* eğer gmnderici ve alıcı farklı hızlar kullanıyorsa stop biti alıcı tarafında beklenilen zamanda almaz
* bu problem çerçeveleme hatası veya framming error olarak adlandırılır
* bu durumda RS-232 cihazları BREAK olarak adlandırılan çerçeveleme hatası mesajı gönderebilir

## Çift-yönlü iletişim
* her iki terminal arasında eş zamanlı olarak veri gönderilebilmesi işlemine full-dublex iletişim denir 
* bu yapı her bir yön için ayrı bir kablo gerektirir

## RS-232 bağlantı stndartları
* RS-232 ye ait 25 tane pinin belirttiği ifadeler aşağıdadır
  - pin 2 alıcı olarak kullanılır
  - pin 3 gönderici
  - pin 4 gönderilmeye hazır veri için
  - pin 5 gönderilen verinin temizlenmesi için
  - pin 7 topraklama hattı

## 2-3 değişim
* alıcı ve gönderici tarafında 2 ve 3 pinlerini birbirine bağlamak için çapraz bağlama kullanılmalıdır
* RS-232 modem tarafında pin 2 üzerinden gönderim yapıp pin 3 üzerinden alım işlemini gerçekleştirirken bilgisayar tarafında pin 3 üzerinden gönderim yaparken pin 2 üzerinden alım işlemini gerçekleştirir.
* bu durumda aynı bacaklarda ( pin 2 -> pin2 , pin 3 -> pin -> 3 ) zıt kutuplar eşleştiğinde çapraz bağlantıya ( swap ) gerek yoktur.

## gerçek donanımın limitleri
* kablodaki dalga formu aşağıdaki şekilde ki gibi görülür
* daha uzun kablolarda harici gürültüler sinyal görünümünün daha da bozulmasına sebep olur
* RS-232 standardı göndericinin üretmesi gereken dalga formunun ne kadar kesinlikte olacağını, alıcı tarafta dalga formunda nen kadar tolerans olması gerektiğini de belirler 

## Donanım bant genişliği
* genellikle k farklı durum içeren sistem için 2Blog2K
* pratikte gürültü iletilecek maximum veri hızı 


## Uzak mesafe haberleşme
* RS-232 tarafından kullanılarak kodlama her durumda çalışmaz
  - uzak mesafe haberleşme
  - telefon gibi var olan sistemleri kullanan yapılar
* bu sebeple farklı kodlama stratejileri gerekir

## uzak mesafelere sinyal gönderimi
* elektrik akımı kablo üzerinde ilerlerken güç kaybeder
* kayıp siyal verinin doğru br şekilde dönüştürülmesini engellleyebilir
* sinyal kaybı durumu RS-232 nin uzak mesafe haberleşmede kullanılmasını olanaksız kılar

## Sürekli salınımlı sinyal
* elektik akımından daha uzak noktalara ulaşabilir
* uzak mesafe haberleşme carrier ( taşıyıcı ) adını verdiğimiz bir sinyal üzerinden gerçekleştirilir
* taşıyıcının dalga formu aşağıdaki şekildeki gibidir
* taşıyıcı RS-232 sinyalinden sinyaline göre çook daha uzak mesafelerden tespit edilebilir. 

## Bir taşıyıcı ile birlikte veri kodlanması
* iletimde verinin kodlanması için kullanılan modifikasyon tekniğine modilasyon denir
* benzer fikir radyo ve televizyon sistemlerinde kullanılır
* Taşıyıcı modilasyonu bütün ortam tipleriye kullanılır. Ortamlara örnek olarak bakır fiber radyo imfrared ve lazer verilebilir.

## Modülasyon teknikleri
* Genlik modilasyonu güç veya taşıyıcının genliği (genlik ne kadar fazla ise sinyal o kadar güçlüdür) veriyi kodlamak için kullanılır
* frekans modulation, taşıyıcının frekansı veriyi kodlamak için kullanılır
/*
	am ile fm arasındaki farklar ve avantajlar
	am daha güçlü dalgalar her alandan çekim gücü
	fm daha güçsüz ama daha kaliteli ses
*/
* Faz kaymalı modülasyon, zaman içerisindeki değişiklikler veya faz kaymaları ile verilerin kodlanması
// frekans yükseldikçe kalite yükselir
* her bir faz kayması birden fazla biti taşımak için kullanabilir örnek olarak olası faz kaymasını 2 bit ile kodlayabiiliriz:
  - 00 - Kayma Yok
  - 01 - 1/4 oranında kayma
  - 10 - 1/2 oranında kayma
  - 11 - 3/4 oranında kayma
* böylece her bir faz kayması 2 bit taşınmış olur
* bu durumda yine veri hızı baud rate nin 2 katıdır

## veri iletimi için donanım
* modülatör veri bitlerini modüle edilmiş taşıyıcı şeklinde kodlar ( veri bitlerini karşılık gelecek şekilde taşıyıcıya dönüştürür )
* demodulatör taşıyıcıdan bitleri dönüştürür
* veri iletimi kaynakta modulatör hedefte demodülatörü gerektirir

## çift yönlü iletişim
* Çoğu sistem eş zamanlı çift yönlü ( full-duplex ) bu sebeple her iki uç noktada da hem modülatör hem de demodülatörü gerektirir.
* uzak mesafe haberleşme 4 kablolu çevirim olarak adlandırılır.
* modulatör ev demodülatör modem adı verilen bir cihaz ierisinde birleştirilmiştir
### (09 / 03 / 2020)

## optik radyo ve dailup modemler

* özelleşmiş veri devrelerine (kablo modem) ek olarak diğer ortamlarda da kullanılan modemler de vardır.
* veri kodlaması için modülasyon tekniğini kullanan dönüştürücülerin kodlanması ve çözülmesinin özel bir formudur.
	- Cam( fiber ) - veri modüle edilmiş ışık şeklinde kodlanır
	- radyo - veri modüle edilmişradyo sinyali şeklinde kodlanır
	- Dailup - veri modüle edilmiş ses şeklinde kodlanır
* Dailup ( 56k modemler ) modemler sıradan telefon hattına bağlanırlar.


evdeki bilgisayar -- rs232 -- modem --   -- modem -- rs232 -- evdeki bilgisayar 
( rs232 kısa mesafeli haberleşmede kullanılan sistem )

## Dailup modemler
* veri gönderme için bir devredir
* Bu devre telefon işleyişini temsil eder
	- ahizeyi kaldırma
	- çevirme
	- hatta bekleme 
	- çevir sesinin tespiti
	
* tekbir ses kanalı üzerinde çift yönlü iletişim vardır
	- her bir yön için farklı taşıyıcı frekanslarını kullanarak
* Gürültüyü filtreler

## Dailup modemlerin işleyişi
* Alıcı modem cevap modunda aramayı bekler
* diğer modemler (gönderici - arayan):
	- ahizeyi kaldırma işlemini taklit eder
	- dial tone gelmesini bekliyor
	- çevirilen numaraya verinin gönderimi
* cevap modundaki modem
	- Aramayı tespit eder
	- Ahizeyi kaldırmayı simüle eder
	- taşıyıcı gönderir
* Modem aranıyor:
    - Operatör gönderir
* veri transferi

## taşıyıcı frekansları ve çoğullama
* veri birden çok sinyalle aynı ortamda gürültü olmadan taşınabilir. 
	- bu bize eş zamanlı olarak çoklu veri akışı olanağı sağlar
	- Dailup modemler tek bir ses kanal üzerinde çift yönlü iletişim gerçekleştirebilirler
* örnek - aynı hava ortamı içerisinde çoklu tv yayınları
* her bir ayrı sinyal bir channel( kanal ) olarak adlandırılır.

## Çoğullama
* bir ortam üzerinde birden çok sinyalin taşınması işlemi multiplexing olarak adlandırılır

birden çok kaynak - pultiplexor denilen bir araca bağlanır bu aygıt bir kanal yardımı ile demultiplexor a bağlanır ve bu araca da kaynaklar bağlanır

* frekans bölütlü çoğullama farklı taşıyıcı frekansları kullanarak çoğullama işlemini gerçekleştirir
* alıcı belirli bir frekansa ait sesi (tune) alabilir ve o kanal için veriyi elde edebilir.
	- Frekanslar gürültüden kaçınmak amacı ile ayrılmak zorundadır
	- farklı frekanslarla birden çok sinyalin taşınabildiği ortamlarda oldukça yararlıdır. (sonuç olarak yüksek bant genişliğine ihtiyacımız vardır)

## Spektrum Çoğullama
* çoklu taşıyıcıları kullanır
* tekli veri akışı parçalanır ve farklı frekanslar üzerinden gönderilir
* gürültünün üstesinden gelmek veya hat dinlemesi gibi olası durumlardan kurtulmak için kullanılabilir

## Zaman bölütlü çoğullama
* zaman bölütlü çoğullama tek bir taşıyıcı kullanır ve veriyi sıralı olarak gönderir
* gönderici ve alıcı çifti tek bir kanalı paylaşırlar.
* birçok bilgisayar ağı paylaşımlı ortamı kullanır

# ÖZET
* uzak mesafe haberleşme güvenilir iletişim için taşıyıcı ve modülasyon tekniğini kullanır
* modulatör veriyi kodlar ve demodulatör çözer
* genlik frekans veya fazkaymalı teknikler kullanılabilir
* çoklu gönderici alıcı çifti tek bir ortamı paylaşmak için multiplexingi kullanır.

### (chapter 6)

## Paylaşımlı iletişim ortamı
* Çoğu network bilgisayarları birbirine bağlayan paylaşımlı bir ortamı kullanır 
* fakat birim zamanda yanlızca bir kaynak veri transferi yapabilir.

## Paketler
* Çoğu network iletişim için veriyi paket adı verilen küçük bloklara böler 
* her paket birbirinden bağımsız şekilde gönderilir
* böyle networkler paket networkler veya paket anahtarlı networkler olarak adlandırılır

## Motivasyon
* Koordinasyon- Gönderici ve alıcı verinin doğru alınıp alınmadığına karar vermelidir.
* Kaynak paylaşımı bilgisayarların network altyapısını paylaşımlı olarak kullanmasına olanak sağlar.
* Networkler adil kullanımı uygularlar. Herbir bilgisayar birim zamanda yalnızca bir paket gönderebilir.

## Dedicated Network Access (adil kullanımda kastı ne )
* 5 MB lık bir dosyayı 56 kbbit/persecond kapasiteli bir modemden bir network boyunca (uzerinden) yaklaşık 12 dk da gönderir.
* (5x10^6 bytes) * (8 bits) / (60 secs/min) * (56x10^3 bit/second) = 11.9 dk 11.54 sn
* Bu hesap sonucunda diğer bütün bilgisayarlar başka bir transfere başlamadan önce 12dk beklemek zorunda kalacaklar.

## Paket Anahtarlamalı Erişim
* Eğer bir dosya paketlere ayrıştırılırsa diğer bilgisayarlar bütün dosyadan ziyade yalnızca paketin gönderilmesini beklemek zorunda kalacaktır.
* Önceki örneğimizden kaynak dosyamızın 1000 Byte lık paketlere bölündüğünü varsayalım.
* Herbir paket gönderim için 0.2 saniyeden az bir zaman alacaktır.
* (1000 bytes) * (8 bit ) / (56x10^3 bits/second) = 0.143 second Saniyenin sekizde biri yaklaşık olarak 
* Diğer bilgisayarlar transfere başlamadan önce yalnızca 0.143 saniye beklemek zorundadır.
* NOT:
 -> Eğer her iki dosyanında 5MB olduğunu düşünürsek herbirinin transfer edilmesi için gereken süre 24 dk olacaktır.
 -> Fakat eğer ikinci dosya yalnızca 10KB uzunluğunda ise ikinci dosya yalnızca 2.8 saniyede transfer edilebilecek ve 5MB lık dosya yine yaklaşık olarak 12 dk zaman alacaktır.

## Zaman bölütlemeli çoğullama
* Verinin küçük paketlere bölünmesi zaman paylaşımını çoğullamaya olanak sağlar
* her paket kaynaktan ayrıdır ve ortak bir iletişim kanalı multiplexor üzerinden ortak bir iletişim kanalına aktarılır.
* hedefte paket demultiplexor üzerinden hedefe aktarılır. 

## Zaman bölütlemeli çoğullama örnek
birim zamanda bir bilgisayar çifti haberleşme linkini kullanarak veri alışverişi yapar

## paketler ve frame'ler
* paket terimi verinin küçük bir bloğununa karşılık gelir
* her bir donanım teknolojisi farklı paket formatı kullanır
* frame veya hardwareframe belirli bir donanım teknolojisi üzerindeki belirli bir yapıya sahip paketi gösterir

## frame Formatları
* veriye ait framenin başlangıcını ve bitişini belirtmek için standart bir format tanımlamamıza ihtiyaç vardır.
* header ve trailer ifadeleri frame için kullanılırlar

## frame standartlarının tanımlanması
* çerçeveleme için iki tane kullanılmayan veri değeri seçilebilir
* örnek-
	eğer veriniz yazılabilir ascii ifadeleri ile sınırlı ise bu durumda
	-> 'startd of header' ( soh )
	-> 'end of text' ( eot )
* gönderici bilgisayar öncelikle soh ifadesini gönderir ardından datayı gönderir ve son olarak da eot ifadesini gönderir.
* alıcı bilgisayar soh ifadesini yorumlar ve gözardı eder verileri buffer da depolar ve eot ifadesini de yorumlayıp göz ardı eder

## frame format
soh - block data in frame - eot

## paket çerçeveleme
* gönderici alıcıya birim zamanda bir karakter gönderir

## uygulamada çerçeveleme
* extra yük oluşturur- soh ve eot un iletilmesi zaman  alırfakat herhangi bir veri taşımazlar
* iletişim problemleri barındırır
	-> kayıp eot ifadesi gönderici bilgisyarın arızalandığına işaret eder
	-> kayıp soh ifadesi alıcı bilgisayarın mesajın başını kaçırdığına ifader 
	-> bu tür kötü frameler göz ardı edilir
 
## Belirli bir veri transferi
* sisteminizin çerçeveleme için 2 tane özel karakter barındıramadığını var sayalım
* örnek 8 bitlik ikili bir verinin transferi
* bu durumda verinin parçaları olan soh ve eot çerçeveleme verisi olacak şekilde yanlış yorumlanacaklardır
* gönderici ve alıcı transferin düzgün şekilde yapılabilmesi için özel karakterlerin kodlanması noktasında uzlaşmalıdır.

## Veri istiflemesi
* ayrılmış byte ların kodlanması için eklenen ekstra veri nıktasında kullanılan iki teknik bit stuffing ile byte stuffing dir
* byte stuffing her bir ayrılmış byte ın iki tane ayrılmamış byte a dönüştürür.
örnek - esc yi örnek olarak kullanabiliriz, arkasından da soh için x i eot için y yi kullanacağız ve unreserved esc yi belirtmek için escnin arkasından z yi kullanacak

## byte stuffing
* gönderici her bir ayrılmış byte ın uygun kodlanmış byte çiftlerine dönüştürür.
* alıcı byte çiftlerini yorumlar ve kodlanmış byte ı buffer a depolar
* veri halen soh ve eot tarafından çerçevelenmiş durumdadır

## byte stuffing örneği
* alıcı esc ve y yi veri içerisindeki eot karakterine karşılık gelecek şekilde yorumlar ve sonrasında alıcı alınan veriyi kaydeder

## iletişim hataları
* harici elektromanyetik sinyaller veri teslimatında bozuntuya sebep olabilir
	-> veri düzgün bir şekilde alınamayabilir
	-> veri kaybolabilir
	-> istenmeyen veriler üretilebilir
* bu problemlerden herhangibiri iletişim hatası olarak adlandırılır

## Hata tespiti ve düzeltme
* hata tespiti - hata tespiti için ek bir bilgi gönderilir ve böylece doğru olmayann veri tespit edilip reddedilir(gözardı).
* hata düzeltme - hata düzeltme için ek bir bilgi gönderilir ve böylece doğru olmayan veri düzeltilebilir ve kabul edilebilir

### (ue1 - 09 / 04 / 2020 )

## iletim hataları
* harici bir elektromanytetik sinyal verinin teslimatının yanlış olmasına sebep olabilir
  - veri kaybolabilir
  - veri düzgünce alınamayabilir
  - istenmeyen veriler alınabilir
* bu problemlerden her biri iletişim problemleri olarak adlandırılır.

## hata tespiti ve düzeltme
* yanlış olan verinin tespiti ve reddedilmesini sağlayabilmek için ek bir bilgi gönderilir
* hata düzeltme kısmında ise yanlış olan verinin düzeltilip kabul edilebilmesi amacı ile ek bir bilgi gönderilir

## parity (italic) checking

* verimizin içerisinde bulunan lojik 1 lerin sayısını gösterir
  - even parity - veri içerisindeki 1 lerin sayısının çift olmasına dayalı sistem
  - odd parity - veri içerisindeki 1lerin sayısının tek olmasına dayalı sistem
* parity biti ekstra bir bittir ve veri ile birlikte gönderilen bittir ve sonuç olarakk bu even veya odd paritiden hangisinin kullanılacağının önceden belirlenmesi gerekiyor
  - örnek even parity de uzlaşılmız ise ve veri örneğin 10010001 ise parity bilgisi olarak 1 eklenir
  - odd parity seçilmiş ise 10010111 ise parity bit 0 dır

## parity ve hata tespiti
* gürültü veya diğer parazitler bizi hataya götürebilir bu veri içerisindeki btlerden biri 0 dan 1 e veya 1 den 0a dönüşebilir 
* sonuçta parity bilgisi yanlış olacaktır.
  - orjinal veri (10010001 + 1) even parity e göre
  - incorrect data (10110001 + 1) (odd parity)
* gönderici ve alıcı başlangıçta hangi parity nin kullanılacağı konusunda anlaşmalıdır
* eğer alınan datada yanlış parity biti varsa alıcı verideki hatayı tespit eder

## Limitations to parity checking
* parity yanlızca tek sayıda bitlerin değişimine bağlı ortaya çıkacak hataları tespit edebilir
  - orjinal data (10010001 + 1 evenparity)
  - incorrect data (10110011 + 1 evenparity!)
* parity bilgisi (teniği) bir bite dayalı hataları tespit etme noktasında kulllanılır

## alternatif hata tespit şemaları
* çoklu bit hatalarını tespit etme noktasında kullanılır
  - veya bunlardan bazıları fazlalık bilgi vasıtası ile hataları düzeltebilir
* chechsum ve crc yaygın kullanılan 2 tekniktir

## checksum
* mesajın içerisindeki verileri bir int dizisi şeklinde düşünüp bunların toplamını baz alır
* bu int yapılar 8 16 veya 32 bitlik olabilir
* bu işlemleri yaparken genellikle 1 e tümleme işlemini kullanılır

## checksum hesaplamanın uygulanması 
* uygulanması basittir yanlızca toplama kullnılır
* 16 bitlik checksum ın en hızlı uygulamaları 32 bitlik aritmetik işlemleri kullanır ve en sonunda eldeyi ekler
* bu hesaplama işlemini döngülleri açarak ve benzer optimizasyon teknikleri kullnarak hızlandıra bilirsiniz

## checksum limitleri
* bütün hataları yakalayamaz (özetle yapılan işlem toplama sonucu çıkan verilerin eşit olup olmadığını kontrol etmek ancak farklı değerler ile aynı sonuca da ulaşılabildiğinden herzaman kullanışlı değildir )

## Cyclic redundancy checks (CRC tekniği)
* mesajın içerisindeki bir fonksiyonun kat sayıları olarak düşünün 
* donra bu katsayılardan oluşan veriyi bilinen bir fonksiyona bölün 
* son kalan kısmı da crc olarak gönderin

## Hata tespiti ve çerçeveler
* hata tespiti tipik olarak her bir frame için gerçekleştirilir
* eğer frame de bir hata varsa alıcı tarafın bu frame yi göz ardı etmesi ile sonuçlanır 
* örneğin crc bilgisi frame içerisinde veriye bağlı olarak hesaplandıktan sonra gönderilir

# özet
* bilgisayar ağları veriyi paketlere böler
  - bu kısımda kaynak paylaşımı
  - adil kullanım vardır
* donanım çerçeveleri vardı ve bunlar özelleşmiş donanıma göre belirlenir
* her bir frame nin spesisifik formatıı vardır bu da frame nin nerede başlayıp nerede bittiğini gösterir
* hata tespiti ve düzeltilmesi iletişim hatalarının tespiti ve düzeltilmesi noktsında kullanılabilir.

### (ue2 - 10 / 04 / 2020)

### (chapter 7)

# Lan Teknolojileri yerel ağ teknolojileri

## doğrudan noktadan noktaya haberleşme
* bilgisayarlar bir iletişim kanalı üzerinden birbirine bağlanır bu kanal tam olarak 2 bilgisayarı birbirine bağlar
* bu tür ağlara noktadan noktadaya veya mesh ağlar denir
* noktadan noktaya haberleşme bize haberleşme donanımında veya paket formatında bize esneklik sağlar
* ilk gelen özelliklerden biri güvenlik ve gizlilik çünkü iletişim hattı paylaşılmadığından hat doğrudan iki bilgisayar arasındadır

 -> noktadan noktaya network bağlantılantı sayısı N adet bilgisayar için ( n * (n - 1) ) / 2 dir örneğin 3 bilgisayar için 3 bağlantı

 -> her eklenen yeni bilgisayar n - 1 adet bağlantı ekler

noktadan noktaya haberleşmenin dezavantaşı bilgisayar sayısının artması ile oluşan kablo ve yönetim problemleri sonucunda
1960 ların sonuda 1970 lerin başında yerel ağ teknolojisi lan teknolojisi geliştirildi

* bilgisayarlar arasında paylaşımlı bağlantılar üzerinden toplam bağlantı sayısının azaltılması
* en nihayetinde bilgisayarlar TDM ye dönüştürüldü ( TDM = zaman paylaşımlı çoğullama)
  - bu sistemler senkronizasyonun kulllanılması aşamasında çeşitli teknolojiler kullanıyor

## Lan teknolojilerinin büyümesi
* lan teknolojileri bağlantıların sayısını azaltarak maliyeti düşürdüler 
* Fakat yerel ağa bağlı bilgisayarlar ortak ağın kullanılması konusunda birbirleri ile yarışmalıdır
* genelde yerel haberleşme yerel alan ağına özgüdür
* uzak mesafe haberleşmede point to pont kullanılır arka planda 
  - smds
  - atm  yapılarını kullanıyoruz

## referans Yerellik ilkesi

* bilgisayarlar arasındaki iletişim modellerini tahmin etmemize yardımcı olur
  - mekansal , konumsal , uzaysal birbirlerine yakın bulunan bilgisayarların birbirleri ile haberleşme olanakları daha fazladır
  - zamansal yerellik bilgisayarların haberleştiği bilgisayarlar ile tekrar tekarr haberleşme olasılıkları daha fazladır

* Lanlar fiziksel yerellik ilkesi bakımından etkindirler zamansal yerellik açıından ise bu durumda hangi bilgisayarların lan da olması gerektiğine bakılabilir

## Lan Topolojileri
* Netvorklerin şekillerine göre sınıflandırılmasıdır
* 3 populer çeşidi vardır
  - star
  - ring
  - bus

## yıldız topolojisi
* bütün bilgisayarlar merkez noktaya bağlanırlar
* yıldız topolojisinde merkezine çoğunlukla hab olarak adlandırılır
* genellikle bağlantı kaploları bilgisayarlara benzer şekilde paraleldir. (cat 5 / 6 kablonun bilgisayardaki karşılıgı rj45 dir)

## Yüzük halta tapolojisi
* bilgisayarlar kapalı bir döngü üzerinden birbirleirne bağlanırlar
* birinci bilgisayar veriyi 2.ye aktarır 2. 3. ye derken döngü bu şekilde ilerler
* bilgisayar ile halka arasında küçük bir bağlantı kablosu var
* yüzük bağlantıarı ofisler içerisinde bulunan soketler yardımıyla bağlantı kablosuyla ofisler arasında da paylaştırılabilir
(yüzük tapolojisinde 2 kalka vardır dış halka veri gönderilirken kullanılan kalkadır iç halka ise arıza durumu dışında iç halka kullanılmaz (herhangi bir arıza durumunda bir kopma durumunda kopan bilgisarın yanındaki bilgisayarlar iç halka yardımı ile kapalı döngüyü sağlaralar))

## Bus topolojisi
* tekli bir kablo üzerinden bütün bilgisayarlar bağlanır
* ortak hatta her bir bilgisayarın bağlanmasını sağlayan bir connector vardır
* bilgisayarlar birim zamanda yalnızca bir bilgisayarın veri gönderebilmesini sağlayacak şekilde senkronize olmalıdır

## neden çoklu topolojiler var
* yüzük topolojisinin senkronizasyonu kolaydır ancak kablo kesildiğinde devre dışı kalabilir
* yıldızın yönetimi basittir ve daha dayanıklıdır kopan kablo yalnızca o bilgisayar ile ilgilidir ancak çok daha fazla kabloya ihtiyaç vardır
* çok da az bir kablo var kablo koptuğunda sistem devre dışı kalacaktır

## Ethernet
* lan teknolojisi olarak oldukça yaygın olarak kullanılır
  - Xerox parc tarafından 1970 lerde icat ediliyor
  - standartları xerox intel ve digital tarafından belirleniyor
  - IEEE tarafından yönetiliyor - formatlaını voltaj değerlerini kablo uzunluğunu
* bus tapalojisini kullanır
  - tekli bir coax kablo var bu kablolara ether denir
  - birden çok bilgisayarda sisteme bağlanabiliyor
* bir ethernet kablosu çoğunlukla segment olrak adlandırılır
  - uzunluğu yaklaşık 500 mt civarındadır
  - bağlantılar arasında min 3m mesafe olmalıdır
* ethernet hızları
  - başlangıçta 3mbps
  - normal hız 10mbps
  - hızlı internet 100mbps
  - 1gbps hızları kadar çıkabiliyor

## Ethernet işleyişi
* birim zamanda yanlızca bir ilgisayar iletimde bulunur
* sinyal modüle edilmiş bir taşıyıcıdır ve göndericiden gelen bu sinyal segmentin her iki yönü boyunca da yayılır

## CSMA
* bilgisayarlar kablolu iletimde bulunduğunda herhangi bir merkezi kontrol mekanizması yoktur
bu sebeple birden çok bağlı bilgisayarlar arasında iletişimi koordine etmek amacı ile ethernet csma kullanır
  - birden çok bilgisayara sisteme bağlıdır ve herhangi biri gönderici olabilir
  - carrier sence - veri göndermek isteyen bilgisayarın veri göndermeye başlamadan önce taşıyıcı için kabloyu test etmesidir

## Collesion detection (CD)
* csma ile bile yine de iki bilgisayar eş zamanlı olarak transfere geçebilir
  - her iki bilgisayarda aynı zamanda kabloyu test ettiler her ikiside kaloyu boş gördü ve transfer işlemine başladılar
* her iki bilgisayardan gelen sinyaller birbiri ile çarpışıp bozulmalara sebep olacaktır
* bu üst üste binen framelere collision denir 
  - bu işlemin donanıma herhangi bir zararı yok 

## Ethernet CD
* ethernet arayüzleri iletimi tespit edebilmek için bir donanım barındırırlar 
  - gien sinyali inceliyorlar
  - Bozuk olan sinyal çakışma olarak yorumlanır
* çakışmanın tespit edilmesinden sonra bilgisayar veri göndermeyi durdurur
* ethernet teknolojisi bu iletimde senkronizasyonu sağlamak amacı ile CSMA/CD birlikte kullanır

## çakışmadan geri dönme
* çakışmayı tespit eden bilgisayar diğer bütün arayüzlere çakışmayı tespit edebilmelerini sağlamak amacı ile özel bir sinyal gönderir
* akabinde bilgisayar daha sonra tekrardan transfere başlamadna önce tekrardan kablonun boş olup olmadığını beklemeye başlıyor 
  - her iki bilgisayar aynı uzunlukta tekrardan beklerse yine çakışma oluşacak
  - bunun önüne geçmek için standartlar maximum bir gecikme süresi belirleniyor ve çakışmaya uğrayan bilgisayarlar maximum süreden daha düşük olacak sürede bir random değer belirliyorlar
* random değer kadar beklenildikten sonra bilgisayar olası alt çakışmalardan sakınmak amacı ile tekrardan carrier science kullanıyor
  - böylece daha düşük bekleme süresine sahip olan bilgisayar transfer işlemine başlıyor
  - diğer bilgisayarlar işlem bittikten sonra kendi transfer işlemlerini gerçekleştiriyorlar

### (ue3 - 16 / 04 / 2020)

## Üstel geri çekilme
* rastgele gecikmelerde bile çarpışmalar meydana gelebilir
* özellikle meşgul segmentlerde
* Bilgisayarlar bekledikler gecikme süresini her bir alt çarpışmada iki katına çıkarırlar
* koleksiyon dizilerinin olasılığını artırır

## wireless lan
* 900mhz radyo sinyaleri kullanılır
* veri hızı 2mbps 
* paylaşımlı ortam olarak coax kablo yerine radyo sinyalleri kullanılır

## wireless deki bağlantı limitleri
* kablolu lan yani ethernetin aksine wireless de bütün katılımcılar birbirleriile haberleşemeyebilirler
  - düşük sinyal gücü
  - yayılımın duvarlar tarafından engellenmesi
* buradaki sistemde CD yapısını kullanamazsınız çünkü bütün katılımcılar birbirlerini duyamayabilir

## CSMA / CA
* wiewlwss ağlar çarpışma tespiti yerine çarğışmadan sakınma algoritmasını kullanırlar
  - gönderici bilgisayar alıcıya çok küçük bir mesaj yollar 
  - alıcı da gönderici için küçük bir slot ayırdığını gösteren mesaj geri döndürür
* bu alıcıdan gelen mesj olası bütün gönderici istasyonlara broadcast yapar (broadcast = bütün herkese yayın yapmak)

## Collesion
* alıcı eş zamanlı istekler alabilir
  - alıcı eşzamanlı istekler alabilir
  - her iki istek kaybedilir
  - hiçbir gönderici için herhangi bir slot ayrımında bulunmaz

* Alıcı çok yakın aralıklar ile istek alabilir
  - alıcı birini seçer
  - seçilen göndericiye mesaj gönderilir
  - seçilmeyen gönderici isteği devre dışşı kaldığı için tekrardan istekte bulunur

## LocalTalk
* lan teknolojisi bus topolojisini kullanır
* macintosh bilgisayarlarda arayüz olarak sağlanır
nispeten hızı 230.4 kbps ile düşük hızda idi
* macintosh larda ücretsizdi ve kurulumu ve kullanımı kolaydı
* CSMA / CD kullanır

## Token ring
* günümüzde hala aktif olarak kullanılan teknoloji
* yüzük tapolojisini kullanan bir lan teknolojisidir yüzüğe erişimlerde senkronizasyonu sağlayabilmek için token geçişi kullanır
* ring kendisi tekil ve paylaşımlı bir ortamdır
* bu halkadan oluşan bitler diğer bilgisayarları geçerek hedef bilgisayarda kopyalanır
* bu donanımda token geçişine uygun şekilde dizayn edilmesi lazım ve herhangi bir bilgisayarın kapanma durumuna bağlı olarak dizayn edilmesi gerekir

## token kullanımı
* bir bilgisayar veri iletimi isteğinde bulunduğunda token ı beklemelidir
* transfer işlemi bittikten sonra bilgisayar tokeni tekrardan ringe verir
* böylece veri göndermek isteyen bir sonraki bilgisayar da tokeni yakalar ve transfer işlemini başlatır

## token ve senkkronizasyonu
* sistemde yanlızca 1 token olduğundan birim zamanda yanlızca 1 bilgisayar bilgisayar bilgi gönderebilir 
  - token özel bir frame dir bu data kısmında değildir 
  - donanım bu tokenı yeniden üretecek şekilde dizayn edilmişte olmalıdır
* token her bir bilgisayara bir frame gönderme izni verir
  - eğer bu sırada veri göndermeye hazır birden çok bilgisayar varsa bu bilgisayarlar arasında roundrobin algoritması kullanır
  - eğer veri göndermeye hzır herhangi bir bilgisayar yoksa token ring üzerinde tur atar

### (ue4 - 04 / 17 / 2020)

## IBM token ring
* çok yaygın olarak kullanılır
* orjinali 4mbps, günümüzde 16mbps
* bilgisayar ile yüzük tapolojisi arasında özel bir bağlantı kablosu kullanır

## FDDI
* FDDI birbaşka yüzük tapolojisidir
  - istasyonlar arasında fiboroptik kullanılır
  - veriyi 100mbps hız ile iletir
* iki fiber hat kullanılır

## FDDI ve güvenilirlik
* yüzük tapolijisini kullanan teknoloji
* zıt yönlü iletişim için halkalar kullanır 
* istasyon kaybı veya fiberin kaybında kalan istasyonlar yedek hat üzerinden tekrardan döngüyü sağlayacak şekilde yapılandırılırlar
 
## ATM - yıldız ağı
* asenkron transfer mod teknolojisi elektronik paket anahtarlarından oluşur, bilgisayarlar da kablo ile bu yapıya bağlanırlar
* ATM switch leri yıldız tapolijisi içerisinde bir hub a abağlanacak şekilde atm switch i oluşturur
* bilgisayarlar göndericiden veriyi doğrudan bir noktadan bir noktaya bağlantı şeklinde alarak switch üzerinden hedefe yönlendirilirler

## ATM Detayları
* veri hızı 100mbps üzerindedir
* bilgisayarlar switch e bağlanmak için fiberoptic kullanılır
* her bir bağlantı için 2 fiber ağlantı kullanılır

# özetle
* lan teknolojilerini paylaşımlı iletişim ortamı olarak kısa mesafeler üzerindenn birden çok bilgisayarı birbirine bağlamak için kullanıdık
* gönderici bilgisayar iletişim ortamının kullanımı noktasında seçkindir; bilgisayarlar iletişim için senkronize olmalı ve mevcut kapasiteyi paylaşmalıdır
* LAN Topologies;
  - Star
  - Ring
  - Bus
* Lan technologies
  - ethernet
  - wireless
  - localtalk
  - localtalk
  - IBM token Ring
  - FDDI
  - ATM

### ( chapter 8 )

# Doannım adresleme ve frame tiplerinin tanımlanması

## GİRİŞ
* bir önceki chapter da lan teknolojisine bağlı olarak bilgisayarlar arasında bağlantıyı sağlayan teknikleri görmüştük
* bizim bunların haricinde bu noktada ihtiyacımız olan şey mesajın lan ortamı üzerinden tekli ve belirli spesifik bir hedef bilgisayara iletilmesi
* gönderici bilgisayar bir donanım adresi kullanır ki bu donanım adresi verinin veya framenin teslim edilmesi gereken bilgisayarı içerir
* veriyi gönderen bilgisayar framenin içerisinde taşıann verinin tipini de tanımlar

## Hedefin Belirlenmesi
* ortak bir ağ üzerinden paylaşılan veri bütün istasyonlara erişir - bütün lan topolojileri için geçerlidir
* aynı donanımı framenin teslimini kabul eder ve ortamdan frameyi alır
* Ama çoğu uygulama başka bilgisayar üzerindeki belirli bir uygulamaya veri teslim etmek ister

## Donanım adresleme
* çoğğu network teknolojisi bir donanım adresleme şemasına sahip ve bu şema ağ üzerindeki istasyonları tanımlar
* her bir istasyona sayısal bir donanım adresi veya fiziksel adres atanır
* gönderici iletilen her bir framenin içerisinde bu donanım adresini koyar
* framenin içerisindeki tanımlanan istasyon yanlızca framenin kopyasını alır
* bunun haricinde birçok lan teknolojisi yine framenin içerisinde göndericinin donanım adresini de barındırır

## Lan donanımı ve paket filtreleme
* lan üzeridnen framelerin alınmasını veya gönderilmesine sağlar bu da arka planda işlemci ve bellekle ilgilidir
* işlemci ve bellekte gidecek olan datayı üretir veya gelen dataları işler
* Lan arayüzü veri alınırken veya gönderilirken bunun ile ilgili veriyi taşıyan framenin bütün detaylarına sahiptir
  - bu data çerçevesine (frame) donanım adreslerini ekler, framenin en son kısmında bulunan hata tespit kodlarını ekler (crc) bunları giden frameye ekler
  - DMA kullanabilir , çerçeve verisini doğrudan ana bellekten almak amacı ile kullanaabilir
  - gönderme sırasında erişm kurallarına uyar
  - gelen frameler üzerinden hata tespit kodlarını inceler
  - DMA yi veriyi doğrudan bellek içerisine transfer etmek için de kullanılabilir
  - gelen framenin hedef adres kontrolü
    -  eğrr gelen frame üzerindeki hedef adres yerel istasyonun adresi ile eşleşir ise framenin bir kopyası bağlı bulunan bilgisayara aktarılır
    -  eğer frame ilgili yerel bilgisayaara ait adrese sahip değil ise göz ardı edlir

## Donanım adresi formatları
* bir sayısal değerdir uzunluğu 6ybte dır

## Donanım adreslerinin atanması
* donanımadresi o yerel ağ üzerinde eşsiz olmalı
* bu adreslerin atanması nasıl olacak, ve bu değerlerin eşsiz olması kim tarafından sağlanıyor
* Static(firma tarafından):
  - donanım üreticisi her bir arayüze kalıcı bir adres atar
  - üretici her bir arayüze eşsiz bir adrese sahip olduğunu garanti etmelidir
* Dynamic():
  - donanım adresi son kullanıcı tarafından atanabilir bu işlem doğrudan bir switch vasıtası veya bir jumpers üzerinden gerçekleştirilebilir
  - sistem yöneticisinin çakışmayı önlemek için koordine etmelidir
* Automatic:
  - arayüz her bir bilgisayar açıldığında doğrudan bir donanım adresi atar
  - otomatik şemalar çakışmaları önleyecek şekilde güvenilir olmalıdır

## Broadcasting
* bazı uygulamalar lan üzerindeki bütün istasyonlara mesajı dağıtmak isteyebilir
* bu durumda ortak iletişim kanalı broadcast i verimli kılar - mesaj bütün istasyonlara dağıtılır
* özel bir broadcast adresi broadcast mesajlarını tanımlamak için kullanılır ki bu sayede mesaj bütün istasyonlar tarafından kabul edilir

## Paket içerikleirnin tanımlanması 
* hedef bilgisayar frame içerisindeki verinin nasıl yorumlanacağı noktasında bazı ip uçlarına sahip olmalıdır
* Kullanımı
  - açık frame tipi - verinin içerisinde, verinin tipini tanımlayan bilgi framenin içerisine yerleştirilir
  - üstü kapalı frame tipi - alıcı aldığı veri üzerinden tipi kendi çıkarmalıdır

## Başlık ve frame formatları
* Lan teknoloji standartları her bir teknoloji iin frame formatı tanımlar
* bütün çağdaş standartlar bu formatı kullanır (başta frame header ve frame data area veya payload )
* frame header adresleri ve diğer tanımlamaları içerir
* bu alanlar içerisindei bilgi genellikle sabit boyut ve konuma sahiptir
* veri alanı boyu değişebilir

### (ue5 - 24 / 04 / 2020)

## Örnek frame format

8 byte lik premble (senkronizasyon için kullanılır)
-- header--
6 bytlık hedef adres 
6 byte lik kaynak adresi
2 byte lik frame tipi
--header--
--payload--
geri kalan frame içerisindeki veri bilgisi 46 ile 1500 byte arasında değişir
--payload--
4 byte CRC

## Ethernet alanları
* preamble ve crc genelde gösterilmez
* eğer hedef adres bilgisinin hepsi 1 ise bu broadcast adresidir
* bazı değerler frame tipi alanı için ayrılmıştır

## Tip alanı olmayan frameler
* bazı yerel ağ (lan) teknolojileri tip alanı içermez bu durumda 
* gönderici ve alıcı framenin yorumlanması aşamasında uzlaşmalıdır
  - tek bir veri formatı uzerinde uzlamşa sağlanacak 
    - yanlızca o format kullanılacaktır
    - yerel ağ üzerindeki bütün bilgisayarlar bu tek formatı kullanmak zorundadır
  - data alanının ilk birkaç byte içerisinde veri formatı kodlanabilir

## Veri tipinin kodlanması
* veri alanının ilk birkaç byte içerisinde veri formatı kodlanacaktır
* evrenselliği sağlayabilmek amacı ile evrensel kabul görmüş bir format kullanılmalıdır
* bu format standart kuruluşlar tarafından belirlenöiştir

## IEEE 802.2 LLC
3 byte lik bir llc bilgisi peşinden 5 byte lik snap bilgisi vardır
günümüzde kullanılan yapı 802.3 tür (ethernet frame 2 olarak geçer)

## Bilinmeyen tipler
* herhangi bir kodlama tekniği ya da bilgisayarlar tarafından alınan bazı frame tipleri henüz bilgisayarın tanımadığı bir tipte olabilir
  - protokol tipi kurulmamış
  - yeni tanımlanmış

## Network analyzers
* notwork analyzer, network monitor ya da network sniffer bir ağın performansını inceleme noktasında veya ağın hatalarını tespit noktasında kullanılabilir
* veya belirli bir framenin ağın üzerindeki dağılımını, çakışma oranını, kapasite kullanımını, tokenin ağdaki dönüş süresini gibi istatistik sonuçlarına ulaşabiliriz
* veya belirli bir frameyi görüntüler ve kayıt edebiliriz, paket iletimlerini ve paket alışverişlerini anlamak ve tespit etmek amacı ile kullanabiliriz

## network analyzer çalışma şekli
* temelfikir şudur network arayüzüne sahip bir bilgisayar ağdaki bütün servisleri alır
* promisicuous mode bazen çağırılır
* birçok masaüstü bilgisayarı bir ağ arayüz kartına ship formülsüz mod olacak şekilde konfigure edilebilirler
  - yazılım ile birlikte combine edilip, bilgisayarın yerel ağ üzerindeki herhangi bir framenin incelemesi sağlanabilir
  - yerel ağ üzerindeki haberleşme asla bunun özel olacağını garanti etmez
* bilgisayar yerel ay üzerindeki frameleri alır ve bunları görüntüler

## Gelen framelerin filtrelenmesi
* analyzer frameleri filtreleyecek ve bunlar üzerinde çalışacak şekilde konfigüle edebilir
  - belirli bir tipteki veya belirli bir boyuttaki frameler sayılabilir
  - belirli bir bilgisayardan gelen veya berirli bir bilgisayara giden frameleri görüntüleyebilir
  - genel olarak sizin belirttiğiniz filtredeki kıstasları karşılayacak şekilde bazı frameler yakalanacak şekilde de konfigure edilebilir
* analyzerlar belirli bir zaman periyodu üzerindeki toplam hesaplamayı gçsterecek şekilde realtime performansı size gösterebilirler

## özetle
* lan teknolojileri donanım adresleri kullanırlar bu adresler ortak iletişim hattı üzerinden gönderilen frameler için hedef adresi tanımlamada kullanılır
* her bir yerel ağ teknolojisinin kendine özgü bir donanım formatı vardır
* adresler static otomatik veya configurable dinamik şekilde atanabilir
* her bir bilgisayarın yerel a üzerinde eşsiz bir adrese sahip olması gerekir
* frameler hedef adres için bir başlık bilgisi barındırırlar kaynak ve diğer bilgiler de yine bu hader bilgisi içerisinde bulunur
* frame tipi frame verisinin nasıl yorumlanacağını tanımlar
* network analyzer gelen bütün frameleri alır ve buna bağlı olarak istatistiki sonuçları size görütüleyebilir veya ortaya çıkacak hata problemlerinde yardımda bulunabilir
 
### (chapter 9)

# Giriş
* Arayüz kartları
 - neden ayrı bir kart yapılıyor
 - bu interface yi bilgisayara nasıl bağlıyacağız
 - tranceiver nedir
* Lan kablolama şemaları* mantıksal ve fiziksel topoloji

## Yerel ağ ve bilgisayarların hızı
* yerel ağdaki veri iletim hızı tipik olarak cpu hızlarına göre daha hızlıdır
* 100mhz lik bir cpu 100mhz lik bir ethernet üzerindeki her bir bit için bir emir icra edebilir
* yerel ağ hızları spesifik bir işlemci hızından bağımsız olarak tasarlanmıştır
  - karışık bağlı sistemlerin çalıştırılabilir olmalarını sağlar
  - yeni bilgisayarlar ağ hızını etkilemeyecek şekilde sisteme etkilemeyebilir

## Network interface hardware
* cpu ağ hızında veriyi işleyemez
* bilgisayar sistemleri ağ baplantısı için özel amaçlı bir donanım kullanırlar
  - bu tipik olarak bu arka plandaki ayrı bir karttır
  - Network adapter card veya network interface card (NIC)
* bilgisayarın arka tarafında bir bağlantısı vardır ve fiziksel network üzerinden kablo ile bu verileri kabul eder

## Nıcs and netwok hardware 
* nic fiziksel network un bir türü için geliştirilmiştir
  - ethernet arayüzü token ring ile birlikte kullanılamaz
  - atm arayüzü fddi ile birlikte kullanılamaz
* Bazı NIC ler farklı ve benzer donanımlar ile kullanılabilir
  - thick, thin, 10BaseT
  - 10mbps ve 100mbps ethernet
 
## Nıc ve Cpu işleme
* nic sistem cpu sundan bağımsız olarak veriyi işleyebilecek yeterli derecede donanıma sahiptir
  - bazı nic lerin kendilerine özgü mikro işlemcileri de vardır
  - bunlar içerisinde (nics) analog bir devre, sistem yolarına bir bağlantı, bufferlama ve işlem
* bu nickler tıpkı diğer giriş çıkış aygıtları gibi sistem cihazına bir giriş çıkış aygıtı olarak görülür
  - sistem cpu su mesaj isteğini gösterir, 
  - verinin iletileceğine dair emirleri nic e gönderir
  - veri geldiğinde de interrupt ile birlikte verinin geldiği bilgisini ethernet kartından alır

## nic ve fiziksel network arasındaki bağlantı
* 2 altarnatif
  - nic bütün bağlantı devresini içerir ve doğrudan network ortamına bağlanır
  - nic den gelen kablo ek bir devreye bağlanır bu ek devre de bizi network ortamına bağlar
* thin ethernet ile 10Base-T
* bunların ikisi de ethernet teknolojisindedir network teknolojisi bir bağlantı ile sınırlı değildir

## Thick eternet kablolama
* coax kablo kullanır
* AUI kablo bu bizi nic den transceiver denilen aygıta bağlar
* nic üzerinden gelen dijital sinyalleri tranceiver e taşır
* tranceiver gelen dijital sinyalleri analog sinyale çevirir ve coax kabloya verir
* AUI içerisindeki kablosu içerisindeki hatlar dijital sinyalleri, güç ve diğer kontrol sinyallerini taşır

## Bağlantı çoğullama
* bazı durumlarda tranceiver lar uygun olmayabilir örnek labarotuarlardaki workstations lar
* bağlantı çoğullayıcı birden çok bilgisayarı tek bir tranceiver a bağlar
  - her bir bilgisayarın AUI kablosu bilgisayarı multiplexor a bağlar 
  - AUI da multiplexor dan coax kabloya bağlar
* çoğullayıcı tamamı ile bağlı bilgisayarlara görünmezdir

### (ue6 - 30 / 04 / 2020)

## thin ethernet wiring
* ince coax kullanılır, buda kalın ethernet coax a göre ucuz maliyet oluşturmamızı ve daha kolay yönetebilmemizi sağlar
* tranceiver elektroniği doğrudan NIC içerisine import edilmiştir; NIC doğrudam network ortamına bağlanır
* coax kablo bağlantı için BNC connector kullanır
* coax kablo doğrudan bağlı bilgisayarın arkasına yerleştirilir
* T connector bilgisayarın üzerinde bulunan NIC a doğruadn bağlantı sağlar
* eğer bilgisayarlar birbirine çok yakın konumlanmış ise faydalıdır
* fakat güvenli değildir bağlantı kopması durumu bütün ağ etkilenir

## 10Base-T
* 10Base-T, twisted pair yada TP Ethernet denilebilir
* AUI kablosu twisted pair cablosu ile değiştirilmiş
* thick coax yerine burada hub var

## Hubs
* bağlantı çoğullama kavramının genişletilmiş halidir
* bazen "Ethernet-in-a-box" olarak çağırılır
* efektif olarak uzun AUI kabloları yerine oldukça kısa Ethernet kabloları mevcut
* Bu ağlar daha büyük ağlara bağlanabilir

## Protokol yazılımı ve ethernet kablolama
* bütün kabolama teknolojileri benzer ethernet tanımlamasını kullanırlar
  - benzer frame formatı
  - benzer CSMA/CD algoritmaları
* birden fazla teknolojiyi harmanlayabilirsiniz
* NIC bize bu 3 bağlantı teknolojisini de sağlar
* protokol yazılımları kablolama teknolojileir arasındaki farkı anlayamaz

## kablolama şemalarının karşılaştırılması
* Ayrı tranceiver, bilgisayarların kapalı olabilmesini veya networktan koptuklarında iletişime zarar vermemesini sağlar
* transciever uygunsuz bir konumda olabikir
* hatalı arızalı çalışan transceiver in bulunması zor olabilir
* thin minimum kablo kullanır
* bir bilgisayarın hatalı bir duruma düşmesi ve bağlantının kopması bütün bir ağı kopartabilir
* hub kablolama elektronik ve bağlantıları merkezleştirir
* maliyetleri sebebi ile oldukça populer

## Tapolojiler ve network teknolojileri
* 10Base-t; kablolama teknolojisi yıldızdır, mantıksal (network topolojisi) ise Bus dır
* Token Ring çalışma teknolojisi mantıksal olarak ring dir, kablolama teknolojisi yıldızdır

## Diğer Teknolojiler
* AppleTalk bağlantı kablosu ile transceivers e bağlanır ve Bus kablolama kullanır
* AppleTalk 4 kablolu telefon kablosunun yedek bağlantılarını kullanarak bağlantıyı sağlar

## Özet
* NIC bilgisayarları networke bağlar
  - nic işlemlerini bağımsız şekilde gerçekleştirir; network ile uyumlu şekilde haraket edecek kadar hızlıdır
  - Genellikle CPU ile etkileşim için kesmeler kullanır
* birçok fiziksel kablolama şeması mantıksal network tapolojisine uygundur
* 10Base-T mantıksal olarak bus fiziksel olarak yıldızdır

### (ue7 - 07 / 05 / 2020)

### (Chapter 10)

# Giriş
* Lan Teknolojileri hız mesafe ve maliyet gibi kısıtlamalar ile dizayn edilmiştir
* tipik lan teknolojisi çoğunlukla birkaç yüz metreye kadar genişleyebilir
* biz bu yerel ağları örnek olarak bir kampusu kaplayacak şekilde nasıl genişletebiliriz

# Mesafe için Lan dizaynı
* bir çok yerel ağ paylaşımlı ortam kullanır - etkernet teknolojisi , token ring
* ortamın uzunluğu ortama erişim noktasındaki adaleti sağlamada rol oynar
  - CSMA / CD - frameler arası gecikme, minimum frame uzunluğu
  - Token passing - ortam büyüdükçe tokenin ağdaki dönüş süreci de artar
* ortam büyüdükçe elektrik sinyalinin gücü de etkilenir, gürültü bağışıklığına karşı bağışıklık kazanılır

## Lan Uzantıları
* çeşitli teknikler ile lan ortamının çapını gebişletiriz
* çoğu tekniker ek donanım kullanır
* Lan sinyalleri lan gegmentleri arasında iletilir
* sonuçta bu bütünleşik teknoloji orjinal mühendislik kısıtlamaları içerisinde kalırken daha uzak mesafeleri kapsayabiliriz

## Fiber Optic uzantılar (Fiber Modem)
* görüleceği üzer fiberoptik cablo kullanarak biz bağlantımızı uzak bir bilgisayara erişecek şekilde genişletebiliriz
* Fiber Modemler
  - AUI sinyalleri dijital sinyallere çevrilir
  - fiber optik kablo üzerinden diğer modemlere gelen sinyalleri iletir
* 2 tane yerel ağı birbirine bağlamak için (en sık kıllanılan yapılardan biri), bir bridge üzerinden sağlanıyor farklı binalar ile

## Repeaters
* repeaters kullanarak yerel ağ ortamını genişletebiliriz
  - ethernet - ortam büyüdükçe zaman kısıtlaması oluşur
  - sinyal gücü limit uzunluğunu sınırlar
* bir repeater lan segmentinin boyutunu etkin bir şekilde iki katına katlayabilir

## Ethernet repeater ları
* baitçe sinyalleri segmentler arasında kopyalar
  - framme formatlarını anlamaz
  - herhangi bir donanım adresi de içermez
* herhangi bir segment 500 metre ile sınırlıdır
* repeater ile bu uzunluk 2 katına çıkartılabilir (1000 metre)

## repeater mimarisi
* repeater sayesinde interneti bina içerisinde güçlendirebilirsiniz
* diğer repeater lar da frameleri diğer segmentler üzerinde iletilirs

-> FOIRL - uzak yerleri bağlama noktasında kullanılabiir

## Repeater ların karakteristikleri
* çok kolay kullanımı vardır - sadece ekleyin
* repeaterlar kolaylıkla analog sinyalleri yeniden iletir
  - çakışma varsa bile bütün network e iletir (Dolayısı ile bütün network etkilenir)
  - geçiş problemleri - gürültü, gürültüyü de network e olduğu gibi iletir

## Bridge ler
* LAn segmmentlerini baplamak için kullanılan yapılardan biri
* bir segmetten gelen frameleri diğer segment veya segmentlere yeniden iletir
* Bütün frameyi işler 
  - diğer istasyonlar gibi NIC kullanır
  - Frame üzerinde bazı işlemler gerçekleştirir
* diğer bağlı bilgisayarlara hissettirmezler

## Bridge lerin karakteristiği
* nispeten kolay kunnımı vardır
* gürültüyü, çakışmayı izole eder
* diğer bridgeler iletilen frameyi alabilir

## Bridgelerin filtrelenmesi
* bridge framme üzerinde ek işlemler yapar
  - çakışma veya gürültüyü iletmez
  - yanlızca gerekliyse frameyi iletir

## Brigde frame filtreleme
* Bridge frame filtreleme yapar, framelri yerel ağ segmentleri boyuncaca hedefe iletir
  - frameleri izleyerek istasyonların konumlarını öğrenir
  - broadcast ve multicast mesajlarını iletmesi gerekir
* bridge gelen her bir framenin hdefini kontrol eder
* ve bu hedefi bilinen istasyonlar istesinde arar
  - kendisine gelen frameyi hedefe doğru olan yoldaki birsonraki arayüze iletir
  - Eğer hedef frameyi aldığımız segmentte ise bu durumda bridge ilgili frameyi bir sonraki segmente iletmez

## bilinen istasyonlar listesini nasıl kurar?
* bridge gelen her bir framenin kaynak adresini inceler
* framenin alındığı lan segmenti için listeye bir girdi ekler
* eğer hedef kendi listesinde yoksa ilgili her bir frameyi iletmeye devam eder










