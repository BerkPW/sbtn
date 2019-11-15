# Sbtn.js (Süreli Buton JS)
Hacii_ ve BerkPW'nin ortak projesi olan Sbtn.js'nin amacı basit bir yapıda javascript kodları ile html butonlara süre ifadesi eklemektir. Bu proje herkese açık ve ücretisiz şekilde paylaşılmıştır. Geliştirmek serbesttir.

***

### Kullanımı
İlk olarak `head` tagının arasına css ve js dosyalarını çağırınız.
```html
<link rel="stylesheet" href="https://raw.githubusercontent.com/BerkPW/sbtn.js/master/css/sbtn.css">
<script src="https://raw.githubusercontent.com/BerkPW/sbtn.js/master/js/sbtn.js"></script>
```

Herhangi bir buton çeşidine `id` ekleyiniz.
```html
<a id="sureli_a" href="http://google.com" class="sbtn sbtn-flat">A Href</a>
```

ve `</body>` tagından önce

```js
sbtn(id, ayar, saniye);

Örnek:
sbtn("sureli_a", {}, 8);
```
kodunu script tagları içinde ekleyin... 
Böylelikle `sureli_a` id'li butonumuza 8 sn bekleme verdik.

####Ayarlar
sbtn fonksyonunda ayarlar kısmı json ile oluşturulur.
```js
sbtn("sureli_a", {
  beklemeYazisi: "deneme-a",
  yaziRenk: "green",
  arkaplanRenk: "#eee"
  yuvarlak: "12"
}, 8);
```
Ayar kodlarının açıklamaları:

| Ayar Kodu     | Örnek Değer   | Açıklama  |
| ------------- | ------------- | --------- |
| beklemeYazisi | Bekleyiniz... | Süre dolana kadar buton üzerinde yazmasını istediğiniz yazı yazar eğer bu değişken olmaz ise butona atanan isim yazılır. |
| yaziRenk      | blue      | Butonun üzerinde yazan yazının rengini belirler eğer bu değişken olmaz ise Beyaz renk olur.  |
| arkaplanRenk  | #000          | Butonun arkadaplan rengini belirler eğer bu değişken olmaz ise Gri renk olur. |
| yuvarlak      | 30            | Butonun kenarlarının yuvarlaklığını belirler eğer bu değişken olmaz ise 0 yani keskin olur. |
