# Etkileşimli Tarih Haritası

### Program açık kaynak kodlu ve tamamen düzenlenebilir şekilde __"Ali ASLANMİRZA"__ tarafından kodlanmıştır.

Bu kısımda programın bütün detaylarıyla nasıl düzenlenebileceğini ve kendi haritanız üzerinde, kendi istediğiniz savaşları kendi videolarınızda nasıl gösterebileceğinizi anlatacağım.

## Başlangıç

- İlk başta kodu açmak ve düzenlemek için bilgisayarınızda __"Visual Studio"__ kurulu olmalı. Proje Visual Studio 2022'de kodlandı fakat diğer sürümlerle de birkaç küçük ayarla açabilirsiniz.
- Üstteki bölümden kodun tamamını .rar uzantılı olarak yüklemek için yeşil __"<> Code"__ butonuna tıklayın ve açılan yerden __"download zip"__ butonuna tıklayın.
- Dosya .zip uzantılı şekilde indikten sonra dosyayı açın ve .sln uzantılı dosyaya çift tıklayarak programı Visual Studio üzerinden açın.
- Projenin bütün sayfaları formun ortasındaki __"bunifuPages1"__ in içerisinde. Bu sayfalara bunifupages'in sol altındaki (ayarlı değilse sol üstündeki) beyaz yazılı butonlarla ulaşabilirsiniz.

(Bunifu crack, yani açıp kodu düzenlemeniz için bunifu lisansına gerek yok.)

## Harita Değiştirme

- Bunifupages içerisinde __"haritalar"__ kısmında inaktif haritaları silip, geriye kalan aktif haritanın picturebox'ına kendi haritanızı yükleyin. (Kodu değiştirmeyin)
- Bunifupages içerisindeki __"Turkiye"__ kısmına girip Türkiye haritasının olduğu picturebox'a kendi haritanızı koyun.

Bu sayede kendi istediğiniz haritayı programa yüklemiş olacaksınız.

## Savaşları değiştirme

- Bunifupages içerisinde __"Turkiye"__ kısmına girip yuvarlak bunifu butonları yapacağınız savaşın olduğu bölgeye sürükleyin.
- Sürüklediğiniz butona çift tıklayın ve kod kısmına girin.
- Kod kısmında sadece ``` savaslardropdown.Items.Add("Savaşın Adı"); ``` bulunan kısım(lar)ı silin.
- Aynı kod parçasını kopyalayarak istediğiniz kadar savaş ekleyin. (Aynı kodu alt alta yapıştırıp savaş ekleyebilirsiniz.)
- Farklı bölgeler eklemek için butonu kopyala-yapıştır yapın ve başka bir yuvarlak butondan kodları alıp aynısını yeni oluşturduğunuz butona ekleyin. Ardından aynı yöntemle istediğiniz savaşları o butona ekleyin.
- Bu sayede o bölgede yaşanan birden fazla savaşı tek butona eklemiş oldunuz.

- Sırada eklemiş olduğunuz savaşların bilgi kutusunu eklemek var.
- Bunu yapmak için haritanın alt tarafında bulunan, soru işaretli kutucuğa çift tıklayın. (522. kod satırı)
- Açılan kod satırında ilk savaşı "if" koşulunda kalan hepsini ise "else if" koşuluna bağlayıp sadece butonlara eklediğiniz savaşların isimlerini yazın. Bu savaşlar bütün butonlar için geçerli. Kısaca eklediğiniz bütün savaşları buraya yazmalısınız.
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

kısaca bütün linklerde watch?v= bölümünden sonrası anahtardır. Bazı videolarda bu kısımda bazı ek işaretler bulunabilir. Bu videonun açılma ayarlarıyla ilgilidir. O kısımları silmelisiniz.
```
- Ve bu sayede eklediğiniz savaşların videoları oynatılabilir olacak.

- Son bir şey daha kaldı, o da arama çubuğunda savaşlarının çıkmasını sağlamak.
- Bunun için ilk olarak formun sağ tarafında saklanmış minik paneli 
