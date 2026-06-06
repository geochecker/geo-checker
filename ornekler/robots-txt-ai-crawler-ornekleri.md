# robots.txt ve AI Crawler Örnekleri

Bu dosya, web sitelerinde `robots.txt` dosyasının yapay zeka botları ve arama motoru crawler’ları açısından nasıl yapılandırılabileceğini göstermek için hazırlanmıştır.

`robots.txt`, hangi botların hangi alanları tarayabileceğini belirtmeye yardımcı olur. Ancak tek başına güvenlik mekanizması değildir ve tüm botların bu kurallara uyacağı garanti edilemez.

## robots.txt nedir?

`robots.txt`, web sitenizin kök dizininde bulunan bir metin dosyasıdır.

Örnek konum:

```
https://example.com/robots.txt
```

Bu dosya, arama motorlarına ve crawler’lara hangi sayfaların taranabileceği veya taranmaması gerektiği hakkında yönergeler verir.

## Temel robots.txt örneği

Aşağıdaki yapı, genel olarak tüm botlara siteyi tarama izni verir ve sitemap dosyasını belirtir.

```
User-agent: *
Allow: /

Sitemap: https://example.com/sitemap.xml
```

## Tüm botları engelleyen örnek

Bu yapı tüm botların siteyi taramasını engeller.

```
User-agent: *
Disallow: /
```

Bu yapı, public bir web sitesi için genellikle önerilmez. Çünkü arama motorları ve yapay zeka crawler’ları içeriği keşfedemez.

## Belirli klasörleri engelleyen örnek

Aşağıdaki örnekte tüm botlara genel erişim verilir, ancak yönetim paneli ve özel dosyalar engellenir.

```
User-agent: *
Allow: /

Disallow: /admin/
Disallow: /panel/
Disallow: /private/
Disallow: /checkout/
Disallow: /cart/

Sitemap: https://example.com/sitemap.xml
```

## Yapay zeka crawler’ları için dikkat edilmesi gerekenler

GEO yani Generative Engine Optimization açısından, web sitesinin önemli içeriklerinin yapay zeka sistemleri tarafından erişilebilir olması önemlidir.

Aşağıdaki durumlar AI görünürlüğünü ve teknik GEO hazırlığını olumsuz etkileyebilir:

* Tüm botları engellemek
* Önemli içerik klasörlerini yanlışlıkla engellemek
* Sitemap bağlantısı eklememek
* Sayfada `noindex` kullanmak
* `nosnippet` veya çok kısıtlayıcı `max-snippet` kullanmak
* İçeriği yalnızca JavaScript ile sonradan yüklemek
* Giriş yapmadan görülemeyen içerikleri ana içerik gibi kullanmak

## AI crawler erişimine izin veren örnek yapı

Bu örnek, genel crawler erişimini açık tutar ve sitemap dosyasını belirtir.

```
User-agent: *
Allow: /

Disallow: /admin/
Disallow: /panel/
Disallow: /private/

Sitemap: https://example.com/sitemap.xml
```

## GEO Checker için örnek robots.txt yapısı

Aşağıdaki örnek, GEO Checker gibi public bir SEO/GEO aracı için uygun temel yapıyı gösterir.

```
User-agent: *
Allow: /

Disallow: /app/
Disallow: /admin/
Disallow: /panel/
Disallow: /checkout/
Disallow: /cart/

Sitemap: https://geochecker.com.tr/sitemap.xml
```

## robots.txt ile llms.txt farkı

`robots.txt`, crawler’lara hangi alanların taranabileceği konusunda yönerge verir.

`llms.txt` ise yapay zeka sistemlerine sitenin kim olduğunu, hangi sayfaların önemli olduğunu ve içeriğin nasıl anlaşılması gerektiğini daha net anlatmaya yardımcı olabilir.

Kısaca:

* `robots.txt`: erişim ve tarama yönergeleri
* `llms.txt`: yapay zeka sistemleri için site özeti ve önemli bağlantılar
* `sitemap.xml`: önemli URL’lerin keşfi
* `schema.org`: sayfadaki varlıkların makine-okunabilir tanımı

## Teknik GEO denetimi için kontrol listesi

Bir web sitesinde `robots.txt` kontrol edilirken şu sorular sorulmalıdır:

* `robots.txt` dosyası erişilebilir mi?
* Dosya 200 HTTP durum kodu döndürüyor mu?
* Tüm site yanlışlıkla engellenmiş mi?
* Önemli sayfalar veya klasörler engellenmiş mi?
* Sitemap bağlantısı belirtilmiş mi?
* Gereksiz veya eski Disallow kuralları var mı?
* AI crawler erişimini etkileyebilecek genel engeller var mı?
* Sayfa seviyesinde `noindex`, `nofollow` veya `nosnippet` direktifleri var mı?

## GEO Checker ile kontrol edin

Web sitenizin `robots.txt`, `llms.txt`, sitemap, schema ve diğer teknik GEO sinyallerini kontrol etmek için GEO Checker kullanabilirsiniz.

Ücretsiz GEO skoru kontrolü:

https://geochecker.com.tr/
