# Bootstrap

## Bootstrap Nedir?

Bootstrap, web sayfaları ve web tabanlı uygulamaların ön yüzlerini(front-end) geliştirmek için kullanabileceğimiz bir uygulama geliştirme çatısıdır.(framework)
Bootstrap mobile first yaklaşımını temel alır.
Bootstrap temelinde HTML5,CSS3 ve Js bulundurmaktadır.

### Neden Bootstrap?

Bootstrap, bünyesinde birçok bileşen barındırır. Bu bileşenleri kolaylıkla öğrenebilir, web sayfanızda kullanabilir ve web sayfanızı daha kısa süre içerisinde kolaylıkla oluşturabilirsiniz.

Bootstrap’teki grid sistemi ile birlikte ekran boyutuna duyarlı web sayfaları oluşturabilirsiniz.

Bootstrap tüm tarayıcıların en yeni sürümlerini destekler.

Bootstrap ile oluşturulmuş siteler(örnek): https://getbootstrap.com/docs/4.0/examples/

Bootstrap Dökümanları: https://getbootstrap.com/docs/5.2/getting-started/introduction/

Kaynak Önerisi: https://www.w3schools.com/bootstrap/bootstrap_get_started.asp


```
<link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">

<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
```

## Bootstrap'te Containers
Containers içlerindeki içeriği doldurmak için kullanılırlar. İki tip Container vardır:

1- `.container` sınıfı, duyarlı sabit genişlikte bir kapsayıcı sağlar.

2- `.container-fluid` sınıfı, görünümün tüm genişliğini kapsayan tam genişlikte bir kapsayıcı sağlar.

![Görsel Hali](https://i.hizliresim.com/r5iduxx.png)

## Sabit Containers(Kapsayıcılar)
`.container` sınıfını kullanarak sabit genişlikte, duyarlı kapsayıdılar oluşturulabilir.
`max-width` ile farklı ekran boyutlarında değişen kapsayıcılar oluşturulabilir.

## Fluid Container
Her zaman ekranın tüm genişliğini kaplayacak tam genişlikte bir kap oluşturmak için `.container-fluid` sınıfı kullanılır.

## Kapsayıcı Dolgusu

Varsayılan olarak kapsayıcılar, üst veya alt dolgu olmadan sol ve sağ dolguya sahiptir. Bu nedenle, daha iyi görünmelerini sağlamak için genellikle fazladan dolgu ve kenar boşlukları gibi  yardımcı programları kullanırız. 

Örneğin, `.pt-5`, "büyük bir üst dolgu ekle" anlamına gelir.

`<div class="container pt-5"></div>`

## Kapsayıcıların Sınırları ve Renkleri

```
<div class="container p-5 my-5 border"></div>

<div class="container p-5 my-5 bg-dark text-white"></div>

<div class="container p-5 my-5 bg-primary text-white"></div>
```

## Bootstrap 5 Izgara(Grid) Sistemi

Bootstrap'in ızgara sistemi flexbox ile oluşturulmuştur. 

Sayfa boyunca 12 sütuna kadar izin verir.

12 sütunun tümünü tek tek kullanmak istemiyorsanız, daha geniş sütunlar oluşturmak için sütunları birlikte gruplayabilirsiniz.

![Grid System](https://i.hizliresim.com/isnd6zs.png)

Grid sistemi duyarlıdır ve sütunlar ekran boyutuna bağlı olarak otomatik olarak yeniden düzenlenir.

## Grid Sınıfları
Bootstrap 5'te altı adet sınıf bulunmaktadır.

| Sınıf         | Açıklaması    | 
| ------------- |:-------------:|
| `.col-`       |extra küçük cihazlar - ekran genişliği 576px'den az                            |
| `.col-sm-`    |küçük cihazlar - ekran genişliği 576px ile 768px arasındaki cihazlar           |
| `.col-md-`    |orta cihazlar - ekran genişliği 768px ile 992px arasındaki cihazlar            |
| `.col-lg-`    |büyük cihazlar - ekran genişliği 992px ile 1200px arasındaki cihazlar          |
| `.col-xl-`    |daha büyük cihazlar - ekran genişliği 1200px ile 1400px arasındaki cihazlar    |
| `.col-xxl-`   |extra büyük cihazlar - ekran genişliği 1400px'den fazla olan cihazlar          |

#### 3 Eşit Kolon Oluşturma
```
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
  
<div class="container-fluid mt-3">
  <h1>3 Eşit Kolon Oluşturma</h1>

  <div class="row">
    <div class="col p-3 bg-primary text-white">.col</div>
    <div class="col p-3 bg-dark text-white">.col</div>
    <div class="col p-3 bg-primary text-white">.col</div>
  </div>
</div>

</body>
</html>
```
![Çıktı](https://i.hizliresim.com/d529tht.png)

#### Eşit Olmayan İki Kolon Oluşturma
```
<!DOCTYPE html>
<html lang="en">
<head>
  <title>Bootstrap Example</title>
  <meta charset="utf-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/css/bootstrap.min.css" rel="stylesheet">
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.1.3/dist/js/bootstrap.bundle.min.js"></script>
</head>
<body>
  
<div class="container-fluid mt-3">
  <h1>Eşit Olmayan İki Kolon Oluşturma</h1>
  <p>Resize the browser window to see the effect.</p>

  <div class="row">
    <div class="col-sm-4 p-3 bg-primary text-white">.col</div>
    <div class="col-sm-8 p-3 bg-dark text-white">.col</div>
  </div>
</div>

</body>
</html>
```
![Çıktı](https://i.hizliresim.com/loyd8gn.png)

# Tipografi Sınıfları

## Bootstrap 5 Varsayılan Özellikler(Default Settings)
Bootstrap 5 varsayılan bir `font-size` kullanır. Bu 16px'dir. `line-height` ise 1.5'tir.
Ek olarak, tüm `<p>` elementleri `margin-top:0` ve `margin-bottom: 1rem` varsayılan özelliklerine sahiptir.

### `<code>` Elementi
HTML sayfasında bir kodu belirtmek için kullanılır. 
Örnek kullanım: `<p> HTML elementlerinden <code>span</code> dökümanda bir bölüm tanımlarken kullanılır.`

### `<kbd>` Elementi
Tuş takımı kombinasyonlarını göstermek için `<kbd>` elementi kullanılır.
Örnek kullanım: `<p> Bir diyaloğu bastırmak için <kbd>ctrl+p</kbd>elementi kullanılır.</p>`

### Daha fazla tipografi sınıfı
| Sınıf         | Açıklaması    | 
| ------------- |:-------------:|
| `.lead`       |Bir paragrafın öne çıkmasını sağlar                          |
| `.text-start`    |Sola hizalanmış metni gösterir          |
| `.text-break`    |Uzun metnin düzeni bozmasını önler          |
| `.text-center`    |Ortaya hizalanmış metni gösterir       |
| `.text-decoration-none`    |Bağlantıdan alt çizgiyi kaldırır   |
| `.text-end`   |Sağa hizalanmış metni gösterir          |
| `.text-nowrap`       |Sarma metni olmadığını gösterir                         |
| `.text-lowercase`    |Küçük harfli metni gösterir           |
| `..text-uppercase`    |Büyük harfli metni gösterir            |
| `.text-capitalize`    |Büyük harfle yazılmış metni gösterir         |
| `.initialism`    |<abbr> öğesinin içindeki metni biraz daha küçük yazı tipi boyutunda görüntüler  |
| `.list-unstyled`   |Liste öğelerindeki varsayılan liste stilini ve sol kenar boşluğunu kaldırır (hem <ul> hem de <ol> üzerinde çalışır). Bu sınıf yalnızca acil alt liste öğeleri için geçerlidir (varsayılan liste stilini herhangi bir yuvalanmış listeden kaldırmak için, bu sınıfı herhangi bir yuvalanmış listeye de uygulayın)         |
| `.list-inline`   |Tüm liste öğelerini tek bir satıra yerleştirir (her <li> öğesinde .list-inline-item ile birlikte kullanılır)       |
