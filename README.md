# Anaokulu Yönetim Sistemi

Veliler okulun duyurularını, etkinlik takvimini ve haftalık yemek listesini web üzerinden takip edebilir. Bu depo ASP.NET Core MVC uygulamasını ve mobil uygulamanın kullandığı API'yi içerir. [React Native mobil uygulaması](https://github.com/HamzaAkilotu/AnaokuluYSMobil)

## Kodda nereden başlamalı?

| İncelemek istediğin bölüm | İlgili dosya veya klasör |
| --- | --- |
| Velinin gördüğü haftalık yemek listesi | [Yemek listesi görünümü](Views/Home/HaftalikYemekListesi.cshtml) |
| Mobil uygulamaya veri sağlayan uç noktalar | [API denetleyicileri](Controllers/Api) |
| Veri modeli ve şema değişiklikleri | [ApplicationDbContext](Data/ApplicationDbContext.cs) ve [migration dosyaları](Migrations) |

## Yerelde çalıştırma

.NET 8 SDK, SQL Server ve Entity Framework Core 9 ile uyumlu `dotnet-ef` aracı gerekir.

1. Bu depoyu klonlayıp `AnaOkuluYS.csproj` dosyasının bulunduğu klasöre geç.
2. `ConnectionStrings__DefaultConnection` ortam değişkenini kendi geliştirme veritabanının SQL Server bağlantı dizesine ayarla.
3. Paketleri yükle, geliştirme veritabanına migration'ları uygula ve uygulamayı başlat.

```sh
dotnet restore
dotnet ef database update
dotnet run
```

Terminalde gösterilen yerel adresi tarayıcıda aç.
