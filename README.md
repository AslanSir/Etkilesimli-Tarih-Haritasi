# Etkileşimli Tarih Haritası

### Program, açık kaynak kodlu ve tamamen düzenlenebilir şekilde __"Ali ASLANMİRZA"__ tarafından kodlanmıştır.

Bu rehberde programın üstünkörü olarak nasıl düzenlenebileceğini ve kendi haritanız üzerinde, kendi istediğiniz savaşları kendi videolarınızda nasıl gösterebileceğinizi anlatacağım.

## Başlangıç

- İlk başta kodu açmak ve düzenlemek için bilgisayarınızda __"Visual Studio"__ kurulu olmalı. Proje Visual Studio 2022'de kodlandı fakat diğer sürümlerle de birkaç küçük ayarla açabilirsiniz.
- Üstteki bölümden kodun tamamını .rar uzantılı olarak yüklemek için __"Program"__ klasörüne girin ve parça parça olan .rar uzantılı dosyaların hepsini indirin.
- İndirdiğiniz bütün dosyaların hepsini birden seçip __"Buraya ayıkla"__ seçeneğine tıklayın.
- Ardından çıkacak __"Etkileşimli Tarih Haritası"__ klasöründeki .sln uzantılı dosyaya çift tıklayarak programı Visual Studio üzerinden açın.
- Projenin bütün sayfaları formun ortasındaki __"bunifuPages1"__ in içerisinde. Bu sayfalara bunifupages'in sol altındaki (ayarlı değilse sol üstündeki) beyaz yazılı butonlarla ulaşabilirsiniz.

(Bunifu crack, yani açıp kodu düzenlemeniz için bunifu lisansına gerek yok.)

## Harita Değiştirme

- Bunifupages içerisinde __"haritalar"__ kısmında inaktif haritaları silip, geriye kalan aktif haritanın picturebox'ına kendi haritanızı yükleyin. (Kodu değiştirmeyin)
- Bunifupages içerisindeki __"Turkiye"__ kısmına girip Türkiye haritasının olduğu picturebox'a kendi haritanızı koyun.


> Bilgilendirme: PictureBox'a resim koymak veya değiştirmek için resime tıklayın.
> Sağ üstte çıkan, üzerinde sağa bakan ok işareti olan minik kutuya tıklayın.
> Görüntü seç'e tıklayın.
> Kaynak Bağlamı'nı seçin ve İçe Aktar'a tıklayın.
> Ardından bilgisayarınıza yüklediğiniz fotoğrafı seçin.


Bu sayede kendi istediğiniz haritayı programa yüklemiş olacaksınız.

## Savaşları ekleme/değiştirme

- Bunifupages içerisinde __"Turkiye"__ kısmına girip yuvarlak bunifu butonlarını yapacağınız savaşın olduğu bölgeye sürükleyin.
- Sürüklediğiniz butona çift tıklayın ve kod kısmına girin.
- Kod kısmında sadece ``` savaslardropdown.Items.Add("Savaşın Adı"); ``` bulunan kısım(lar)ı silin.
- Aynı kod parçasını kopyalayarak istediğiniz kadar savaş ekleyin. (Aynı kodu alt alta yapıştırıp savaş ekleyebilirsiniz.)
- Farklı bölgeler eklemek için butonu kopyala-yapıştır yapın ve başka bir yuvarlak butondan kodları alıp aynısını yeni oluşturduğunuz butona ekleyin. Ardından aynı yöntemle istediğiniz savaşları o butona ekleyin.
- Bu sayede yeni savaşlar eklemiş oldunuz.

### Savaşlara bilgi kutusu ekleme
- Sırada eklemiş olduğunuz savaşların bilgi kutusunu eklemek var.
- Bunu yapmak için haritanın alt tarafında bulunan, soru işaretli kutucuğa çift tıklayın. (522. kod satırı)
- Açılan kod satırında ilk savaşı "if" koşuluna kalan hepsini ise "else if" koşuluna bağlayıp sadece butonlara eklediğiniz savaşların isimlerini yazın. Bu savaşlar bütün butonlar için geçerli. Kısaca eklediğiniz bütün savaşları buraya yazmalısınız.
```
if (savaslardropdown.Text == "Eklediğiniz savaşın ismi")
            {
                veriTaratVeAktar("https://github.com/AslanSir/etkilesimlitarihharitasi/blob/main/Sava%C5%9Flar/malazgirt");

            }
            else if (savaslardropdown.Text == "Eklediğin bir diğer savaşın adı")
            {
                veriTaratVeAktar("https://github.com/AslanSir/etkilesimlitarihharitasi/blob/main/Sava%C5%9Flar/sakarya%20meydan%20muharebesi");

            }
```
- Koşulun içindeki __"veriTaratVeAktar"__ fonksiyonunun içindeki __linki__ kendiniz ayarlayın. Bu ayarlayacağınız sayfa örnekteki linkteki ve bu projenin sayfasındaki __"Savaşlar"__ klasöründeki savaşlardan birinin şablonunu içeriyor olmalı. Şablon şu şekilde:

```
saldiranordu:*  
savunanordu:*  
tarih:*  
savassebebi:*  
savassonucu:*  
saldirankomutan:*  
saldirankaraordusu:*  
saldirandonanma:*  
saldirankayip:*
savunankomutan:*  
savunankaraordusu:*  
savunandonanma:*
savunankayip:*

```
- Şablonun örneklerine bu sayfadaki __"Savaşlar"__ klasöründen herhangi bir savaşa tıklayarak bakabilirsiniz. Yazılar iki nokta (:) ile yıldız işareti (*) arasında olmalıdır.
- Bu sayede eklediğiniz bütün savaşlara bilgi kutusu eklemiş oldunuz.

### Savaş videosunu ekleme
- Sırada o savaşın animasyonunu oynatmakta.
- Bunu yapmak için bilgi kutusu butonunun yanında oynatma tuşlu butona basın. (547. kod satırı)
- Ardından aşağı inin ve 2 uzun çizgi arasında bulunan koşullu kodu kendinize göre ayarlayın:
```
  if (secilensavas == "Eklediğiniz Savaş")
            {
                videoac("YouTube Video Link Anahtarı");
            }
  else if (secilensavas == "Eklediğiniz savaş")
            {
                videoac("YouTube Video Link Anahtarı");
            }
  else if (secilensavas == "Eklediğiniz savaş")
            {
                videoac("0IMvXXmuwJ0");
            }
```

- YouTube video link anahtarı kısmına o savaşta açılmasını istediğiniz videonun anahtarını girin:
```
Örneğin tam linki bu olan bir videonun: https://www.youtube.com/watch?v=0IMvXXmuwJ0

anahtarı budur: 0IMvXXmuwJ0

kısaca bütün linklerde watch?v= bölümünden sonrası anahtardır. Bazı videolarda bu kısımda bazı ek işaretler bulunabilir.
Bu videonun açılma ayarlarıyla ilgilidir. O kısımları silmelisiniz.
```
- Ve bu sayede eklediğiniz savaşların videoları oynatılabilir olacak.

### Savaşları arama çubuğuna ekleme
- Son bir şey daha kaldı, o da arama çubuğunda savaşlarının çıkmasını sağlamak.
- Bunun için ilk olarak formun sağ tarafında saklanmış minik paneli sola doğru genişletmen gerekiyor. (Eğer bulamazsanız kod sayfasından 643. kod satırına gidin.)
- Ardından üst taraftaki arama kutusuna çift tıklayın. (643. kod satırı)
- Kod sayfası açıldığında en üstteki kodu düzenlemeniz gerekiyor:
```
Dictionary<BunifuButton2, List<string>> butonSavaslar = new Dictionary<BunifuButton2, List<string>>
            {
Değiştirmeniz, kopyala-yapıştır yapmanız gereken satır --->{ bunifuButton1, new List<string> { "Sakarya Meydan Muharebesi", "Deneme Savaşı","BLABLA"} },
Bunlarda örnek (Çalışması için başlarındaki çift taksimi silmeniz gerekiyor.)--->//{ butonadi, new List<string> { "İstanbul'un Fethi (1453)", "Çanakkale Savaşı" } },
                                                                                //{ butonadi, new List<string> { "Malazgirt Meydan Muharebesi" } },
                                                                                // Bu şekilde yeni butonlara yeni maddeler ekleyebilirsiniz.
            };
```
- Yapmanız gereken __"Dictionary"__ içindeki kodda her bir savaş butonu (yuvarlak buton) için işaretlenen satırı kopyala-yapıştır ile eklemeniz.
- Sadece bu kod satırında en baştaki buton adını değiştirip bir yuvarlak butonun ismini oraya yazmanız ve yazdığınız isimdeki butonun savaşlarını, yanına çift tırnak içinde virgülle ayırarak eklemeniz gerekiyor.
- Bir butonun ismini öğrenmek için o butona bir kez sol tıklamanız gerekmektedir. Ardından sağ tarafta __"özellikler (properties)"__ penceresinde, en üstte o butonun ismi gözükecektir.
- O butonun ismini __"butonadi"__ kısmına yazın ve o butona eklediğiniz savaşları da, yanına üstte yazan yöntemle ekleyin.
- Bu sayede arama çubuğunu da bitirmiş olacaksınız.

# Son
Her şey bu kadardı. Bu adımları uygulamak için temel düzeyde Visual Studio'yu ve herhangi bir dilde kodlama bilmeniz gerekiyor. Eğer adımları tek tek uygularsanız programı kendinize göre ayarlayabilir ve değiştirebilirsiniz. Bu rehberde "Ya burayı neden anlatmamış?" dediğiniz yerler anlatmakta zorlandığım yerler. Bu tarz yerleri kullandığım kelimelerle aratıp YouTube veya internet/yazılım forumlarında bulabilirsiniz.

> - Yazılım ve Rehber Yazarı: Ali ASLANMİRZA
> - Rehber Öğretmen: Emre YILDIRIM
> - Kaya Karakaya Fen Lisesi / Merkez / ELAZIĞ
> - Etkileşimli Tarih Haritası Projesi

## Hakkımda

> - Ali ASLANMİRZA
> - Sınıf: 9/D
> - Numara: 797
