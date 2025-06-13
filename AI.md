### Kullanıcı:

Merhaba dostum, proje ödevime başlamak istiyorum ama hiçbir fikrim yok. Sana adım adım danışacağım.

### ChatGPT:

Elbette, birlikte ilerleriz. Önce proje metnini atabilir misin?

### Kullanıcı:

\[Proje metnini attı: Web Tabanlı Programlama - PHP, MySQL, HTML, CSS kullanılacak, kullanıcı kaydı, giriş, CRUD işlemleri olacak. Hosting'e yüklenmesi isteniyor.]

### Kullanıcı:

"Oto Kiralama ve Satış Sistemi" adlı konuyu seçtim. Daha önceden bir veritabanım vardı, onu atayım.

### ChatGPT:

Uygun, birlikte mevcut veritabanına göre PHP sayfalarını yönlendirebiliriz. Veritabanında hangi tablolar kullanılacaksa sadece onları aktif tutman yeterli.

### Kullanıcı:

Ben bu veritabanının tamamını kullanmayacağım. Bazı tabloları silsem mi?

### ChatGPT:

Eğer kullanmıyorsan silmen daha sade ve profesyonel bir sunum sağlar. Ama önce yedek almanı öneririm.

### Kullanıcı:

Hosting kısmını hiç bilmiyorum. Hosting nedir nasıl kullanmam lazım.

### ChatGPT:

FTP, dosyaları uzak bir sunucuya taşımak için kullanılan bir yöntemdir. Senin aldığın bilgilerde IP, kullaıncı adı, şifre ve port bilgisiyle FileZilla gibi bir programla hostingine bağlanıp dosyaları yükleyebilirsin.

### Kullanıcı:

FTP Nedir?,

### ChatGPT:


### Kullanıcı:

FileZilla kurarken virüslü uyarısı verdi. 
### ChatGPT:

Kurarken "sponsored" olmayan çıplak versiyonu indir. Veya WinSCP gibi alternatif bir FTP istemcisi de kullanabilirsin.

### Kullanıcı:

Dosyaları attım ama tarayıcıda "Forbidden" hatası alıyorum.

### ChatGPT:

Bu hata genellikle "permission" yani dosya izinlerinden kaynaklanır. FileZilla'da `public_html` klasörü ve içindeki dosyalar için izinleri 755 klasör, 644 dosya yap. Ayrıca dizinin içinde `index.php` veya `index.html` olması gerekir.

### Kullanıcı:

Yaptım ama bu sefer de "Not Found" hatası verdi.

### ChatGPT:

URL'yi doğru yazdığından emin ol. Örneğin:

```
http://95.130.171.20/~st22360859023/oto_sistem/giris.php
```

Ayrıca dosya adlarının büyük/küçük harf duyarlı olduğuna dikkat et.

### Kullanıcı:

Veritabanıyla bağlantıda `mysqli_sql_exception` hatası alıyorum.

### ChatGPT:

Bu hata genellikle veritabanı adının, kullanıcı adının ya da şifresinin yanlış olmasından kaynaklanır. `veritabani.php` içeriğinde bunları doğru yazdığından emin ol:

```php
$baglanti = new mysqli("localhost", "dbusr22360859023", "6gVhVTQBLsv5", "dbstorage22360859023");
```

### Kullanıcı:

Bazı dosyalarda "table doesn't exist" hatası veriyor.

### ChatGPT:

Bu tablo adları veritabanında tam aynı olmalı. `Arac` yazıyorsa veritabanında da `Arac` şeklinde büyük harfli olmalı. `arac` ise `arac` yazmalı.



1. Hosting Nedir?

Soru: FTP ne oluyor, hiç bilmeyen birine göre anlatır mısın?

Yanıt: FTP (File Transfer Protocol), bilgisayarımızdaki dosyaları uzaktaki bir sunucuya (örneğin hosting hizmeti) yüklememize veya oradan indirmemize yarayan bir protokoldür. Web projelerini canlıya almak için kullanılır. Dosya aktarımı için genelde FileZilla gibi programlar kullanılır.

2. Hosting Kurulumu Sırasında Alınan Hatalar

FileZilla indirme sırasında virüs uyarısı verdiği için .zip sürümünün indirilmesi önerildi.

index.php dosyası olmasına rağmen sunucudan "403 Forbidden" hatası alındı. Bu, dosya izinlerinden kaynaklı olabilir (CHMOD ayarları 755 yapılmalıydı).

Daha sonra "404 Not Found" hatası alındı, çünkü klasör yolu yanlış girilmişti ya da yönlendirme dosyası eksikti.

Soru: Şu an bu ekrandayım ama biz veritabani.php dosyasını güncellemedik, şimdi ne yapacağım?

Yanıt: Hosting ortamındaki veritabanı bağlantı bilgilerinin (sunucu adı, kullanıcı adı, şifre, veritabanı adı) yerel veritabanından farklı olduğu için veritabani.php dosyası güncellenmelidir.

3. Veritabanı İlişkili Hatalar

FOREIGN KEY hataları nedeniyle önce bağlı olduğu tabloya (örneğin sube) veri girildi.

Duplicate entry gibi hatalar, aynı plakalı araç iki kez girilmeye çalışıldığında alındı.

ENUM değerleri (örneğin durum, tur) için veritabanındaki seçenekler dışındaki bir değer gönderildiğinde Data truncated hatası alındı.

Soru: Bizim bu veritabanındaki şubeye neden bir değer eklediğimizi ben hala anlamadım.

Yanıt: Çünkü musteri tablosundaki sube_id, sube tablosuna bağlı foreign key olduğundan dolayı, önce sube tablosunda en az bir kayıt olması gerekiyor.

4. Tasarım ve UI Soruları

Soru: Tasarımdan vazgeçtim.

Yanıt: Tasarımda Bootstrap gibi kütüphaneler zorunlu değilse, sade HTML/CSS kullanımı anlaşılır ve öğrenci düzeyine uygun olabilir. Tasarımın puana etkisi varsa temel seviyede CSS önerildi.

5. Panel ve Giriş Sistemi Sorunları

Soru: Giriş yaptıktan sonra sadece "Giriş başarılı, hoş geldin!" yazısı geliyor, başka bir şey yok.

Yanıt: Giriş sonrası yönlendirme yapılan panel.php dosyasına, kullanıcıyı yönlendirecek bağlantılar (araç listeleme, araç ekleme vs.) manuel olarak eklendi.


Hosting erişimi sağlandıktan sonra veritabanı bilgileri veritabani.php dosyasına güncellendi.

oto_sistem klasörü FileZilla ile /public_html/ dizinine yüklendi.

Hostingdeki dizin izni (permission) 755 olarak düzeltildi.

Test için index.php sayfası eklendi, giriş sayfasına yönlendirildi.

Sunucuda veritabanı eksik olduğunda alınan hatalar kontrol edildi ve yeniden yüklendi.

Musteri, Arac, Personel gibi tabloların bazılarının kullanılmadığı fark edildi ama silinmesine gerek olmadığına karar verildi.

