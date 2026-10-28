# Anki Çoktan Seçmeli Test Şablonu Kurulum Kılavuzu

Bu kılavuz Anki üzerinde otomatik karıştırılan çoktan seçmeli test kart tipi oluşturma, deste yönetimi, toplu kart aktarma ve yapay zeka ile soru hazırlama adımlarını içerir.

---

## İçindekiler
- [Anki Çoktan Seçmeli Test Şablonu Kurulum Kılavuzu](#anki-çoktan-seçmeli-test-şablonu-kurulum-kılavuzu)
  - [İçindekiler](#i̇çindekiler)
  - [1. Masaüstü Uygulaması (Anki Desktop)](#1-masaüstü-uygulaması-anki-desktop)
    - [1.1. Not Tipinin Oluşturulması](#11-not-tipinin-oluşturulması)
    - [1.2. Şablon ve Tasarım Kodlarının Eklenmesi](#12-şablon-ve-tasarım-kodlarının-eklenmesi)
  - [2. Mobil Uygulama (AnkiDroid)](#2-mobil-uygulama-ankidroid)
    - [2.1. Not Tipinin Oluşturulması](#21-not-tipinin-oluşturulması)
    - [2.2. Şablon ve Tasarım Kodlarının Eklenmesi](#22-şablon-ve-tasarım-kodlarının-eklenmesi)
  - [3. Yeni Deste Oluşturma ve Manuel Not Ekleme](#3-yeni-deste-oluşturma-ve-manuel-not-ekleme)
    - [3.1. Masaüstü Uygulamasında](#31-masaüstü-uygulamasında)
    - [3.2. Mobil Uygulamada (AnkiDroid)](#32-mobil-uygulamada-ankidroid)
  - [4. Toplu Not Oluşturma ve İçe Aktarma (TXT / CSV)](#4-toplu-not-oluşturma-ve-i̇çe-aktarma-txt--csv)
    - [4.1. Dosya Formatı ve Yapısı](#41-dosya-formatı-ve-yapısı)
    - [4.2. Dosyayı Anki'ye İçe Aktarma (Masaüstü)](#42-dosyayı-ankiye-i̇çe-aktarma-masaüstü)
    - [4.3. Dosyayı AnkiDroid'e İçe Aktarma (Mobil)](#43-dosyayı-ankidroide-i̇çe-aktarma-mobil)
  - [5. Yapay Zeka ile Kaynaklardan Soru Üretme](#5-yapay-zeka-ile-kaynaklardan-soru-üretme)
    - [5.1. Soru Üretiminde Karşılaşılan Hatalar](#51-soru-üretiminde-karşılaşılan-hatalar)
    - [5.2. Hazır Prompt Şablonu](#52-hazır-prompt-şablonu)
    - [5.3. Çıktıyı Dosyaya Dönüştürme ve İçe Aktarma](#53-çıktıyı-dosyaya-dönüştürme-ve-i̇çe-aktarma)

---

## 1. Masaüstü Uygulaması (Anki Desktop)

### 1.1. Not Tipinin Oluşturulması
1. https://apps.ankiweb.net/ adresinden Anki uygulamasını indirin ve bilgisayarınıza kurun.
2. Uygulamayı çalıştırın.
3. Klavyeden `Ctrl + Shift + N` tuşlarına basın (veya üst menüden **Tools > Manage note types** yolunu izleyin).
4. **Add** butonuna tıklayın, listeden **Add: Basic** seçeneğini işaretleyip **OK** butonuna tıklayın.
5. **Name** alanına `Test Formatı` yazın ve onaylayın.
6. Listeye eklenen `Test Formatı` isimli not tipini seçin.
7. Sağ tarafta yer alan **Fields** (Alanlar) butonuna tıklayın.
8. `1: Front` alanını seçip sağdaki **Rename** butonuna tıklayın ve alan adını `Soru` olarak değiştirin.
9. `2: Back` alanını seçip sağdaki **Rename** butonuna tıklayın ve alan adını `DogruCevap` olarak değiştirin.
10. Sağdaki **Add** butonuna tıklayarak sırasıyla şu üç yeni alanı ekleyin:
    - `Celdirici1`
    - `Celdirici2`
    - `Celdirici3`
11. Pencerenin altındaki **Save** butonuna tıklayarak alanları kaydedin.

### 1.2. Şablon ve Tasarım Kodlarının Eklenmesi
1. Not Tipleri penceresinde `Test Formatı` seçiliyken sağdaki **Cards** (Kartlar) butonuna tıklayın.
2. Açılan pencerede üst kısımdan **Front Template** sekmesini seçin; mevcut kodları silerek [Front Template.html](https://github.com/acrilot/anki-test-template/blob/main/Front%20Template.html) dosyasının içeriğini yapıştırın.
3. Üst kısımdan **Back Template** sekmesini seçin; mevcut kodları silerek [Back Template.html](https://github.com/acrilot/anki-test-template/blob/main/Back%20Template.html) dosyasının içeriğini yapıştırın.
4. Üst kısımdan **Styling** sekmesini seçin; mevcut kodları silerek [Styling.css](https://github.com/acrilot/anki-test-template/blob/main/Styling.css) dosyasının içeriğini yapıştırın.
5. **Save** butonuna tıklayarak değişiklikleri kaydedin ve pencereleri kapatın.

---

## 2. Mobil Uygulama (AnkiDroid)

### 2.1. Not Tipinin Oluşturulması
1. Google Play Store üzerinden AnkiDroid uygulamasını indirin ve açın.
2. Sağ üst köşede bulunan üç nokta menüsüne dokunun ve **Manage note types** seçeneğine girin.
3. Sağ alt köşedeki **+** simgesine dokunun.
4. Tip olarak **Add: Basic** seçeneğini belirleyin ve isim alanına `Test Formatı` yazın.
5. Listeye eklenen `Test Formatı` not tipinin üzerine dokunun.
6. `Front` alanının sağındaki üç nokta menüsünden **Rename field** seçeneğine dokunarak alan adını `Soru` olarak değiştirin.
7. `Back` alanının sağındaki üç nokta menüsünden **Rename field** seçeneğine dokunarak alan adını `DogruCevap` olarak değiştirin.
8. Sağ alttaki **+** simgesine dokunarak sırasıyla şu üç alanı ekleyin:
   - `Celdirici1`
   - `Celdirici2`
   - `Celdirici3`
9. Geri tuşuna basarak **Manage note types** listesine dönün.

### 2.2. Şablon ve Tasarım Kodlarının Eklenmesi
1. `Test Formatı` not tipinin sağındaki düzenleme (kalem) simgesine dokunun.
2. Varsayılan olarak **Front** sekmesi açılacaktır; ekrandaki mevcut kodları silip [Front Template.html](https://github.com/acrilot/anki-test-template/blob/main/Front%20Template.html) dosyasının içeriğini yapıştırın.
3. Ekranın altından **Back** sekmesini seçin; ekrandaki kodları silip [Back Template.html](https://github.com/acrilot/anki-test-template/blob/main/Back%20Template.html) dosyasının içeriğini yapıştırın.
4. Ekranın altından **Styling** sekmesini seçin; ekrandaki kodları silip [Styling.css](https://github.com/acrilot/anki-test-template/blob/main/Styling.css) dosyasının içeriğini yapıştırın.
5. Ekranın üst tarafındaki onay (✓) simgesine dokunarak değişiklikleri kaydedin ve çıkın.

---

## 3. Yeni Deste Oluşturma ve Manuel Not Ekleme

### 3.1. Masaüstü Uygulamasında
1. **Deste Oluşturma:**
   - Ana ekranın alt kısmında yer alan **Create Deck** butonuna tıklayın.
   - Destenize bir isim verin ve **OK** butonuna tıklayın.
2. **Not (Kart) Ekleme:**
   - Ana ekranın üst kısmındaki **Add** butonuna tıklayın (veya klavyeden `A` tuşuna basın).
   - **Type** açılır menüsünden `Test Formatı`nı seçin.
   - **Deck** açılır menüsünden kartları eklemek istediğiniz desteyi seçin.
   - Alanları doldurun:
     - **Soru:** Soru metni
     - **DogruCevap:** Doğru cevap şıkkı
     - **Celdirici1:** 1. Yanlış şık
     - **Celdirici2:** 2. Yanlış şık
     - **Celdirici3:** 3. Yanlış şık
   - Pencerenin altındaki **Add** butonuna tıklayarak kartı kaydedin.

### 3.2. Mobil Uygulamada (AnkiDroid)
1. **Deste Oluşturma:**
   - Ana ekranda sağ alt köşede yer alan **+** simgesine dokunun.
   - Açılan seçeneklerden **Create deck** seçeneğine dokunun, isim girip onaylayın.
2. **Not (Kart) Ekleme:**
   - Kart eklemek istediğiniz desteye dokunarak içine girin.
   - Sağ alt köşedeki **+** simgesine dokunup **Add note** seçeneğini seçin.
   - Üst tarafta **Type** alanının `Test Formatı`, **Deck** alanının ise ilgili deste olduğundan emin olun.
   - `Soru`, `DogruCevap`, `Celdirici1`, `Celdirici2`, `Celdirici3` alanlarını doldurun.
   - Sağ üst köşedeki onay (✓) simgesine dokunarak kartı kaydedin.

---

## 4. Toplu Not Oluşturma ve İçe Aktarma (TXT / CSV)

Çok sayıda soruyu tek tek girmek yerine bir metin editörü (Not Defteri, VS Code vb.) veya tablo programı (Excel, Google E-Tablolar) kullanarak toplu olarak hazırlayıp içe aktarabilirsiniz.

### 4.1. Dosya Formatı ve Yapısı
Hazırlayacağınız `.txt` veya `.csv` dosyasında her satır bir kartı temsil eder ve sütunlar noktalı virgül (`;`) ile ayrılmalıdır.

Format yapısı:
```text
Soru;DogruCevap;Celdirici1;Celdirici2;Celdirici3
```

Örnek dosya içeriği:
```text
Türkiye'nin başkenti neresidir?;Ankara;İstanbul;İzmir;Bursa
Hangi gezegen Güneş'e en yakındır?;Merkür;Venüs;Mars;Jüpiter
Suyun kimyasal formülü nedir?;H2O;CO2;NaCl;O2
Mona Lisa tablosu kime aittir?;Leonardo da Vinci;Michelangelo;Raphael;Donatello
```

> Not: Dosyayı kaydederken karakter kodlamasının (encoding) mutlaka **UTF-8** olduğundan emin olun. Bu sayede Türkçe karakterler (ç, ğ, ı, ö, ş, ü) sorunsuz görüntülenir.

### 4.2. Dosyayı Anki'ye İçe Aktarma (Masaüstü)
1. Anki ana ekranında sol üst menüden **File > Import** seçeneğine tıklayın (veya `Ctrl + I` kısayolunu kullanın).
2. Hazırladığınız `.txt` veya `.csv` dosyasını seçip açın.
3. Açılan içe aktarma penceresinde aşağıdaki ayarları kontrol edin:
   - **Field separator:** `Semicolon` (Noktalı virgül `;`) olarak belirlenmiş olmalıdır.
   - **Note Type:** `Test Formatı` olarak seçili olmalıdır.
   - **Deck:** Soruların aktarılacağı desteyi seçin.
   - **Field mapping:** Sütunların şablon alanlarıyla sırasıyla eşleştiğini kontrol edin:
     - 1. Alan -> `Soru`
     - 2. Alan -> `DogruCevap`
     - 3. Alan -> `Celdirici1`
     - 4. Alan -> `Celdirici2`
     - 5. Alan -> `Celdirici3`
   - Geri kalan kısımlar aynı kalabilir.
4. Ayarları doğruladıktan sonra sağ alt kısımdaki **Import** butonuna tıklayın.
5. İçe aktarma tamamlandığında eklenen not sayısı ekranda bildirilir ve tüm sorular destenizde kullanıma hazır hale gelir.

### 4.3. Dosyayı AnkiDroid'e İçe Aktarma (Mobil)
1. Hazırladığınız `.txt` veya `.csv` dosyasını telefonunuza aktarın.
2. AnkiDroid uygulamasını açın.
3. Sağ üst köşedeki üç nokta menüsüne dokunun ve **Import** seçeneğini seçin.
4. **Text file (.txt, .csv)**'a tıklayın.
5. Telefon hafızasından hazırladığınız `.txt` veya `.csv` dosyasını seçin.
6. İçe aktarma ekranında:
   - **Field separator:** Noktalı virgül (`;`) olarak belirleyin.
   - **Note type:** `Test Formatı` olarak seçin.
   - **Deck:** Soruların aktarılacağı desteyi seçin.
   - **Field mapping:** Alanların sırasıyla `Soru`, `DogruCevap`, `Celdirici1`, `Celdirici2`, `Celdirici3` ile eşleştiğini doğrulayın.
   - Geri kalan kısımlar aynı kalabilir.
7. Sağ üst köşedeki onay (✓) simgesine dokunarak içe aktarma işlemini tamamlayın.

*(Alternatif olarak; telefonun dosya yöneticisinden `.txt` veya `.csv` dosyasına dokunup "Birlikte Aç > AnkiDroid" seçeneğini kullanabilir ya da kartları Masaüstü sürümünde içe aktardıktan sonra senkronizasyon [Sync] butonu ile tek tıkla telefonunuza eşitleyebilirsiniz.)*

---

## 5. Yapay Zeka ile Kaynaklardan Soru Üretme

Ders notları, makaleler, PDF'ler veya kitap özetleri gibi kaynak metinlerden ChatGPT, Claude, Gemini veya yerel yapay zeka modelleri aracılığıyla doğrudan Anki'ye aktarılabilir `.txt` veya `.csv` çıktısı alınabilir.

### 5.1. Soru Üretiminde Karşılaşılan Hatalar
Yapay zeka modellerine soru ürettirirken sıkça iki temel sorun yaşanır:
1. **Soru Kökünde İpucu Verme:** Modelin soru cümlesinde gereksiz detay, tanım veya bağlam vererek doğru cevabı açık etmesi. Bu durum, sorunun bilgiyi ölçmek yerine basit bir mantık çıkarımıyla çözülmesine yol açar. Soru kökü net, odaklı ve kısa olmalıdır.
2. **Cevap Uzunluğu ve Detay Dengesizliği:** Doğru cevabın diğer şıklara kıyasla belirgin şekilde daha uzun, detaylı veya açıklayıcı yazılması. Bu durum, soruyu okumayan birinin bile en uzun şıkkın doğru olduğunu tahmin etmesine neden olur. Dört şık da (doğru cevap ve 3 çeldirici) benzer uzunlukta, homojen ve aynı inandırıcılık düzeyinde olmalıdır.

### 5.2. Hazır Prompt Şablonu
Aşağıdaki prompt şablonunu doğrudan kopyalayarak veya ihtiyacınıza uygun bir şekilde düzenlemeler yaparak eklediğiniz kaynaklarla birlikte yapay zekaya iletebilirsiniz:

```text
Eklediğim kaynakları dikkatle incele ve önemli bilgileri ölçen çoktan seçmeli test soruları üret.

Çıktıyı oluştururken şu kurallara KESİNLİKLE uy:

1. FORMAT KURALLARI:
   - Her soru tek bir satırda yer almalıdır.
   - Alanlar yalnızca noktalı virgül (;) ile ayrılmalıdır:
     Soru;DogruCevap;Celdirici1;Celdirici2;Celdirici3
   - Satır başlarına veya sonlarına numara (1., 2.), harf (A, B) ya da işaret koyma.
   - Soru kökünde veya şıkların metni içinde asla noktalı virgül (;) karakteri kullanma.
   - Çıktıyı yalnızca temiz bir kod bloğu (code block) içinde ver. Başında veya sonunda selamlama, açıklama ya da ek not yazma.

2. SORU KÖKÜ KURALLARI:
   - Soru kökünde cevabı açık eden, ima eden veya gereksiz bağlam/tanım içeren ipuçları verme.
   - Soruyu doğrudan, net ve gereksiz laf kalabalığı yapmadan sor.

3. ŞIK VE ÇELDİRİCİ KURALLARI:
   - Doğru cevap KESİNLİKLE çeldiricilerden daha uzun, daha detaylı veya daha açıklayıcı OLMAMALIDIR.
   - Dört şık da (DogruCevap, Celdirici1, Celdirici2, Celdirici3) yaklaşık olarak aynı kelime ve karakter uzunluğunda olmalıdır.
   - Dört şık da aynı dilbilgisi yapısında (örneğin hepsi sadece kavram, hepsi aynı fiil ekiyle biten ifade veya hepsi tam cümle) hazırlanmalıdır.
   - Çeldiriciler uydurma veya bariz biçimde saçma olmamalı; metinle ilişkili, inandırıcı ve güçlü alternatifler olmalıdır.
   - Parantez içinde açıklamalar veya ifadeler bulunmamalıdır.
```

Bunlara ek olarak istenirse soru sayısı belirtilebilir veya örnek sorular verilerek benzer formatta sorular üretmesi istenebilir.

### 5.3. Çıktıyı Dosyaya Dönüştürme ve İçe Aktarma
1. Yapay zekanın ürettiği kod bloğu içerisindeki metni kopyalayın.
2. Bilgisayarınızda veya telefonunuzda bir metin düzenleyici (Not Defteri vb.) açarak yapıştırın.
3. Dosyayı kaydederken uzantısını `.txt` veya `.csv` yapın ve karakter kodlamasını (encoding) mutlaka **UTF-8** olarak belirleyin.
4. Bu rehberin **Bölüm 4.2** veya **Bölüm 4.3** adımlarını uygulayarak hazırladığınız dosyayı destenize aktarın.
