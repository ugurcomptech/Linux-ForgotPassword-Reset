# Unutulan Linux Serverın Şifresini Sıfırlama

Merhaba, bu dökümanda şifresini unuttuğumuz linux sunucuların şifrelerini nasıl sıfırlayabileceğimizi öğreneceğiz. Aşağıdaki adımları takip ederek başarılı bir şekilde sıfırlama işLemini gerçekleştirebilirsinz.


İlk öncelikle sunucumuzu restart ediyoruz.

![image](https://github.com/ugurcomptech/Linux-ForgotPassword-Reset/assets/133202238/95a6f5b7-c71f-4713-945c-3376fc61e8d0)


Restart ettikten sonra sistemimiz seçiliyken "E" tuşuna basıyoruz.

![image](https://github.com/ugurcomptech/Linux-ForgotPassword-Reset/assets/133202238/61a4e9b8-064f-44bb-af8d-3026a1c759ca)


"E" tuşuna bastıktan sonra karşımıza açılan kısımda "linux" ile başlayan yere gelip "end" tuşuna basarak sonuna geliyoruz.

![image](https://github.com/ugurcomptech/Linux-ForgotPassword-Reset/assets/133202238/387a870f-3b58-4243-89e6-fd0b9863646f)

Son satıra gelip aşağıdaki kodu yazıyoruz:

```
fw init= /bin/bash
```

Bu komutu yazdıktan sonra "Ctrl + X" yaparak boot işlemine devam ediyoruz.

Bash ile boot ettirdik bilgisayarı şimdi gerekli işlemleri sırayla sağlayalım.

![image](https://github.com/ugurcomptech/Linux-ForgotPassword-Reset/assets/133202238/6537003e-7586-4d99-85b2-4acbc1e886bc)


## Root Şifre Değiştirme

`passwd` komutunu yazdıktan sonra başarılı bir şekilde şifrenizi sıfırlayabilirsiniz.

![image](https://github.com/ugurcomptech/Linux-ForgotPassword-Reset/assets/133202238/cccd0372-dd75-4cef-842c-ba3edcd8fc1b)

Eğer kullanıcı bazlı sıfırlamak istiyorsanız `passwd username` yazmanız gerekecektir.

## touch /.autorelabel İşlemi ve Açıklaması

SELinux (Security-Enhanced Linux) etkinleştirilmiş bir Linux sistemi üzerinde kullanıldığında, dosya sistemini tekrar etiketlemek için bir işlem başlatır. Bu işlem, dosya sistemini tekrar etiketleyerek, dosya ve dizinlerin güvenlik bağlamını düzeltmeye çalışır.

Aşağıdaki komutu yazınız:

```
touch /.autorelabel
```

## Reboot

Konsola gelip aşağıdaki komutu yazıp enter tuşuna basıyoruz:

```
/sbin/reboot -f
```


## Son

![image](https://github.com/ugurcomptech/Linux-ForgotPassword-Reset/assets/133202238/82f76262-d89d-4279-af52-69adc590bb0c)

Başarılı bir şekilde şifre sıfırlama işlemini gerçekleştirdik.
