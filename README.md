# PHP-MySQL-Araç satımı kiralama veritabanı sistemi

##  Kullanılan Diller Ve Uygulamalar

- PHP 
- MySQL / MariaDB
- HTML & CSS
- FileZilla ile Hosting'e Yükleme
- GitHub Deposu


- Bu proje, bir araç kiralama firmasının basit düzeyde müşteri ve araç yönetimini yapabilmesi için yapılmıştır. Kullanıcılar sisteme kayıt olabilir, giriş yapabilir ve sisteme araç ekleyebilir, düzenleyebilir ya da silebilir. Aynı zamanda kullanıcı oturumu açıldığında sistemde kayıtlı araçları görüntüleyebilir. Proje, sade bir kullanıcı arayüzü ile temel işlemlerini yerine getirecek şekilde tasarlanmıştır.

## Proje yapısı

- oto_sistem/
- arac_ekle.php
- arac_duzenle.php
- arac_sil.php
- arac_listele.php
- kayit.php
- giris.php
- cikis.php
- panel.php
- veritabani.php
- index.php

Yapıda başlıklardan her şey belli olmakta fakat farklı olarak index.php bulunmakta. Bu kısım ile linkimiz direk giriş ekranına yönlendirmektedir.

## Giriş ekranı

![giriş](https://github.com/user-attachments/assets/1e7d580f-b0ca-441a-bf0e-9fc470b2d129)

- Resimde de görüldüğü üzere kullanıcıyı giriş ekranı karşılayacaktır. Kullanıcımız bu ekranda kayıt olduktan sonra giriş işlemini gerçekleştirmektedir. Bu kısım ise musteri adlı veritabanı tablosunda bilgileri tutulmaktadır.

## Kayıt ekranı

![kayıt](https://github.com/user-attachments/assets/88436bee-4396-40f0-9a77-e037db3e1f5a)

- Resimde görüldüğü üzere kullanıcımızdan ad,soyad,tc,telefon ve giriş ekranında istenecek olan eposta şifre bilgileri alınmaktadır.

## Panel ekranı

![panel](https://github.com/user-attachments/assets/3fa5e932-161d-4679-b590-ad304db81b41)

- Resimde görüldüğü üzere kullanıcımız giriş yaptıktan sonra karşımıza bu ekran gelmekte. Kullanıcımız burdan eklenen araçların listesini görmekte veya araç eklemesi yapabilmektedir. Tüm işlerini bitirdikten sonra çıkış yapabilmesi için çıkış yap seçeneği bulunmaktadır.

## Ekleme ekranı

![ekleme](https://github.com/user-attachments/assets/8ae03684-af03-4cfc-9c4f-f763a4b3a31f)

- Resimde görüldüğü gibi kullanıcımızdan araca dair bilgiler alınarak veritabanına kaydedilmektedir. Ekleme ekranın altında ise araç listene dön seçeneği ile listeye iletilmekte ve panele dön seçeneği ile seçim ekranına iletilmektedir.

## Araç listesi ekranı

![liste](https://github.com/user-attachments/assets/d7b3a857-7c98-4335-8cc3-d746f661d197)

- Bu kısımda şu ana kadar eklenen araçların bilgisi veritabanından çağırılarak ekranda kullanıcıya verilmektedir. Yan çubukta ise seçili olan aracı silme ve düzenleme işlemleri için seçenek bulunmaktadır. Düzenle seçeneği seçildiği zaman ekleme ekranı gelmekte ve bilgiler değiştirilebilmektedir.

## Site Linki Ve Video linki 
-https://youtu.be/cTmZWhQHE_Y?si=J-QRbCG-lNzIJmfI
-http://95.130.171.20/~st22360859023






