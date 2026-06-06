# Schema.org ve JSON-LD Örnekleri

Bu dosya, web sitelerinin yapay zeka sistemleri ve arama motorları tarafından daha net anlaşılmasına yardımcı olan temel Schema.org ve JSON-LD örneklerini içerir.

Schema.org ve JSON-LD, bir sayfadaki marka, web sitesi, uygulama, ürün, hizmet, makale veya sık sorulan soru gibi varlıkları makine-okunabilir şekilde tanımlamaya yardımcı olur.

## Schema neden GEO için önemlidir?

GEO, yani Generative Engine Optimization, web sitelerinin yapay zeka cevap motorları tarafından daha iyi anlaşılmasını hedefler.

Schema.org ve JSON-LD kullanımı şu konularda yardımcı olabilir:

* Marka adını netleştirmek
* Web sitesinin resmi URL’sini belirtmek
* Logo ve sosyal profilleri tanımlamak
* Ürün veya hizmetin ne olduğunu anlatmak
* Sık sorulan soruları yapılandırmak
* Web uygulamasının amacını açıklamak
* İçeriğin bağlamını makine-okunabilir hâle getirmek

## Organization schema örneği

Aşağıdaki örnek, bir markayı veya şirketi tanımlamak için kullanılabilir.

```
{
  "@context": "https://schema.org",
  "@type": "Organization",
  "@id": "https://example.com/#organization",
  "name": "Marka Adı",
  "url": "https://example.com/",
  "logo": {
    "@type": "ImageObject",
    "url": "https://example.com/logo.png"
  },
  "sameAs": [
    "https://www.linkedin.com/company/example",
    "https://github.com/example",
    "https://x.com/example"
  ]
}
```

## WebSite schema örneği

Aşağıdaki örnek, web sitesini tanımlamak için kullanılabilir.

```
{
  "@context": "https://schema.org",
  "@type": "WebSite",
  "@id": "https://example.com/#website",
  "name": "Marka Adı",
  "url": "https://example.com/",
  "inLanguage": "tr",
  "publisher": {
    "@id": "https://example.com/#organization"
  }
}
```

## WebApplication schema örneği

Aşağıdaki örnek, web tabanlı bir araç veya uygulama için kullanılabilir.

```
{
  "@context": "https://schema.org",
  "@type": "WebApplication",
  "@id": "https://example.com/#webapp",
  "name": "Uygulama Adı",
  "url": "https://example.com/",
  "applicationCategory": "SEOApplication",
  "operatingSystem": "All",
  "browserRequirements": "Requires JavaScript",
  "isAccessibleForFree": true,
  "inLanguage": "tr",
  "description": "Bu uygulama, web sitelerinin teknik SEO ve GEO sinyallerini analiz eder.",
  "offers": {
    "@type": "Offer",
    "price": "0",
    "priceCurrency": "USD"
  },
  "publisher": {
    "@id": "https://example.com/#organization"
  }
}
```

## FAQPage schema örneği

Aşağıdaki örnek, sayfada gerçekten görünen sık sorulan sorular için kullanılmalıdır.

```
{
  "@context": "https://schema.org",
  "@type": "FAQPage",
  "@id": "https://example.com/#faq",
  "mainEntity": [
    {
      "@type": "Question",
      "name": "GEO nedir?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "GEO, Generative Engine Optimization anlamına gelir. Web sitelerinin yapay zeka cevap motorları tarafından daha iyi anlaşılması için yapılan optimizasyonları ifade eder."
      }
    },
    {
      "@type": "Question",
      "name": "Schema GEO için neden önemlidir?",
      "acceptedAnswer": {
        "@type": "Answer",
        "text": "Schema, web sitesindeki marka, ürün, hizmet veya içerik gibi varlıkları makine-okunabilir şekilde tanımlamaya yardımcı olur."
      }
    }
  ]
}
```

## GEO Checker için örnek JSON-LD yapısı

Aşağıdaki örnek, GEO Checker gibi Generative Engine Optimization odaklı bir web uygulaması için hazırlanmıştır.

```
{
  "@context": "https://schema.org",
  "@graph": [
    {
      "@type": "Organization",
      "@id": "https://geochecker.com.tr/#organization",
      "name": "GEO Checker",
      "url": "https://geochecker.com.tr/",
      "logo": {
        "@type": "ImageObject",
        "url": "https://geochecker.com.tr/logo.png"
      },
      "sameAs": [
        "https://github.com/geochecker",
        "https://dev.to/geochecker",
        "https://medium.com/@geochecker",
        "https://x.com/geocheckercomtr",
        "https://www.linkedin.com/company/geo-checker"
      ]
    },
    {
      "@type": "WebSite",
      "@id": "https://geochecker.com.tr/#website",
      "name": "GEO Checker",
      "alternateName": [
        "GEO Skoru Kontrol Aracı",
        "AI Bot Kontrol Aracı",
        "Generative Engine Optimization Aracı"
      ],
      "url": "https://geochecker.com.tr/",
      "inLanguage": "tr",
      "publisher": {
        "@id": "https://geochecker.com.tr/#organization"
      }
    },
    {
      "@type": "WebApplication",
      "@id": "https://geochecker.com.tr/#webapp",
      "name": "GEO Checker",
      "url": "https://geochecker.com.tr/",
      "applicationCategory": "SEOApplication",
      "operatingSystem": "All",
      "isAccessibleForFree": true,
      "inLanguage": "tr",
      "description": "GEO Checker, web sitelerinin AI botlar, ChatGPT, Perplexity, Gemini ve Google AI gibi cevap motorları için teknik olarak ne kadar hazır olduğunu analiz eden ücretsiz GEO skoru ve yapay zeka uygunluk kontrol aracıdır.",
      "featureList": [
        "Ücretsiz GEO skoru kontrolü",
        "AI bot ve crawler erişim kontrolü",
        "robots.txt denetimi",
        "llms.txt kontrolü",
        "XML sitemap kontrolü",
        "Schema.org ve JSON-LD kontrolü",
        "Teknik GEO denetimi"
      ],
      "offers": {
        "@type": "Offer",
        "price": "0",
        "priceCurrency": "USD"
      },
      "publisher": {
        "@id": "https://geochecker.com.tr/#organization"
      }
    }
  ]
}
```

## Schema kullanırken dikkat edilecekler

* JSON-LD geçerli JSON formatında olmalıdır.
* Virgül hatalarına dikkat edilmelidir.
* Sayfada görünmeyen FAQ içerikleri FAQPage schema içine eklenmemelidir.
* Marka adı, logo, URL ve sosyal profiller tutarlı olmalıdır.
* `sameAs` alanına yalnızca gerçekten markaya ait profiller eklenmelidir.
* Her sayfaya gereksiz schema eklenmemelidir.
* Schema görünürlük garantisi vermez; teknik anlamlandırma sinyali sağlar.

## GEO Checker ile kontrol edin

Web sitenizin Schema.org, JSON-LD, `llms.txt`, `robots.txt`, sitemap ve diğer teknik GEO sinyallerini kontrol etmek için GEO Checker kullanabilirsiniz.

Ücretsiz GEO skoru kontrolü:

https://geochecker.com.tr/
