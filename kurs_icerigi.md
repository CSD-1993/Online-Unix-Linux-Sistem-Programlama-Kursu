# Online UNIX/Linux Sistem Programlama Kurs İçeriği

## Temel Kavramlar 

+ Kurs için gereken temel kavramların gözden geçirilmesi
+ UNIX türevi sistemlerin tarihsel gelişimi
+ Özgür Yazılım ve Açık Kaynak Kod akımları
+ UNIX türevi sistemlere yönelik standartlar 
+ Kaynak yöneticisi olarak işletim sistemleri
+ Dağıtım `(distribution)` kavramı.
+ Belli başlı Linux dağıtımları ve bu dağıtımlar arasındaki ilişkiler
+ Proses kavramı 
+ Proseslerin kontrol blokları
+ Çok prosesli `(multiprocessing)` çalışma ve zaman paylaşımlı `(time sharing)` CPU kullanımı 
+ Preemptive işletim sistemlerinin temel özellikleri 
+ Kavramsal olarak POSIX fonksiyonları, Standart C Fonksiyonları ve işletim sisteminin sistem fonksiyonları
+ POSIX fonksiyonlarında başarısızlık durumunun tespit edilmesi ve eele alınması

## UNIX Türevi Sistemlerde Login İşlemleri

+ Sisteme giriş ve login işlemi
+ Kullanıcı ve grup kavramları
+ Kullanıcı ve grup isimleri
+ Login sırasında yapılan kontroller
+ Linux dizin yapısının incelenmesi `(/bin dizini, /lib dizini, /usr dizini, /mnt dizini, …)`

## UNIX/Linux Sistemlerinde Temel Dosya İşlemleri

+ Proseslerin kullanıcı ve grup id’leri
+ Proseslerin ek grup id’leri `(supplemantary group ids)`
+ Kullanıcı ve grup bilgilerinin elde edilmesi
+ Yol ifadelerinin anlamı, mutlak ve göreli yol ifadeleri
+ Prosesin çalışma dizininin `(current working directory)` anlamı, elde edilmesi ve değiştirilmesi
+ UNIX/Linux sistemlerinde dosya işlemleri ve temel POSIX dosya fonksiyonları `(open, read, write, lseek, close)`
+ Dosyaların ve dizinlerin erişim hakları ve anlamları 
+ Ayrıcalıklı `(root)` erişim hakkına sahip prosesler 
+ Dosya bilgilerinin elde edilmesi ve stat fonksiyonları
+ Yardımcı dosya fonksiyonları (chmod, remove, chown,  …)
+ Dizinler üzerinde işlemler (dizinlerin yaratılması, yok edilmesi, dizinlerin erişim özellikleri, …)
+ Dizin içerisindeki girişlerin elde edilmesi
+ Dizin ağacının özyinelemeli olarak dolaşılması

## Önbellek (cache) Kavramı ve Linux Çekirdeğinin Uyguladığı Önbellek Mekanizmaları

+ Önbellek sistemleri
+ Linux çekirdeğinde `“buffer cache”` ve `page cache”` sistemleri
+ Kullanıcı modundaki `(user mode)` dosya işlemlerinde gerçekleştirilen ön bellek `(tampon)` sistemleri
+ C Programlama Dilinin stdio kütüphanesi tarafından uygulanan önbellek mekanizması
+ stdin, stdout ve stderr dosyalarının kullanıcı düzeyinde önbelleklenmesi
+ Linux çekirdeğinin `“page cache”`, `“dentry cache”` ve `“i-node cache”` sistemleri

## Dosya Yönlendirmeleri

+ Dosya betimleyicilerinin `(file descriptors)` anlamı
+ Linux çekirdeğinde dosya nesneleri ve dosyalara ilişkin veri yapıları
+ Dosya yönlendirmesinin yapılması `(dup ve dup2 fonksiyonlarının kullanımı)`
+ stdin, stdout ve stderr dosyalarının yönlendirilmesi

## İşlemcilerin Koruma Mekanizmaları ve KullanıcıModu (User Mode) / Çekirdek Modu (KernelMode) Proses Kavramı

+ Koruma mekanizmasının anlamı
+ Bellek ve komut korumaları
+ Proseslerin bellek izolasyonu hakkında temel bilgiler
+ Çekirdeğin kendini kullanıcı modundaki `(user mode)` prosesler tarafından koruması
+ Kullanıcı modu `(user mode)` ve çekirdek modu `(kernel mode)` kavramları
+ Prosesin kullanıcı modundan çekirdek moduna geçmesi ve geri dönmesi (user mode/kernel mode transition)

## İşlemcilerin Sayfalama (Paging) Mekanizmları ve Sanal Bellek (Virtual Memory) Kullanımı

+ İşlemcilerin sayfalama mekanizması
+ Intel ve ARM işlemcilerinde sayfalama mekanizması
+ Sayfa tabloları (page tables) 
+ Çok prosesli çalışmalarda sayfa tablolarının organizasyonu
+ Sayfalama için kullanılan içsel kesmeler 
+ Sanal bellek mekanizması
+ Linux çekirdeğinin sanal bellek gerçekleştirimi hakkında temel bilgiler
+ 32 bit ve 64 bit Linux proseslerinin sanal belleğe yüklenmesi
+ Linux sistemlerinde proseslerin bellek alanlarının izole edilmesi

## UNIX/Linux Sisteminde Proseslerin Yaratılması ve Proseslerle İlgili Temel İşlemler

+ Üst `(parent)` ve alt proses `(child)` kavramları
+ Proseslerin id değerleri
+ fork fonksiyonunun kullanımı
+ fork işleminin çekirdek tarafından gerçekleştirilmesi
+ fork işleminde üst prosesten alt prosese aktarılan bilgiler
+ exec işleminin anlamı
+ exec fonksiyonları
+ fork ve exec fonksiyonlarının birlikte kullanılması
+ Prosesler üzerine işlemler yapan POSIX fonksiyonları
+ Proseslerin exit kodları ve anlamı
+ Alt proseslerin beklenmesi ve wait fonksiyonları
+ init prosesi
+ Hortlak `(zombie)` prosesler, hortlaklığın nedeni ve ortadan kaldırılması
+ Öksüz `(orphan)` prosesler
+ Proseslerin kod, data ve stack alanları

## Proseslerin Çevre Değişkenleri `(Environment Variables)`

+ Proseslerin çevre değişkenlerinin anlamı ve önemi
+ Çevre değişkenlerinin değerlerinin elde edilmesi ve değiştirilmesi
+ Prosesin çevre değişken listesinin elde edilmesi
+ Çevre değişkenlerinin Linux çekirdeği tarafından organize edilme biçimleri
+ Çevre değişkenlerinin alt proseslere aktarılması

## Prosesler Arası Haberleşmeler

+ Prosesler arası haberleşmenin anlamı ve önemi
+ İsimli ve isimsiz boru haberleşmeleri `(named/unnamed pipes)`
+ Boru haberleşmeleri yoluyla client/server tarzı uygulamalar
+ Linux çekirdeğinin boru haberleşmesini sağlama biçimi
+ Paylaşılan bellek alanları `(shared memory)` yoluyla prosesler arası haberleşme
+ Paylaşılan bellek alanlarının System 5 ve modern POSIX fonksiyonlarıyla oluşturulması
+ Paylaşılan bellek alanlarının Linux çekirdeği tarafından gerçekleştirimi
+ Paylaşılan bellek alanlarında senkronizasyon sorunu
+ Bellek tabanlı dosyalar `(memory mapped files)`
+ Mesaj kuyrukları yöntemi
+ Mesaj kuyruklarının System 5 ve modern POSIX fonksiyonlarıyla oluşturulması ve kullanılması
+ Aynı makinenin prosesleri arasında haberleşmede kullanılan diğer yöntemler

## Thread’lerle İşlemler

+ Genel olarak thread kavramı 
+ Thread’lerin kullanılma gerekçeleri
+ POSIX'in pthread kütüphanesinin tanıtımı
+ Thread’lerin yaratılması ve ve sonlanması
+ Thread’lerin özellikleri (thread attributes)
+ Thread’lerin sonlanmasının beklenmesi
+ Thread’lerin yok edilmesi (therad cancellation)
+ Thread’lerin bloke olması
+ Çok thread’li uygulamalar
+ Thread’ler arası haberleşmeler
+ Thread senkronizasyonun anlamı
+ Mutex senkronizasyon nesnelerinin kullanımı
+ Mutex özelliklerinin değiştirilmesi
+ Semaphore senkronizasyon nesnelerinin kullanımı
+ Farklı proseslerin thread’leri arasında senkronizasyon
+ Okuma/yazma kilitleri
+ Koşul Değişkenleri `condition variables)`
+ Interlock işlemleri
+ Kilitlenmeye yol açmayan veri yapıları `(lock-free data sturctures)` hakkında temel bilgiler
+ Thread’e özgü alanlar `(thread specific data)`
+ Fonksiyonların thread güvenliliği `(thread safety)` 
+ Linux çekirdeğinin thread gerçekleştirimi
+ POSIX thread çizelgelemesi ve thread öncelikleri
+ Linux sistemlerinde thread çizelgelemesinin ayrıntıları
+ Thread havuzları `(thread pools)` ve thread havuzlarının gerçekleştirimleri

## Sinyal (Signal) İşlemleri

+ Sinyal kavramı
+ POSIX sinyallerinin tanıtımı
+ Sinyallerin oluşması ve proseslere gönderilmesi
+ Sinyallerin ele alınması, signal ve sigaction fonksiyonlarının kullanımı
+ Proseslere sinyal gönderilmesi ve kill fonksiyonun kullanımı
+ Sinyallerin bloke edilmesi
+ Sinyaller ve thread’ler
+ Gerçek zamanlı sinyaller
+ Sinyaller yoluyla proses senkronizasyonu
+ Sinyaller tarafından kesilen sistem fonksiyonlarının yeniden başlatılması

## Proseslere İlişkin Ayrıntılar

+ Proses grupları
+ Terminal Kavramı
+ Oturum `(session)` kavramı
+ İş `(job)` kavramı ve iş kontrol sinyalleri

## Proseslerin Kaynak Kullanımı

+ Proseslerin kullandığı kaynaklar
+ Proseslerin kaynak limitlerinin elde edilmesi ve değiştirilmesi
+ Proseslerin kaynak kullanımlarının sınırlandırılması

## Daemon Prosesler (Linux Servis Programları)

+ Daemon kavramı ve daemon proseslerin aşağı seviyeli incelenmesi
+ Daemon’ların yazımı ve kullanımı
+ Daemon’lara ilişkin ayrıntılı işlemler

## Linux Sistemlerinde Proseslere İlişkin Yetenekler `(Process Capabilities)`

+ Linux sistemlerinde proses yetenekleri `(process capabilities)` kavramı
+ Proses yeteneklerinin listesi ve anlamı
+ Proses yeteneklerinin set edilmesi ve üst prosesten alt prosese aktarılması

## Linux Sistemlerinde Tarih ve Zaman İşlemleri 

+ Tarih ve zaman işlemleri yapan standart C fonksiyonları ve POSIX fonksiyonları
+ Bölgesel ayarlar ve locale işlemleri
+ Linux çekirdeğinde zamanlama işlemleri 
+ Sistem zamanının güncellenmesi

## Linux Sistemlerinde Statik ve Dinamik (Shared) Kütüphaneler

+ Kütüphane `(library)` kavramı
+ Statik ve dinamik kütüphaneler arasındaki farklılıklar
+ Statik kütüphanelerin yaratılması ve kullanılması
+ Dinamik kütüphanelerin yaratılması ve kullanılması
+ Dinamik kütüphanelerin yüklenmesi
+ Konumdan bağımsız kod `(position independent code)` kavramı
+ Dinamik kütüphanelerde versiyonlama
+ Dinamik kütüphane kullanan uygulamaların konuşlandırılması
+ Dinamik kütüphanelerin programın çalışma zamanı sırasında dinamik biçimdeyüklenmesi ve kullanılması
+ Dinamik kütüphaneler konusunda kullanılan yardımcı programlar

## İleri Dosya İşlemleri

+ Proseslerin kök dizinleri
+ Dosya özelliklerinin değiştirilmesi
+ Dosyaların kilitlenmesi `(file locks)`
+ Dosya sistemi üzerinde gerçekleşen olayların ele alınması
+ Asenkron dosya işlemleri
+ select ve poll fonksiyonlarının kullanımı
+ Dosya delikleri `(file holes)`
+ Dosya tamponlarının yönetilmesi
+ Dosya sisteminin mount edilmesi 
+ Otomatik mount işlemleri
+ Linux çekirdeğinin mount işlemlerini ele alma biçimi

## UNIX/Linux Sistemlerinde Soket Programlama

+ Bilgisayar ağları hakkında temel bilgiler
+ Haberleşme protokollerine kısa bir bakış
+ IP protokol ailesi
+ OSI katmanları ve IP protokol ailesi katmanları
+ Berkeley soket arayüzü ve soket kütüphanesinin kullanımı
+ TCP/IP client/server programlama
+ Client/server programlamadaki mesa formatları
+ Çok client’lı uygulamalar ve çok client’lı uygulamalarda izlenecek stratejiler
+ IP protokol ailesinin uygulama katmanına ilişkin bazı protokolleri hakkında açıklamalar `(telnet, pop3, imap, http ...)` ve bunlara ilişkin client programların yazımı
+ UDP/IP uygulamaları
+ UNIX domain soketlerinin kullanımı
+ Ölçeklenebilir `(scaleable)` dağıtık uygulamaların gerçekleştirilmesine yönelik stratejiler
+ Linux çekirdeğinin protokol mimarisi `(Linux TCP/IP stack)`
+ `Network sniffer` programlar ve pcap kütüphanesinin kullanımı

## Proc ve Sys Dosya Sistemleri

+ Proc ve Sys dosya sistemlerinin tanıtımı
+ Proc ve Sys dosya sistemlerinin girişlerinin anlamı
+ Proc ve Sys dosya sistemlerinin okunması ve yazılması
+ Proc ve Sys Dosya sistemlerinin Linux çekirdeği tarafından gerçekleştirimi

## Object ve Executable Dosya Formatları

+ Object dosya ve executable dosya kavramları
+ ELF formatının incelenmesi
+ ELF formatı üzerinde işlem yapan programlar
+ GNU BFD kütüphanesinin temel kullanımı
+ Object dosyaların link edilmesi
+ Relocation işlemi 
+ Flat binary dosyaların oluşturulması

## Linux Dosya Sisteminde Disk Organizasyonu

+ Linux sistemlerinin kullandığı dosya sistemlerinin tanıtımı
+ Linux'ta disk sektörlerinin okunması ve yazılması
+ Loopback aygıtlar
+ I-Node tabanlı dosya sistemlerinin disk organizasyonları
+ Dosyaların i-node bilgileri
+ Hard link ve soft link kavramları
+ Ext-2, Ext-2 ve Ext-4 sistemlerinin disk organizasyonu ve bu dosya sistemlerinin aşağı seviyeli incelenmesi

## Linux Sistemlerinde Boot Süreci

+ Linux sistemlerinin boot edilmesi
+ Boot sürecinin ayrıntıları
+ Çekirdeğin boot parametreleri `(kernel boot parameters)`
+ Çekirdek imaj dosyasının yüklenmesi
+ Boot işlemi sırasında işlem gören çeşitli sistem dosyaları ve işlevleri
+ Boot işleminden sonra yaratılan temel prosesler 

## Linux Çekirdek Kodlarının İncelenmesi

+ Linux çekirdek kodlarının dizin organizasyonu
+ Linux çekirdek kodlarının genel yazım biçimi
+ Linux çekirdek kodlarında kullanılan temel veri yapıları
+ Linux çekirdeğindeki dinamik tahsisat sistemleri `(buddy allocator, slab allocator, …)`
+ Linux çekirdekleri arasındaki versiyon farklılıkları

## Linux Çekirdeğinin Yeniden Derlenmesi

+ Linux çekirdeğinin derlemesi
+ Linux modüllerinin eklenip çıkartılması
+ Linux kaynak kodlarında değişiklikler yapılması

## Linux Aygıt Sürücüleri

+ Aygıt sürücülerin anlamı
+ Linux aygıt sürücü mimarisinin tanıtımı
+ Linux çekirdek modüllerinin yazımı
+ Çekirdek modüllerinin yüklenmesi ve boşaltılması
+ Karakter aygıt sürücülerinin yazımı
+ Aygıt sürücülerde senkronizasyon işlemleri
+ Aygıt sürücülerde bekleme kuyruklarının yaratılması ve bloke işlemlerinin sağlanması
+ Aygıt sürücülerde bellek tahsisatları
+ Aygıt sürücülerin IO portlarını kullanması
+ Aygıt sürücülerde kesme işlemlerinin yönetilmesi
+ Blok aygıt sürücülerinin yazımı
+ Blok aygıt sürücülerinde bellek haritalaması ve DMA kullanımı 
+ USB aygıt sürücüleri























	
