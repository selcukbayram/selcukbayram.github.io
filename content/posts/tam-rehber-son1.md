---
title: "N.I.N.A İle Gözlem Kılavuzu"
date: 2026-08-09T21:04:00+03:00
draft: false
classes:
---

# **<mark>Adım Adım N.I.N.A Gözlem Rehberi:</mark>** 

# **Adım 1: Fiziksel Kurulum ve Kubbe Açılışı** 

1. **Güç Aktivasyonu:** Akşam havası gözlem için uygunsa bilgisayar odasına geçilir. Duvarda yer alan filtre, odaklayıcı (focuser) ve kubbe görüntü sistemlerine elektrik veren o beyaz tuşlar açılır. 

2. **Oturum Açma:** Bilgisayar açılır ve NINA Gözlemci oturumuna girilir. Şifre 55900'dür. 

3. **Yazılımların Başlatılması:** Masaüstünden N.I.N.A. programı ve kubbe kontrolü için Dome Control programı çalıştırılır. 

4. **Mekanik Kubbe Açılışı:** Kubbeye fiziksel olarak çıkılır. Panolardan kubbe kapağını açmak için şu mekanik hiyerarşi izlenir: 

**Pano-1 Kontrolleri:** Bu pano kubbenin gökyüzüne açılan kapağını açmak için kullanılır. 

- Önce ON (Güç verilir). 

- Sonra OPEN (Kubbe kapağı açılır). 

- Açılma bitince sesli uyarı sonrası tuş Boş-Orta konuma alınır (Kapak motoru devreden çıkarılır). 

- En son OFF (Güç tamamen kesilir). 

**Pano-2 Kontrolleri:** Bu pano kubbenin dome control programı ile kendi ekseni etrafında sağa sola döndürülmesini sağlamak için kullanılır. 

   - Önce ON (Güç verilir). 

   - Sonra OPEN (Kubbe kapağı açılır). 

   - Açılma bitince sesli uyarı sonrası tuş Boş-Orta konuma alınır (Kapak motoru devreden çıkarılır). 

   - En son OFF (Güç tamamen kesilir). 

5. **Teleskop Kapağı (Shutter) Açılışı:** Kubbe açıldıktan sonra, iç ortam ile dış ortamın ısı dengesinin sağlanması şarttır. Ayrıca kubbe açılırken ray sistemlerinden fiziki olarak teleskop camına herhangi bir madde düşme tehlikesi olduğundan dolayı teleskobun fiziki kapağı (shutter) KESİNLİKLE KAPALI bırakılır. Kubbe açılması fiziki olarak tamamlanınca teleskop kapağı (shutter) açılır. 

6. **Karanlık Adaptasyonu:** Kubbeden bilgisayar odasına inilirken kubbe odasının ışıkları tamamen kapatılır (Kaçak ışık veriyi bozar). 

# **Adım 2: N.I.N.A. ve Donanım Bağlantıları** 

Fiziksel donanımları yazılıma (N.I.N.A.) entegre ettiğimiz kısımdır. Ana menüden **Equipment** (Ekipman) sekmesine girilerek sırasıyla tüm cihazların köprüleri kurulur: 

1. **Camera:** Camera menüsünden "ZWO ASI1600MM Pro" seçili olduğu kontrol edilir ve güç simgesine tıklanarak kamera ile bağlantı kurulur. Sağdaki Temperature control kısmından kar tanesi simgesine tıklanarak kameranın sensör soğutması başlatılır. (Termal gürültüyü azaltmak için kameranın belli bir eksi dereceye inmesi beklenir). 

2. **Filter Wheel:** Filter Wheel menüsünden güç simgesine tıklanır ve gözlem hangi filtre/filtreler ile yapılacaksa açılır menüden seçilerek change tuşuna basılır.. 

3. **Focuser:** Focuser menüsünden "DeviceHub (ASCOM)" seçeneğinin seçili olduğu kontrol edildikten sonra güç tuşu simgesi tıklanarak focuser bağlantısı sağlanır. 

4. **Guider:** Guider sekmesinden güç simgesine tıklanır ve kılavuz kamerasını yönetecek olan **PHD2** uygulamasının arka planda otomatik açılması sağlanır. 

5. **Mount (Teleskop):** Mount sekmesinden **POTH Hub** seçilerek güç simgesine tıklanır ve teleskop yazılıma bağlanır. 

6. **Kubbe (Dome):** Masaüstündeki Dome Control (Observa Dome) uygulamasında bağlantı portu **COM4** seçilir ve **Connect** tuşuna basılır. N.I.N.A.'nın teleskop döndükçe kubbeyi de otonom olarak döndürebilmesi için mutlaka **Enable** kutucuğu işaretlenir. 

# **Adım 3: Gözlem Bilgilerinin Girilmesi:** 

1. **Gözlemci Bilgilerinin Girilmesi:** Uygulama ana menüden önce **Options** sekmesine daha sonra **General** sekmesine tıklanır. Astrometry başlığı altındaki **Observer** kutucuğuna gözlemcilerin isim ve soyisim baş harfleri büyük harfle 

olacak biçimde “-“ ile ayırarak sırayla yazılır. ( Örn:SB-BB-KB-EB) 

2. **Gözlem Klasörü Oluşturma:** “G:\Gözlemler\2026-01-01\Yıldız_Adı\BDF, MBDF“şeklinde ooluşturulur. Bdf; bias, dark, flat demektir kalibrasyon alınacağı zaman dosya yolu bu klasör olarak değiştirilir. 

3. **Gözlem Klasörünün Yolunu Belirtme:** Uygulama ana menüsünden önce **Options** sekmesine daha sonra **Imaging** sekmesine tıklanır. **“Image File Path”** kutucuğu görüntülerin kaydedileceği klasör yolunu belirtir. Yanındaki 3 nokta tuşuna tıklanır ve gözlem klasörü seçilir. (Not: Bir gecede birden fazla gözlem olacaksa veya kalibrasyon görüntüleri için farklı klasörler açılmışsa her seferinde dosya yolu değiştirilmelidir.) 

# **Flat Alma Aşamaları:** 

1. **Teleskobu Yönlendirme:** N.I.N.A. Ana sayfa menüsünden önce **Equipment** daha sonra **Mount** sekmesine gelinir. Sağ üstteki Altitude (Yükseklik) değerine **60 ile 85** arasında bir değer girilir. Azimut kısmına ise Güneş'in battığı yönün tersi olan bir ufuk açısı değeri yazılır ve **Slew** butonuna basılarak teleskop o yöne gönderilir. ( **Not1:** Azimut değeri akşam flatı alıancağı zaman güneş batıdan battığı için doğudan alınmalıdır. Sabah flatı alınacağı zaman ise güneş doğudan doğduğu için batıdan alınmalıdır. Bir çember düşündüğümüzde tepe kısmı kuzey zemin kısmı güney sağ taraf doğu ve sol taraf batı şeklinde düşünülmelidir. Kuzey için azimut değeri 0 veya 360 derecedir. Güney için 180, doğu için 90 ve batı için 270 derecedir yani akşam flatı alıncağı zaman 90 derece sabah flatı alıncağı zaman 270 derece yazılmalıdır.) ( **Not2:** Alt (Altitude) değeri için teleskopa doğrudan hiç güneş ışının gelmeyeceği ve homojenliği bozmayacak değer seçilmelidir. Düşük değerlerde dünyanın geoit şekli yüzünden atmosfer tabakası kalın olduğu için gelen ışınlar homojenlik şartını sağlamamaktadır. Yüksek değerler için ise doğrudan güneş ışını gelme ihtimali bulunduğu için 60 ile 85 derece arası bir değer girilmesi en optimum kalibrasyon sonucu verecektir.) 

2. **Kubbeyi Senkronize Etme:** Dome Control programına geçilir. Input yazan boşluğa, az önce teleskoba girdiğimiz aynı **Azimut** değeri yazılarak **GotoAzimuth** butonuna tıklanır. Kubbe, tam teleskobun baktığı yöne döner. 

3. **Takibi Durdurma (Kritik İşlem):** Flat alırken uzayı veya yıldızları değil, gökyüzünün homojen boşluğunu çekmek istiyoruz. Motor takibi açık kalırsa, belirmeye başlayan ilk yıldızlar görüntüde iz yapar. Bu durumu engellemk için ana sayfadan Mount sekmesindeki Set tracking rate yanındaki açılır pencereden, **Stopped** seçilir ve teleskobun motor takibi tamamen durdurulur. (POTH ekranından da "Track" tikinin kapalı olduğu teyit edilebilir). 

# 4. **Flat Sihirbazını Çalıştırma:** 

- N.I.N.A. ana menüsünden **Flat Wizard** sekmesi açılır. 

- Kullanılacak filtre sayısına göre **Single Mode** (tek filtre) veya **Multi Mode** (çoklu filtre, ör:B, V, R) seçilir. 

- Alt kısımdaki yeşil **Play (Başlat)** tuşuna basılarak işlem başlatılır. 

- _Not:_ Flat Sihirbazı ortam ışığına göre ideal poz süresini kendi hesaplar. Akşam saatlerinde Güneş battıkça gökyüzü yavaş yavaş karardığı için, yazılım her çektiği yeni karede poz süresini saniye saniye artırarak piksellerdeki ışık doygunluğunu (ADU) sabit tutar. 

# **Adım 4: Geometrik Çerçeveleme ve Veri Hedefleme (Simbad)** 

Amacımız sadece ana hedefi değil, onun ışık değişimini matematiksel olarak kıyaslayacağımız sabit yıldızları da aynı kadraja sığdırmaktır. 

1. **Görüş Alanı (FOV - Field of View):** Simbad açılır. Gözlenecek yıldız aranır ve görsel büyütülür. Ekranın sol tarafındaki imlece 1 kere dokununca seçilen yıldız için bilgileri gösterir. N.I.N.A Imaging ekranındaki kamera kadrajıyla birebir eşleşmesi için sol altta yazan FoV değeri18-20 aralığına getirilir. 

# 2. **Mukayese Yıldızlarının Seçimi:** 

   - Mukayese yıldız parlaklığı sabit ve tür olarak yıldız olmalıdır. 

   - Gözlencek yıldız ile seçilen 2 adet mukayese yıldızlar arasında parlaklıkları birbirine yakın olanlar seçilmelidir. (Not:Mag değeri parlaklığı kadir cinsinden ifade eder. _Unutma 9 kadir, 12 kadirden daha parlaktır)._ 

   - Birinci mukayese yıldızı kontrol etmek için 2. Mukayese Yıldız (Dened) seçilir. 

3. **Koordinat Tespiti (Kritik İşlem):** Hedef yıldız ve seçilen iki mukayese yıldızını aynı anda tam kadraja sığdıracak tahmini orta noktaya fare ile gidilir. Bu orta noktanın kaybolmaması için ekranın sol üst köşesindeki RA ve Dec verilerinin fotoğrafı çekilir. 

# **Adım 4: Teleskobun Yönlendirilmesi (Slew & Plate Solving)** 

1. **N.I.N.A.'ya Veri Girişi:** Çektiğimiz fotoğraftaki "orta nokta" koordinatları, N.I.N.A.'da **Framing** (Çerçeveleme) sekmesindeki koordinat alanına yazılıp Load Image denilir veya **Equipment** sekmesinden **Mount** başlığı altındaki **Target RA/Dec** kısmına girilir. 

2. **Hedefe Gidiş: Slew** butonuna basılır. Teleskop bu noktaya gönderilir ve yazılım Plate Solving (yıldız haritası eşleştirme) yaparak o üç yıldızı milimetrik olarak kadraja oturtur. 

# **Adım 5: Güvenlik Kontrolü ve Kubbe Senkronizasyonu (Stellarium)** 

Teleskop hareketini tamamladıktan sonra mekanik güvenlik ve kubbe hizalaması yapılır. 

1. **Güvenlik (Alt Değeri):** Stellarium programına girilir ve gözlenecek yıldızın **Alt (Altitude - İrtifa)** değerine bakılır. (Not _:_ Teleskobun 20 derecenin altına dönmesi mekanik olarak tehlikelidir, bu sınır mutlaka teyit edilir.) 

2. **Kubbe Hizalama (Az Değeri):** Stellarium'dan gözlenecek yıldızın **Az (Azimut)** değeri alınır. Masaüstündeki Dome Control paneline gelinir, Input yazan kısma bu 

Azimut değeri girilip **GotoAzimuth** butonuna tıklanarak kubbe yarığı tam teleskobun önüne getirilir. 

# **Adım 6: Auto Focus** 

Auto-Focus işleminin fizik labarotuvar "ortalama/grafik çizme" mantığıyla hatasız çalışabilmesi için yıldızların pikseller üzerinde kaymaması, yani motor takibinin aktif olması şarttır. 

1. **Takip Kontrolü:** POTH ekranından Track (Takip) kutucuğunun açık (işaretli) olduğu teyit edilir. _(Not: POTH acil durumlarda teleskoba müdahale için kullanılan köprüdür)._ 

2. **Geçici Kılavuz (Guiding):** PHD2 ekranında herhangi bir yıldıza dokunulur ve **yeşil ok (Start)** simgesine basılarak otomatik takip başlatılır. _(Teleskop üzerindeki o küçük kısım PHD2'ye görüntü verir)._ 

3. **Filtre:** N.I.N.A. üzerinden filtre tekerleğinin **CLEAR** konumunda olduğu kontrol edilir. 

4. **Odaklamayı Başlatma:** N.I.N.A. **Imaging** sekmesinden sağ üstteki **AF (Auto Focus)** butonuna basılarak Start denilir. 

   - _Veri Kalitesi Kuralı:_ İşlem bitince çizilen grafikteki Hyperbolic değer 0.5'ten küçük olmamalıdır. Eğer grafik düzgün çıkmadıysa PHD2 ile takip kontrol edilip Auto Focus tekrarlanır. 

   - _Donanım Teyidi:_ Auto Focus arayüzünde "Position" olarak gösterilen sayısal odak değeri ile duvardaki siyah Optec Focus cihazının üzerindeki yuvarlağın/ekranın gösterdiği değer birebir aynı olmalıdır. 

# **Adım 7: İdeal Poz Süresinin Tespiti (ADU Sayımı)** 

Sistemin kör olmaması (doyuma ulaşmaması) için doğru poz süresini (Time) tespit ediyoruz. 

1. **Test Çekimi:** Gereksiz veriler klasöre dolmasın diye Imaging sekmesinden sağ üstteki **Save** butonu **OFF** (Kapalı) yapılır. 

2. **İlk Analiz:** Poz süresi örneğin 10 saniye ayarlanıp çekim yapılır. Klasöre düşen görüntüde herhangi bir yıldıza tıklanır ve Ctrl + I (Information) ile Max sayım (ADU) değerine bakılır. Diyelim ki 16.000 saydı. Poz süresi **30 Saniye** yapılarak tekrar çekilir. Max değerine tekrar bakılır. Eğer sayım iyi bir değerdeyse, bu kameranın patlamadan (saturasyona uğramadan) toplayabileceği en ideal ve güvenli sinyal seviyesidir. 

3. Karar kılınan bu 30 saniyelik değer, Bölüm 3'teki programlama (Sequence) aşamasında kullanılmak üzere not edilir. 

# **Adım 8: Gözlem Şablonunun Kurulması (Advanced Sequencer)** 

İnsan müdahalesini devreden çıkarıp, sistemi sabaha kadar veri toplamaya programladığımız aşamadır. 

1. **Sequencer'a Geçiş:** N.I.N.A. ana menüsünden Sequencer > Advanced Sequencer sekmesi açılır. 

2. **Veri Kapsayıcısı:** Ana fonksiyon bloğu olan **Variable Star Object Container** çalışma alanına alını **r.** 

   - İçerisine hedef yıldızın adı yazılır. 

   - RA ve Dec kısımlarına ise Simbad'dan fotoğrafını çektiğimiz o "tahmini orta noktanın" koordinatları manuel olarak girilir. 

3. **Güvenlik Ağı (Triggers):** Kapsayıcının sol üst köşesindeki Triggers kısmına, olası bulut geçişlerinde veya takip kayıplarında sistemi kurtarması için **Restore Guiding** ve **Set Tracking** bileşenleri eklenir. 

4. **Zaman Döngüsü (Loop Condition):** Stellarium'dan veya sistem grafiğinden hedefin 20 derece altına ineceği veya batacağı süre hesaplanır. Kapsayıcının içindeki Loop Condition kısmına **Loop for Time** eklenip bu 5 saatlik döngü süresi tanımlanır. 

5. **Talimatlar (Instructions) ve Matematiksel Poz Planı:** Kapsayıcının talimatlar kısmına yukarıdan aşağıya şu bloklar dizilir: 

   - **Slew and center:** Hedefi merkeze almak için. 

   - **Start Guiding:** PHD2 takibini başlatmak için. 

   - **Take Many Exposures:** Çekim bloğudur. Test aşamasında bulduğumuz 30 saniye değeri Time (süre) kısmına yazılır. Count (Miktar) için rasyonel hesap yapılır. 30 saniyede 1 adet, 1 dakikada 2 adet, 1 saatte 120 adet poz çekilir. 5 saatlik gözlem için miktar boşluğuna 600 yazılır. 

6. **Veri Kaydı Aktivasyonu:** Deneme çekimleri (sayım tespiti) sırasında veriler diske dolmasın diye Imaging ekranının sağ üstünden kapattığımız Save butonu artık ON (Açık) konumuna getirilir. (Kapalı unutulursa sabaha kadar çekilen hiçbir veri kaydedilmez). 

7. **Gözlemi Başlatma:** Sağ alttaki Play (Çalıştır) butonuna basılarak otonom gözlem başlatılır. Ham veriler doğrudan klasörüne akmaya başlar. 

# **Adım 9: Mekanik Sistemlerin Park Edilmesi ve Bağlantıların Kesilmesi** 

Teleskobun ve kubbenin, eksenlerini sıfırlaması (homing) ve kapalı konumda kalması gerekir. Bu işlem yapılmadan sistem kapatılırsa, teleskop uzaydaki referans noktasını kaybeder. 

1. **Kubbe (Dome):** Masaüstündeki Observa Dome (Dome Control System) uygulamasına geçilir. 

   - Öncelikle kubbeyi başlangıç noktasına döndürmek için **Park Dome** butonuna tıklanır. 

   - Ardından **Enable** kutucuğundaki işaret kaldırılarak N.I.N.A.'nın otomatik kontrolü devre dışı bırakılır. 

   - Son olarak **Disconnect** tuşuna basılarak kubbe ile olan yazılım bağlantısı koparılır. 

2. **Teleskop (Mount):** N.I.N.A. arayüzünde Equipment > Mount sekmesine gidilir. 

   - Sağ alt köşedeki **Park** butonuna tıklanarak teleskop park konumuna getirilir. 

   - Teleskop hareketini bitirdikten sonra üst kısımdaki açma/kapama (güç) simgesine tıklanarak mount bağlantısı sonlandırılır. 

# **Adım 10: Teleskop Kapağının Kapatılması ve Dark/Bias Verilerinin Alınması** 

- Dark ve Bias kalibrasyon kareleri alınırken sensöre dışarıdan tek bir fotonun dahi düşmemesi gerekir, bu yüzden bu işlem yapılmadan önce teleskobun fiziksel kapağı kapatılmalıdır. Teleskop park edildiği için artık kubbeye çıkıp teleskobun kapağını ve kubbeyi mekanik olarak kapatılmalıdır. 

# **Adım 11: Dark ve Bias Verilerinin Alınması** 

# **Dark ve Bias Hakkında Genel Bilgiler:** 

- **Dark Frame:** Sensör, -20°C'de soğutulsa bile, uzun pozlamalarda elektronik devrenin kendi ısısından kaynaklanan bir "Termal Gürültü" (Dark Current) üretir. Ana görüntülerle (Light) aynı sıcaklıkta ve aynı poz süresinde ama kapak kapalıyken çekilen siyahtan oluşan matrislerdir. 

- **Bias Frame:** Kameranın sensöründeki veriyi bilgisayara okurken yarattığı anlık elektronik okuma gürültüsüdür (Read Noise). Aynı sıcaklıkta, kameranın çekebildiği _en kısa sürede_ kapak kapalıyken çekilir. 

# **Dark ve Bias Alma Prosedürü:** 

1. N.I.N.A. ana menüsünden Sequencer sekmesi tıklanır ve Target Set (Legacy) açılır. 

2. Ekranda görünen hedef seçeneklerinin (Slew to target, Center target, vb.) hepsinin **OFF** (kapalı) olduğundan emin olunur. 

3. Sol alt taraftaki **"+"** tuşuna basılarak bir işlem satırı eklenir. 

4. Alınması gereken kare sayısı **Total** kısmına ve poz **süresi** Tıme kısmına girilir. 

5. **Type** kısmından alınacak kalibrasyon verisine göre **DARK** veya **BIAS** seçilir. 

6. Başlat tuşuna basmadan önce, Options > Imaging sekmesinden dosya kayıt yolunu (Image File Path) sadece bu kalibrasyon dosyalarının kaydedileceği yeni bir klasör olarak değiştirmelisin (Bdf klasörü). Aksi takdirde ana veri klasörüne karışır. 

7. Sağ alt köşedeki **Play** (Çalıştır) tuşuna basılarak kalibrasyon verileri alınır. 

# **Adım 12: Yardımcı Donanımların Kapatılması** 

Kalibrasyon verileri diske yazıldıktan sonra alt sistemler kapatılır. 

1. **Guider (PHD2):** Arka planda açık olan PHD2 Guiding uygulamasından **Camera** ve **Mount** seçeneklerinin bağlantısı kesilir. Ardından N.I.N.A.'da Equipment > Guider menüsünden güç simgesine tıklanarak takip bağlantısı tamamen koparılır. 

2. **Focuser & Filtre:** Sırasıyla Equipment > Focuser ve Equipment > Filter Wheel sekmelerine girilip güç (açma/kapama) simgelerine tıklanarak bu mekanizmalarla bağlantı kesilir. 

3. **Isıtma (Warming):** N.I.N.A.'da Equipment > Camera sekmesine girilir. "Temperature control" başlığı altındaki **Alev (Isıtma) simgesine** tıklanır. Yazılım, sensörün sıcaklığını kademeli ve kontrollü bir şekilde ortam sıcaklığına kadar çıkarır. Bu sürecin bitmesi beklenmelidir. Kamera güvenli sıcaklığa ulaştıktan sonra, kameranın ana **Güç** simgesine tıklanarak cihaz bağlantısı kesilir. 

4. Tüm donanım bağlantıları güvenle kesildikten sonra N.I.N.A. programı kapatılarak operasyon tamamen sonlandırılır. 

# **<mark>Genel Gözlem-Rasathane Soru-Cevap:</mark>** 

# **Bilimsel Açıdan Flat, Dark Ve Bias Nedir?** 

# **CCD Çalışma Mantığı ve Kalibrasyonun Fiziksel Temeli:** 

Astronomide kullandığımız CCD (Charge-Coupled Device) kameralar, akıllı telefonlarımızdaki sensörlerle temelde aynı fiziksel prensiple çalışır. Buna “Fotoelektrik Olay” denir. 

- Sensörün en üst katmanında hassas bir silikon tabaka bulunur. Uzaydan gelen fotonlar (ışık tanecikleri) bu silikon tabaka yüzeyine çarptığında atomlardan elektron koparır. 

- Koparılan bu elektronlar, pikseller adı verilen potansiyel-elektron kuyularında birikmeye başlar. 

- Pozlama süresi bittiğinde okuma (Readout) işlemi başlar. Örneğin 1024x1024 piksellik bir matriste, sütunlar boyunca uygulanan potansiyel farklar (voltaj dalgaları) yardımıyla elektronlar sıra sıra en kenardaki (1025.sütun veya satır) okuma yazmacına (register) aktarılır ve burada elektronlar sayılır. 

- Donanımın kendi içinde ürettiği akım değerinin dijital karşılığına ADU (Analog-toDigital Unit) yani _sayım_ denir. Kameranın uyguladığı voltaj ile elde edilen akım ( _V_ = _I ⋅ R_ mantığıyla) işlenerek piksellerdeki toplam yük dijital birime çevrilir. 

İşte tam bu noktada, yıldızdan gelen gerçek fotonlar ile kameranın kendi donanımından, sıcaklığından veya optik kusurlarından kaynaklanan sahte sinyalleri birbirinden ayırmak zorundayız. Kalibrasyon dediğimiz olay tam olarak bu safsızlıkları temizleme matematiğidir. Kısaca kameranın piksellerine-elektron kuyularına dolan yıldızdan gelmeyen kameranın kusurlarından dolayı fazlalık olan elektronları temizlemektir. 

# **1. BIAS: Elektronik Okuma Gürültüsünün Haritası** 

- Fiziksel Arka Plan: Sensördeki elektronları okumak için uygulanan potansiyel fark ve devre elemanlarının kendisi, dışarıdan hiç ışık gelmese bile anlık elektriksel parazitler (okuma gürültüsü) üretir. 

- Nasıl Alınır? Teleskobun kapağı (shutter) tamamen kapalıyken, kameranın desteklediği en kısa (sıfıra en yakın) poz süresinde çekilir. Teknik olarak "0 saniye" denilen bu süre, aslında sistemin tek bir okuma döngüsünü gerçekleştirdiği anlık süredir. 

- Amacı: Yıldızdan gelmeyen, tamamen kameranın okuma devrelerinin yarattığı o anlık taban gürültüsünü (elektron sayısını) ölçüp veriden izole etmektir. 

# **2. DARK: Termal Işıma ve Isınma Gürültüsü** 

- Fiziksel Arka Plan: Termodinamiğin temel kuralına göre, mutlak sıfırdan (-273.15°C / 0 Kelvin) farklı sıcaklığa sahip her cisim ışıma yapar. Kameralarımızı ne kadar soğutsak da (örneğin -20°C veya -100°C'ye kadar), sensör çalışırken ısınır ve yarı iletken malzemedeki elektronlar termal enerji nedeniyle uyarılır. Bu 

durum, dışarıdan hiç foton gelmese bile piksellerde sahte elektronların birikmesine (Dark Current) yol açar. 

- Nasıl Alınır? Teleskobun fiziksel kapağı kapalıyken, asıl gözlemde kullandığımız poz süresiyle ve birebir aynı sensör sıcaklığında çekilir. 

- Amacı: Yıldızdan gelmeyen, tamamen kameranın kendi ısı enerjisinden dolayı poz süresi boyunca ürettiği fazladan elektron sayısını (termal gürültüyü) ölçüp matristen çıkarmaktır. 

# **3. FLAT: Piksellerin Kuantum Tepki Matrisi** 

- Fiziksel Arka Plan: Sensörleri oluşturan pikseller mikron seviyesinde, hatta günümüz teknolojisinde atom boyutunda transistörler barındıran kuantum yapılı hassas cihazlardır. Fabrika çıkışlı bile olsa hiçbir piksel ışığa aynı tepkiyi vermez (Buna Kuantum Etkinliği - Quantum Efficiency denir; örneğin 100 foton düştüğünde kimi piksel %80'ini, kimi %40'ını algılar). Ayrıca cam üzerindeki mikroskobik tozlar ve optik vinyet (kenar kararması) bu tepkiyi daha da bozar. Piksellerin bu değişken duyarlılığını ölçmenin tek yolu, üzerlerine homojen bir ışık düşürmektir. 

- Nasıl Alınır? Güneş ufkun tamamen altına indikten sonra (doğrudan gelen sert Güneş ışınlarından kaçınmak için ufuk seviyesinde değil, atmosferik homojensizliği atlatmak adına 60°-85° irtifa aralığında, Güneş'in ters istikametinde) homojen aydınlanmış gökyüzü fonu taranarak alınır. En garantisi hem akşam hem sabah almaktır. 

- Amacı: Piksellerin ışığa nasıl tepki verdiğini matematiksel olarak sabitlemek, toz ve kenar kararması lekelerini ortadan kaldırarak sensörün her bölgesini eşit duyarlılık seviyesine getirmektir. 

Özetle: Bias kameranın _anlık okuma gürültüsünü_ , Dark _zamanla biriken ısı gürültüsünü_ , Flat ise _piksellerin ışığa verdiği farklı tepki ve optik kusurları_ yakalar. Bu üçlü olmadan saf ve hatasız bir astrofiziksel veri üretmek imkansızdır. 

# **Flat Almanın Amacı Nedir?** 

Gökyüzünün yıldızlar belirmeden hemen önceki pürüzsüz ve homojen aydınlığını kullanarak aslında uzayı değil, doğrudan kendi donanımımızın kusurlarını fotoğraflamış oluruz. Bu işlemin veri kalitesini maksimize eden üç rasyonel sebebi vardır: 

- **Kenar Kararmasını (Vignetting) Eşitlemek:** Optik fiziğin doğası gereği, sensörün (kameranın) tam merkezi daha fazla ışık alırken, köşelere doğru ışık miktarı azalır. Flat verisi, bu kararmayı hesaplayıp görüntünün her köşesini aynı parlaklık seviyesine (matematiksel olarak) eşitler. 

- **Toz Lekelerini (Dust Donuts) Yok Etmek:** Teleskobun aynasında, filtrelerinde veya sensörün camında bulunan mikroskobik toz taneleri, alınan uzun pozlu görüntülerde dairesel siyah lekeler (donut) yaratır. Flat çekimi bu lekelerin yerini milimetrik olarak tespit eder. 

- **Piksel Duyarlılığını (Sensitivity) Standardize Etmek:** Sensördeki milyonlarca pikselin, üzerine düşen fotonları elektrik sinyaline dönüştürme kapasitesi birebir aynı değildir. Bazı pikseller daha hassas, bazıları daha sağırdır. Homojen bir ışık çekildiğinde, hangi pikselin ne kadar saptığı ölçülür. 

# **Veri Analizi Rasyoneli (Arka Plandaki Matematik)** 

Gözlemden elde ettiğin ham uzay fotoğrafı (Light Frame) tek başına analiz edilemez. Veri işleme aşamasına geçildiğinde (örneğin Python ile veriyi temizlerken), yazılım şu mantıkla çalışır: 

Ana görüntüdeki her bir piksel değeri, Flat görüntüsündeki ilgili piksel değerine **bölünür** . Bu bölme işlemi sayesinde; toz lekeleri ve kenar kararmaları denklemden çıkarak "1"e eşitlenir (normalize edilir). Geriye sadece yıldızlardan veya galaksilerden gelen gerçek ve pürüzsüz foton verisi (saf sinyal) kalır. 

# **Dark Ve Bias Nasıl Alınır?** 

# **1. DARK (Karanlık) Matrisi Nedir ve Nasıl Alınır?** 

İşin Fiziği (Termal Gürültü): Sensör ışık toplarken aynı zamanda çalışmaktan dolayı ısınır. Kamerayı eksi derecelere soğutsak bile, yarı iletken malzemedeki elektronlar kendi kendilerine uyarılıp sanki uzaydan ışık gelmiş gibi bazı pikselleri parlatır (Buna "Dark Current / Karanlık Akım" ve "Hot Pixel / Sıcak Piksel" denir). Bizim amacımız, kapağı tamamen kapatıp uzay ışığını keserek sadece bu "ısınma haritasının" fotoğrafını çekmektir. 

# **Altın Kurallar:** 

- Aynı Sıcaklık: Ana gözlemi hangi derecede yaptıysan (-15°C veya -20°C), Dark da milimetrik olarak aynı sıcaklıkta alınmalıdır. 

- Aynı Süre: Ana hedefin poz süresi (Time) 30 saniye ise, Dark poz süresi de kesinlikle 30 saniye olmak zorundadır. (Çünkü ısı gürültüsü zamanla birikir). 

# **N.I.N.A.'da Adım Adım Dark Çekimi:** 

1. Kapağı Kapat: Teleskop park konumundayken, teleskobun ucundaki fiziksel kapağı KESİNLİKLE kapat. İçeri tek bir foton bile sızmamalı. 

2. Menüye Giriş: N.I.N.A. sol menüsünden klasik Sequencer (Target Set) ekranını aç. 

3. Güvenlik: Hedefe yönelmemesi için ekrandaki Slew to target ve Center target gibi tüm yönlendirme tuşlarını OFF (kapalı) konumuna getir. 

4. Dosya Yolu: Verilerin ana fotoğraflarla karışmaması için Options > Imaging sekmesinden kayıt klasörünü BDF (Bias Dark Flat) olarak seçtiğinden emin ol. 

# 5. Parametreleri Gir: 

   - Type (Tür) menüsünden DARK seçeneğini tıkla. 

   - Time (Süre) kısmına ana hedefinle aynı süreyi, yani 30 yaz. 

   - Count (Miktar) kısmına istatistiksel bir ortalama (Master Dark) oluşturabilmek için en az 20 veya 30 yaz (Ne kadar çok, o kadar pürüzsüz gürültü haritası demek). 

6. Oynat (Play) tuşuna bas. Makine 30'ar saniyelik simsiyah fotoğraflar çekip klasöre dizecektir. 

# **2. BIAS (Okuma Gürültüsü) Matrisi Nedir ve Nasıl Alınır?** 

Sensördeki pikseller dolduktan sonra, bu elektrik yükünün dijital sayılara (ADU) çevrilip bilgisayara "okunması" gerekir. Ancak işlemci (ADC) bu veriyi okurken mükemmel çalışmaz; her seferinde en tabana mikroskobik bir elektriksel parazit ekler. Bias (Okuma Gürültüsü), zaman veya ısıyla ilgili değildir; anlıktır ve saniyenin sıfırıncı anında gerçekleşir. 

# **Altın Kurallar:** 

- Sıfır Saniye: Sürenin okuma işlemine karışmaması için kameranın desteklediği en kısa poz süresi (0 saniye) ile çekilir. 

- Aynı Sıcaklık: Elektronik direnç sıcaklıkla değiştiği için, Bias da yine ana verilerle aynı eksi derecede alınmalıdır. 

# **N.I.N.A.'da Adım Adım Bias Çekimi:** 

1. Kapak Kapalı: Dark çekerken olduğu gibi teleskobun fiziksel kapağı sımsıkı kapalı kalmaya devam eder. 

2. Menü: Yine klasik Sequencer (Target Set) ekranındayız. Tüm Slew/Center yönlendirme ayarları hala OFF durumunda. 

3. Parametreleri Gir: 

   - Type (Tür) menüsünden BIAS seçeneğini tıkla. 

   - Time (Süre) kısmı N.I.N.A.'da Bias seçildiğinde otomatik olarak sıfırlanabilir veya kilitlenebilir. Eğer manuel girmeni isterse kameranın desteklediği en düşük rakamı (örneğin 0 veya 0.001) yaz. 

   - Count (Miktar) kısmına yine iyi bir Master Bias oluşturmak için 30 ile 50 arası bir rakam gir (Çok hızlı çekileceği için fazla sayı girmek zaman kaybettirmez). 

4. Oynat (Play) tuşuna bas. Kameran saniyeler içinde takır takır taban gürültüsü haritalarını çekip BDF klasörüne yollayacaktır. 

# **Gözlem Prosedürü Hakkında Genel Bilgiler:** 

N.I.N.A. yazılımında Sequence (Gözlem Prosedürü), manuel müdahaleye gerek kalmadan tüm gece boyunca otomatik gözlem yapılmasını sağlayan bir görev listesidir. Bu listede, hangi hedefin ne kadar süreyle ve hangi ayarlar (pozlama süresi, poz sayısı, filtreler vb.) kullanılarak gözleneceği tanımlanır. 

Eksiksiz bir şablon oluşturmak ve yönetmek için izlenmesi gereken adımlar şunlardır: 

# **1. Advanced Sequencer Menüsüne Giriş** 

- Uygulamanın sol menüsünde yer alan "Sequencer" seçeneğine tıklanır. 

- Ardından açılan ekrandan "Advanced Sequencer" seçeneği tıklanır. 

- Bu ekranda, sağ tarafta yer alan araçlar sürükle-bırak yöntemiyle orta kısımdaki çalışma alanına (Sequence Target Area) taşınarak gözlem prosedürü oluşturulur. 

# **2. Temel Şablon Bileşenlerinin Eklenmesi ve İşlevleri** 

Gözlemin kusursuz ilerlemesi için şablona şu bileşenler dahil edilir: 

- **Variable Star Object Container:** Gözlem yapılacak cisme dair "Object name", "RA" (Sağ Açıklık), "Dec" (Dik Açıklık) ve "Hedef Yükseklik Grafiği" gibi gerekli alt bileşenleri içeren ana komut kutucuğudur. 

- **Slew and Center:** Teleskobu girilen koordinatlara yönlendiren (gönderen) bileşendir. 

- **Start Guiding ve Stop Guiding:** Teleskop hedefe gittiğinde görüntü almaya başlamadan önce takibi başlatmak için Start Guiding, gözlem bitiminde ise takibi durdurmak için Stop Guiding bileşeni kullanılır. 

- **Switch Filter:** Filtre tekerini kontrol edebilmeyi ve istenilen filtreye geçilmesini sağlayan bileşendir. 

- **Take Many Exposures:** CCD görüntülerini almak için kullanılır. Bu bileşen üzerinden kaç poz alınacağı, kaç saniye poz süresi verileceği ve hangi binning değerinin kullanılacağı tanımlanır. 

- **Loop Condition (Döngü Koşulu):** Döngünün ne zamana veya hangi duruma kadar devam edeceğini belirler. Bütün döngü bileşenleri sadece "instruction 

set"lerdeki "loop" bölgelerine taşınabilmektedir. Örneğin; **"Loop Until Time"** bileşeni, internetten çekilen zaman bilgisini kullanarak astronomik tan veya sivil tan gibi istenilen saate kadar döngünün devam etmesini sağlar. 

# **3. Triggers (Koşullu Acil Durum Bileşenleri)** 

Yanında yıldırım simgesi bulunan bileşenler koşulludur ve yalnızca "global triggers" bölgesine veya "instruction set"lerdeki "triggers" alanlarına taşınabilir. 

- **Restore Guiding:** Kılavuz kamerasının referans yıldızını çerçeveden kaybetmesi veya sinyal/gürültü (SNR) oranının azalması gibi sebeplerle Guiding durduğunda, takibi otomatik olarak yeniden çalıştırır. 

- **Set Tracking:** Özellikle flat görüntüleri alınırken takip modu kapatılmışsa, tedbir amaçlı olarak yıldız takibini tekrar başlatmayı sağlayan bileşendir. 

# **4. Hazır Şablon Yükleme ve Düzenleme** 

Sıfırdan prosedür kurmak yerine, önceden hazırlanmış bir şablonu yükleyip düzenlemek daha güvenilir bir yöntemdir: 

- "Advanced Sequencer" ekranına girildikten sonra yükleme kutucuğuna tıklanarak bilgisayardaki hazır şablon seçilir ve "Open" ile açılır. 

- Target Name kısmına "Yıldız_İsmi" formatında hedefin adı girilir. 

- Variable Star Object Container içerisindeki RA ve Dec alanlarına yıldızın koordinatları girilir. 

- Loop until Time alanına ne kadar süreyle gözlem yapılacağı girilir. 

- Start Guiding bloğunun altındaki Switch Filter bloğundan gözlemde kullanılacak filtre seçilir. Eğer kullanılmayacak başka Switch Filter blokları varsa, yanlarındaki çöp kutusu simgesine tıklanarak silinir. 

- Take Many Exposures bloğuna istenilen poz sayısı ve pozlama süresi girilir. 

- Tüm kontroller yapıldıktan sonra sağ altta bulunan çalıştırma (oynat) simgesine tıklanarak gözlem otomatik olarak başlatılır. 

# **Gözlem Prosedürü Nasıl Oluşturulur?** 

Sağ menüden sürükleyip orta alana (çalışma alanına) bırakacağımız blokların mantıksal hiyerarşisi ve sıralaması şu şekilde olmalıdır: 

# **1. Ana Kapsayıcı (Main Function)** 

İlk olarak çalışma alanına en temel taşıyıcı bloğu ekliyoruz. 

- **Variable Star Object Container:** Bu bizim ana fonksiyonumuzdur. Basit bir Sequential Instruction Set yerine bunu kullanmamızın sebebi; hedefin adını, RA ve Dec koordinatlarını ve hedef yükseklik grafiğini kendi içinde barındıran gelişmiş bir yapı olmasıdır. 

# **2. Hata Ayıklama (Exception Handling / Triggers)** 

Oluşturduğumuz ana kapsayıcının (Container) sol üstünde bir Triggers (Tetikleyiciler - Yıldırım simgesi) alanı bulunur. Bu alan bizim güvenlik ağımızdır. 

- **Restore Guiding:** Kapsayıcının Triggers kısmına eklenir. Herhangi bir sebepten (bulut geçişi vs.) SNR (Sinyal/Gürültü) düşerse veya yıldız çerçeveden çıkarsa Guiding durabilir; bu bileşen koşullar düzeldiğinde takibi otomatik olarak yeniden başlatır. 

- **Set Tracking:** Yine Triggers kısmına eklenir. Flat görüntüsü alımı sonrasında motor takibi kapalı unutulmuşsa, sistemi korumak adına yıldız takibini tekrar başlatır. 

# **3. Döngü Koşulu (While Condition / Loop)** 

Kapsayıcının içinde Loop Conditions (Döngü Koşulları) adlı özel bir alan bulunur. Veri toplama işleminin ne zaman sonlanacağını burası belirler. 

- **Loop Until Time:** Döngü alanına sürüklenir. İnternetten çekilen saat verisine göre (örneğin "Astronomik Tan" vaktine kadar) altındaki talimatların sürekli tekrarlanmasını sağlar. Farklı senaryolar için Loop for Time Span (belirli bir süre boyunca) veya Loop for Iterations (belirli bir tekrar sayısı) gibi alternatifler de mevcuttur. 

# **4. İşlem Adımları (Instructions / Payload)** 

Kapsayıcının Instructions (Talimatlar) kısmına ekleyeceğimiz bileşenler, kronolojik olarak yukarıdan aşağıya doğru sırayla çalıştırılır. Buradaki sıralama fiziki bir zorunluluktur: 

1. **Slew and center:** Teleskobun önce girilen koordinatlara gitmesi ve hedefi merkeze alması gerekir. Bu nedenle talimat listesinin en başına eklenir. 

2. **Start Guiding:** Hedef merkezlendikten sonra, görüntü alımına başlanmadan hemen önce kılavuz (takip) kamerasının devreye girmesi gerekir. İkinci sıraya eklenir. 

3. **Switch Filter:** Takip başladıktan sonra, ışığın hangi dalga boyunda toplanacağını belirlemek için filtre tekerini kontrol eden bu blok eklenir (örneğin CLEAR filtresi seçilir). 

4. **Take Many Exposures:** Filtre ayarlandıktan sonra, asıl veriyi çeken komuttur. Kaç adet poz alınacağı, süresi ve binning değeri buraya girilir. CCD görüntüleri bu bileşenle alınır. 

(Not: Eğer gecenin planında birden fazla filtreyle veri alınacaksa, Take Many Exposures bloğunun hemen altına yeni bir Switch Filter ve onun altına tekrar Take Many Exposures eklenerek bu zincir uzatılır. Kullanılmayacak filtre blokları ise yanlarındaki çöp kutusu simgesi ile silinmelidir.) 

Bu hiyerarşiyi (Kapsayıcı -> Tetikleyici -> Döngü Koşulu -> Talimatlar Dizisi) bir kez rasyonel olarak kurduğunda, oluşturduğun bu algoritmayı şablon olarak kaydedebilir ve ileride sadece koordinat/süre değiştirerek tüm gözlemlerini tam otomasyonla yürütebilirsin. 

# **Örnek Gözlem Prosedürü:** 

Bu algoritmik yapıyı somut, rasyonel bir gözlem senaryosu üzerinden örneklendirelim. Hedefimiz, astronomik verisini (ışık eğrisini) analiz edeceğimiz bir "Değişen Yıldız" olsun ve sabaha kadar "CLEAR" filtresiyle aralıksız veri toplayalım. 

N.I.N.A. arayüzünde "Advanced Sequencer" ekranını açtığını ve sağ taraftaki bileşen menüsünü kullandığını varsayarak adım adım ilerliyoruz: 

# **Senaryo: V0332_Cyg Değişen Yıldız Gözlemi** 

# **1. Ana Çerçeveyi (Kapsayıcıyı) Oluşturma** 

- Sağ menüden **Variable Star Object Container** bileşenini sürükleyip orta çalışma alanına bırakıyoruz. 

- Target Name: V0332_Cyg yazıyoruz. 

- RA / Dec: Yıldızın koordinatlarını (örn. RA: 20 15 30, Dec: +45 10 00) ilgili alanlara giriyoruz. 

# **2. Güvenlik Ağını (Triggers) Kurma** 

- Sağ menüdeki koşullu bileşenlerden **Restore Guiding'i** sürükleyip, Variable Star Object Container'ın sol üstündeki Triggers (Tetikleyiciler) alanına bırakıyoruz. (Bulut geçerse takip kopmasın diye). 

- Hemen altına Set Tracking bileşenini de aynı Triggers alanına ekliyoruz. (Motor takibi güvenceye alınır). 

# **3. Veri Toplama Döngüsünü (Loop) Belirleme** 

- Sağ menüden **Loop Until Time** bileşenini sürükleyip, kapsayıcının içindeki Loop Conditions kısmına bırakıyoruz. 

- Zaman seçeneğini Astronomik Tan (veya bitmesini istediğin spesifik bir saat) olarak ayarlıyoruz. (Sistem bu saate kadar aşağıdaki işlemleri tekrarlayacak). 

# **4. Operasyonel Talimatları (Instructions) Sıralama** 

Kapsayıcının Instructions kısmına, yukarıdan aşağıya doğru tam olarak şu sırayla bileşenleri ekliyoruz: 

- 1. **Slew and center:** Sağ menüden sürükleyip en başa koyuyoruz. (Teleskop önce V0332_Cyg koordinatına gidecek ve hedefi piksel merkezine oturtacak). 

- 2. **Start Guiding:** Altına bunu ekliyoruz. (Hedef merkezlendi, artık Dünya'nın dönüşünü sıfır hatayla takip etmeye başlıyoruz). 

- 3. **Switch Filter:** Altına ekleyip, açılır menüden CLEAR filtresini seçiyoruz. (Gelen tüm fotonları maksimum sinyalle almak için). 

- 4. **Take Many Exposures:** En alta bu asıl veri toplama bloğunu ekliyoruz. 

   - Count (Miktar): 100 yazıyoruz. 

   - Time (Süre): 60 (saniye) yazıyoruz. 

   - Type (Tür): LIGHT seçiyoruz. 

(Eğer aynı hedeften BESSEL-V filtresiyle de veri almak isteseydik, bu son bloğun altına yeni bir Switch Filter (BESSEL-V) ve yeni bir Take Many Exposures daha ekleyecektik. Şablonda kullanmayacağımız fazla filtre blokları varsa yanlarındaki çöp kutusuna tıklayıp siliyoruz.) 

Sonuç: Sağ alttaki Play (Çalıştır) tuşuna bastığında; sistem V0332_Cyg hedefine dönecek, kendini hizalayacak, takibi başlatacak, filtreyi CLEAR yapacak ve astronomik tan vaktine kadar 60'ar saniyelik pozlar halinde .FITS veri matrislerini senin için diske yazacaktır. Bu tamamen insan müdahalesinden arındırılmış, rasyonel bir veri toplama kurgusudur. 

# **Adu Nedir?** 

ADU, İngilizce Analog-to-Digital Unit (Analogdan Dijitale Dönüşüm Birimi) kelimelerinin kısaltmasıdır. Rasathanede pratik dilde buna genellikle "Sayım" (Count) deriz. 

# **Olayın arka plandaki fiziksel ve dijital mantığı şu şekilde işler:** 

- Fotonun Düşüşü: Uzaydan gelen ışık (fotonlar) teleskoptan geçer ve kameranın sensöründeki minik piksellere çarpar. 

- Elektrona Dönüşüm: Piksel, bu fotonları hapseder ve fiziksel bir elektrik yüküne (analog sinyale) çevirir. 

- Sayısal Veri (ADU): Kameranın içindeki dönüştürücü işlemci (ADC - Analog to Digital Converter), bu elektrik yükünü ölçer ve senin bilgisayar ekranında okuyabileceğin dijital bir sayıya dönüştürür. İşte bu sayıya ADU (Sayım) denir. 

# **16-Bit Kamera Matematiği:** 

Kullandığınız bilimsel astronomi kameraları genellikle 16-bit veri üretir. Bu da bir pikselin alabileceği ADU (sayım) değerinin matematiksel olarak 0 ile 65.535 arasında olması demektir. 

- 0 ADU: Piksele hiç ışık düşmemiştir (Simsiyah). 

- 65.535 ADU: Piksel alabileceği maksimum ışığı almış, ağzına kadar dolmuş ve taşmıştır (Bembeyaz). Astronomide buna Saturasyon (Doyuma Ulaşma) denir. 

# **Gözlemdeki Rasyonel Önemi Nedir?** 

Rehberde ADU veya "sayım" değerine baktığımız iki kritik yer vardı, işte veri analizi açısından sebepleri: 

1. Doğru Poz Süresini (Time) Belirlerken: Deneme çekimi yapıp yıldızın Max Sayımına (ADU) bakıyoruz demiştik. Eğer çektiğin yıldızının pikseli 65.535 ADU değerine ulaştıysa, o piksel "patlamış" demektir. Taşan bir bardağa sonradan ne kadar daha su eklendiğini ölçemeyeceğin gibi, doymuş bir yıldızın parlaklık değişimini de (ışık eğrisini) ölçemezsin. 

2. Flat Alırken: Flat Wizard neden ortam ışığı karardıkça poz süresini kendi artırıyor? Çünkü yazılımın amacı, o pürüzsüz gökyüzü fonunun ortalama sayım değerini (ADU'sunu) 65.535'e vurdurmadan, tam ortalarda (genelde 25.000 ile 35.000 ADU arasında) homojen ve güvenli bir seviyede tutmaktır. 

Kısacası ADU; uzaydan gelen fiziksel ışığı, senin AstroImageJ'de analiz edebileceğin somut matematiksel sayılara dönüştüren yegane ölçü birimidir. 

