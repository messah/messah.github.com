---
layout: post
title: 19 Sayfa Şablonu
---

**DİKKAT!  Bu sayfayı güncelleyeceğiz.  Lütfen şu aşamada dokümana dayalı
olarak hiçbir işlem yapmayın.**

Bu depoda 19 organizasyonu üyelerinin kişisel sitelerinde yararlanabileceği
GitHub Jekyll şablonu bulunmaktadır.  Şablonla ilgili sorunları veya istekleri
lütfen [proje hataları sayfasına](http://github.com/00010011/site/issues) girdi
ekleyerek bildirin.

## Kurulum

Kurulumdan önce aşağıdaki koşulları sağladığınıza emin olmalısınız.  (Bu
doküman boyunca kullanılan konvansiyona lütfen dikkat edin.  Uçbirimde
yazmanız gereken komutlar `$` karakteri ile başlamaktadır.  **Bu komutları
uçbirime kopyalıyorsanız baştaki `$` karakterini silmeniz gerekiyor!**)

1. GitHub'a kaydolduğunuzu, GitHub hesap adınızı (`<hesapadı>`) ve GitHub
   servislerine bu hesap üzerinden erişirken gerekli olan "GitHub API Token"
   değerini (`<token>`) bildiğinizi varsayıyoruz.  "GitHub API Token" GitHub
   [hesap ayarlarınızda](https://github.com/account) "Account Admin"
   sekmesinde "API Token" adıyla bulacağınız bir onaltılı karakter dizisidir.

2. Kuruluma başlamadan önce `<hesapadı>` ve `<token>` değerlerinin kişisel Git
   yapılandırma dosyasına kaydedildiğine emin olun.  Bu aşamayla ilgili daha
   ayrıntılı bilgi almak için lütfen [ilgili GitHub
   sayfasını](http://help.github.com/git-email-settings/) okuyun.

3. Mevcut hesabınızda `<hesapadı>.github.com` isimli bir depo zaten varsa bu
   deponun ismini değiştirmeli veya (yedekledikten sonra) silmelisiniz.  Aksi
   halde kurulum komutu işlem yapmayı reddedecektir.

Bu koşulları sağlıyorsanız kurulum için aşağıdaki komutunu kullanın.

            $ wget ondokuz.biz/kur -qO- | sh

Kurulum sürecinde karşılaştığınız sorunları lütfen 19 haberleşme listesine
raporlayın.  Kurulum sırasında her şey yolunda gitmişse kişisel sitenize
aşağıdaki adresten erişebiliyor olmanız lazım.

            http://<hesapadı>.github.com

Dikkat!  GitHub'ın siteyi güncellemesi biraz zaman almaktadır.  Değişiklikleri
GitHub'a gönderdikten sonra kısa bir süre beklemeyi unutmayın.

Bu noktadan sonra deponuzu düzenlemeye, yeni sayfa eklemeye başlayabilirsiniz.
Lütfen bu işlemler için dokümanın tamamını okumayı unutmayın.

## Kullanım

Sitede "`0-1-2-7-9`" sayfalama sisteminin Jekyll'a uyarlanmış bir modeli
kullanılmaktadır.  Bu model kısaca ilgili bölümde anlatılmıştır.  Sitede girdi
ekleme, girdi düzenleme işlemlerini bu açıklamalara uygun şekilde elle yapmak
yerine bu süreci hızlandırmak amacıyla hazırlanmış 19 komutlarını veya bu
komutların kurulum sırasında tanımlanmış olan kısayollarını (Git "alias")
kullanabilirsiniz.

Site girdilerini doğrudan HTML olarak yazmak yerine, dosya uzantısını `.md`
yapmak kaydıyla, HTML üreten hafif bir etiketleme dili olan
[Markdown](http://daringfireball.net/projects/markdown/syntax) sözdizimini
kullanabilirsiniz.

**İpucu**  Gedit metin düzenleyicide markdown eklentisini kurar ve
etkinleştirirseniz düzenleme sırasında üretilen HTML çıktıyı izleyebilirsiniz.
Gedit'in kullanımı hakkında daha ayrıntılı bilgi edinmek için Emre Can
Yılmaz'ın yazdığı [Gedit Kullanım
Kılavuzunu](http://ecylmz.com/107/gedit-kullanimi/) inceleyin.

### Sayfa Ekleme

1. Ekleyeceğiniz sayfanın kategorisini belirleyin.

    - Kişisel düşünce ve duygularınızı yansıtan "Web Günlüğü" niteliğinde
      yazılar **`0`** kategorisinde

    - Öğretici değer taşıyan teknik yazılar **`1`** kategorisinde

   **Dikkat!**  Web günlüğündeki yazılar teknik nitelikte olabilir, örneğin
   Ubuntu'nun yeni sürümü hakkında yapılan bir inceleme veya yeni aldığınız
   bir dizüstü bilgisayarın incelemesi gibi.  **`0`** kategorisinin ayırt
   edici özelliği yazıda ifade edilen düşüncelerin büyük ölçüde öznel, size
   ait olmasıdır.

2. Depo içindeyken aşağıdaki 19 komutunu kullanarak ilgili kategoride (tarih
   verilmiş, fakat henüz isimlendirilmemiş) bir girdi açın.  Çoğu durumda
   "`<kategori>`"nin yazılması gerekmeyebilir.  Kategori verilmezse ilgili
   şablonun tanımladığı kategori kullanılır.

            $ git 19 sayfa yeni <kategori> <şablon>

            # veya depo Git kısayoluyla:
            $ git y <kategori> <şablon>

3. Yeni oluşturduğunuz girdi `isimsiz` olarak adlandırılacaktır.  Öncelikle
   girdinin ismini uygun anahtar kelimelerden oluşan bir başlıkla değiştirin.
   Örneğin `1` kategorisinde "GitHub'a Giriş" başlıklı bir girdi oluşturdunuz.
   Bu girdinin dosyayolu başlangıçta `1/_posts/2010-09-19-isimsiz.md`
   olacaktır (girdinin oluşturulma tarihine göre sizdeki tarih farklı
   olabilir).  Verilen başlığa uygun olarak ismi "`github-giris`" olarak
   değiştirin.  Bu şekilde dosyayolu `1/_posts/2010-09-19-github-giris.md`
   olarak değişecektir.

4. Son olarak girdiyi depoya ekleyin ve GitHub'a gönderin.  Yukarıdaki örnekle
   anlatılacak olursa:

            $ git add 1/_posts/2010-09-19-github-giris.md
            $ git commit -m "yeni girdi: github-giris"
            $ git push origin master

### Sayfa Düzenleme

İlgili sayfayı herhangi bir metin düzenleyicide açarak düzenlemeniz ve
değişiklikleri GitHub'a göndermeniz yeterlidir.  Yeni girdi ekledikten sonra
sıklıkla yaşanan "son eklenen girdiyi aç - düzenle - çık" çevrimini
kolaylaştırmak amacıyla aşağıdaki 19 komutunu kullanabilirsiniz.

            $ git 19 sayfa enson

Kurulum sırasında bu komut için `e` kısayolu eklenmektedir.  Aynı işlemi daha
kısa olarak şu komutla da yapabilirsiniz.

            $ git e

Bu komut kategori numarasını en son düzenleme yapılan kategori dizinine
bakarak otomatik şekilde belirlemektedir.  Depoya yeni bir girdi ekledikten
sonra, başka bir kategoride elle düzenleme yapmışsanız komut, son eklenen
girdiyi değil, o kategorinin son girdisini açar.  Böyle bir durumda son
eklenen girdiyi düzenlemek için kategori numarasını açık şekilde vermelisiniz.

            $ git e <kategori>

Belgeyi düzenledikten sonra değişiklikleri, uygun bir açıklamayla depoya
kaydedip GitHub'a göndermeyi unutmayın.  Örneğin bir imla hatası
düzeltmişseniz:

            $ git commit -m "imla hatasını düzelt"
            $ git push origin master

Tüm bu adımlar aşağıdaki "Gedit" canlandırmasında izlenebilir.

### Siteyi Test Etme

Siteyi test etmek için GitHub'a test gönderileri göndermenize gerek yoktur.
Jekyll'ı kendi makinenize kurarak (bu işlem kurulum sırasında yapılmaktadır)
program tarafından sunulan ve `localhost:4000` adresinde servis yapan yerel
sunucuyu kullanabilirsiniz.

- Test sunucusunu çalıştırın.

            $ git 19 sayfa test
            # veya depo Git kısayoluyla:
            $ git t

- Tarayıcınızda [localhost:4000](http://localhost:4000) yerel adresine girin.

- Depoda değişiklik yaptığınızda üretilen site de (`_site` dizini) otomatik
  olarak güncellenecektir.

  **Dikkat!**  `_config.yml` dosyasında yaptığınız değişiklikler otomatik
  olarak etkinleşmeyecektir.  Bu dosyada değişiklik yapmışsanız yukarıdaki
  komutu tekrar çalıştırın.

### Kaynaklar

Sitenizde ileri düzeyde özelleştirmeler yapmak için aşağıdaki kaynaklara da
başvurabilirsiniz.

- [GitHub sayfaları hakkında GitHub dokümantasyonu](http://pages.github.com/)

- [Jekyll dokümantasyonu](http://wiki.github.com/mojombo/jekyll/)

- [Liquid şablonlama sistemi](http://wiki.github.com/tobi/liquid/)


## Sayfa Kategorilerinin Seçimi

Sayfanın kategorisini belirlemek için aşağıdaki sorgulamayı yapabilirsiniz.

**`0`** Sayfa, "öğreten" olmaktan çok kişisel görüş ve deneyimlerinizi
yansıtan (örneğin bir günlük girdisi gibi) kişisel bir sayfa mı?  Evet ise `0`
kategorisini kullanın.  Örnekte cevap **hayır** .  Eğer örnekteki sayfa
Ubuntu'nun son sürümü hakkındaki görüşlerinizi anlatan bir sayfa olsaydı bu
kategoriyi kullanabilirdiniz.

**`9`** Teknik nitelikteki bu sayfa, kısa bir bilgi notu mu?  Evet ise `9`
kategorisini kullanın.  Örnekte cevap **hayır**.  Eğer örnekteki sayfa basitçe
GitHub'ın tek bir özelliğini birkaç paragrafta anlatan kısa bir bilgi notu
olsaydı `9` kategorisini kullanabilirdiniz.

**`2`** Sayfa, teknik bir konuyu bilgi yönünden sunmaktan çok, izlenmesi
gereken ilke veya pratikler yönünden mi ele alıyor?  Örnekte cevap (büyük
ölçüde) **hayır**.  Eğer örnekteki sayfa GitHub üzerinden birlikte çalışma
sırasında uyulması gereken bir prosedürü anlatan bir sayfa olsaydı `2`
kategorisini kullanabilirdiniz.

**`1`** Sayfa, teknik bir konuyu "öğreten" üslubunda sunan (örneğin bir
"NASIL" veya "tutoryal" gibi) göreceli olarak uzun bir sayfa mı?  Bu tür
sayfalar uzun olması, bir veya birkaç küçük bilgiden çok daha fazlasını
içermesi yönüyle `9` kategorisinden ayrılmaktadır.  Örnekte cevap **evet**.

**`7`** Yukarıdaki kategorilerin hiçbirine uymuyorsa (nadir bir durum) `7`
kategorisini kullanabilirsiniz.

## Sıkça Sorulan Sorular

### Site Görünümünü Nasıl Değiştirebilirim?

"`0-1-2-7-9`" sayfalama modeline uymak kaydıyla site görünümünü istediğiniz
şekilde değiştirebilirsiniz.  Bu değişiklikleri "hafiften ağıra" şekilde
sıralarsak:

- Sitede kullanılan logo'yu `param.logo` parametresiyle değiştirebilirsiniz.
  Bu parametreyi `~` olarak ayarlarsanız logo görüntülenmez.

- Sitede kullanılan CSS'yi "üzerine yazma" yoluyla değiştirmek için depodaki
  `chrome/local.css` dosyasını düzenleyebilirsiniz.

- Sitede Jekyll tarafından üretilen HTML çıktılarda yerleşim şablonu olarak
  `_layouts` dizini altındaki dosyalar kullanılmaktadır.  Bu dizinde kendi
  özel yerleşimlerinizi oluşturarak kullanabilirsiniz.  Fakat **dikkat**,
  şablondan (`template` dalı) mevcut olan dosyaları, örneğin
  `_layouts/site-default.html`, düzenlemek yerine bu dosyanın bir kopyasını
  farklı bir isimle oluşturarak değişikliklerinizi bu dosyada yapın.

### Site Yerleşimini Nasıl Değiştirebilirim?

HTML çıktı üretmekte kullanılan Jekyll yerleşim şablonları `_layouts`
dizininde bulunmaktadır.  Özelleştirmelerde bu dizinde gelen şablonları
değiştirmek yerine önce kendi dosyanızı oluşturun ve daha sonra ilgili ana
şablonu bu dosyayı gösterecek şekilde değiştirin.  Örneğin `default.html`
şablonunu özelleştirmek için:

- Kendi şablonunuzu, örneğin `local-default.html` ismiyle oluşturun.
  şablondan gelen `site-default.html`'ye dokunmayın, ama başlangıç noktası
  olarak bu dosyayı `local-default.html` adıyla kopyalayabilirsiniz.

- Kurulum sırasında eklenen `default.html` ana şablon dosyasını bir önceki
  adımda oluşturduğunuz `local-default.html` dosyasını gösterecek şekilde
  değiştirin.  Örnek:

            ---
            layout: local-default
            ---
            {{ content }}

### Site Şablonundaki Değişiklikleri Nasıl Alabilirim?

Sitenizi bu sayfanın ilk bölümündeki adımları izleyerek oluşturmuş iseniz
deponuzda `19` isimli bir başvuruya sahipsiniz demektir.  Bu başvurudaki
`template` isimli dalda site şablonundaki en temel (ve değiştirmemiş olmanızı
beklediğimiz) dosyalar bulunmaktadır.  Aşağıdaki komutları kullanarak bu
daldaki değişiklikleri yayının yapıldığı dala (`master` veya `gh-pages`)
uygulayabilirsiniz.

            $ git fetch 19
            $ git merge 19/template

**Dikkat!**  Bu depoda `19/template` isimli dalda bulunan dosyalardan herhangi
birini değiştirmiş iseniz yukarıdaki işlemler sonucunda, elle müdahele yoluyla
çözmeniz gereken bir "birleştirme uyuşmazlığı" ("merge conflict") ile
karşılaşabilirsiniz.  Bu nedenle lütfen `19/template`'de de bulunan dosyaları
değiştirmeyin.  Bu dalda bulunan bir dizin altında (ör. `_layouts`) yeni bir
dosya oluşturabilirsiniz, bunun herhangi bir sakıncası yoktur.

### Depoda Ne Nedir?

Depodaki dosya/dizinler ve işlevleri şunlardır:

- `_config.yml`: Jekyll yapılandırma dosyası (YAML formatında).  Deponun pek
  çok özelliğini sadece bu dosyayı düzenleyerek değiştirebilirsiniz.

- `index.html`: Web sitesinin kök adresinde görüntülenecek dosya.

- `0`, `1`, `2`, `7` ve `9`: Bu bölüm dizinleri ilgili "Kurallar" sayfasında
  dokümante edilmiştir.  Site gönderileri bu dizinlerdeki `_posts` alt
  dizininde bulunmaktadır.

- `_layouts`: Depoya ekleyeceğiniz girdilerden HTML çıktı üretmekte
  kullanılacak olan Jekyll şablonları.  Ayrıntılı bilgi için lütfen [Jekyll
  NASIL](TODO) sayfasını okuyun.

- `_includes`: Şablonlarda kullanılan "işlev" parçaları.  Bu şablon depoda
  bulunan işlevler, özelleştirilmesi zor büyük dosyalar yerine, parçalı halde
  bu dizindeki dosyalara dağıtılmıştır.  Yapacağınız özelleştirmelerde ilgili
  parçaları `include` ederek o özellikten yararlanabilirsiniz.  Herhangi bir
  parçayı kullanmak için Jekyll `include` etiketini kullanın.

- `_templates`: Belirli türde girdileri çabuk şekilde oluşturmaya yarayan
  şablonları bu dizine koyabilirsiniz.  Bu dizinde ayrıca kurulum sırasında
  kullanılan çeşitli dosyalar da bulunmaktadır.

- `chrome`: Depo özelleştirmesinde, içeriklerde kullanacağınız "sayısal
  varlık"ların (ör. görseller, resimler, CSS dosyaları, JavaScript betikleri)
  tutulacağı dizin.  Site görünümü ve işlevleriyle ilgili her türlü dosya bu
  dizinde tutulur.  Örnek dosyalar:

    + logo, arka plan resim vb görseller

    + css dosyaları

    + JavaScript betikleri

  Site görünümünü özelleştirmek için `local.css` dosyasını kullanılır.  Bu
  dizindeki dosyalara (ikinci seviye dizinlerde) aşağıdaki göreceli yolla
  erişilebilir:

            ![<isim>](../chrome/<dosya>)

  **Dikkat!**  İçeriklerde kullanılan her türlü görsel `images` dizinindedir.

- `images`: İçeriklerde kullanılan görseller bu dizinde tutulur.  Bu dizindeki
  dosyalara (ikinci seviye dizinlerde) aşağıdaki göreceli yolla erişilebilir:

            ![<isim>](../images/<dosya>)

  **Dikkat!**  Site görünümünü düzenleyen görseller (ör. logo, arka plan)
  `chrome` dizinindedir.

- `atom.xml`: Depodan üretilen sitenin kök dizininde yayın yapacak "Atom" özet
  akışı tanımı.

- `404.html`: Web siteniz GitHub'da yayımlanıyorsa, bulunamayan dosyalar için
  üretilen `404` hataları bu sayfaya yönlendirilecektir.  (Not: GitHub'ın
  `404` yönlendirme özelliği geçici olarak kaldırılmıştır.)

### Mevcut GitHub Sitemi Bu Sisteme Nasıl Taşırım?

Aşağıdaki adımları izleyin:

- GitHub'daki eski depoyu silin.  Depo kopyasının makinenizde `<eski_depo>`
  adıyla zaten bulunduğunu varsayıyoruz.

- Bu sayfada anlatılan şekilde kurulum yapın.

- Mevcut sayfalarınızı "`0-1-2-7-9`" modeline uyarlayın.  Hangi sayfa hangi
  kategoride olmalı bunu belirleyin ve ilgili kategoride bir dizin açarak
  taşıma yapın.

- Aktarılan girdileri kontrol ettikten sonra yeni depoya gönderin.

            $ git add 0 1
            $ git commit -a -m "eski site aktarıldı"
            $ git push origin master

### `0-1-2-7-9` Sayfalama Sistemi Nedir?

TODO

## Atıf

Şablon sitenin mevcut görünümünde Jekyll'ın yazarı [Tom
Preston-Werner'in](http://github.com/mojombo) kişisel sitesindeki görünüm esas
alınmıştır.
