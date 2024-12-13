
# Proxy Aracı

## Genel Bakış

**Proxy Aracı**, proxy'leri çekmek ve doğrulamak için kapsamlı bir Python tabanlı araçtır. Birden fazla API kaynağından proxy'leri almayı, geçerliliğini kontrol etmeyi ve gelecekteki kullanım için kaydetmeyi destekler. Araç, kullanıcı dostu bir menü sistemi ve görsel olarak çekici ASCII sanat display'ine sahiptir.

## Özellikler

- **Proxy Çekici**: Güvenilir API kaynaklarından proxy'ler toplar ve bir dosyaya kaydeder.
- **Proxy Doğrulayıcı**: Alınan proxy'lerin geçerliliğini hedef bir web sitesine bağlantı testi yaparak doğrular.
- **Günlük Proxy Sayısı**: Gün içinde toplanan toplam proxy sayısını takip eder.
- **Geliştirici Bilgisi**: Yaratıcının iletişim bilgilerini görüntüler.
- **Etkileşimli Menü**: Özellikler arasında gezinmeyi sağlayan basit ve kullanıcı dostu bir arayüz.

## Nasıl Çalışır

1. **Proxy Çekme**:
   - Aşağıdaki API'lerden proxy'ler toplar:
     - [ProxyScrape](https://api.proxyscrape.com)
     - [Proxy-List.download](https://www.proxy-list.download)
     - [TheSpeedX Proxy List](https://github.com/TheSpeedX/PROXY-List)
     - [ProxyScan](https://www.proxyscan.io)
     - [OpenProxyList](https://api.openproxylist.xyz)
   - Geçersiz veya boş girişleri filtreler ve geçerli olanları bir günlük dosyasına kaydeder.

2. **Proxy Doğrulama**:
   - Her proxy'nin geçerliliğini `http://www.google.com` adresine bağlantı kurarak test eder.
   - Geçerli proxy'ler `valid_proxies.txt` dosyasına, geçersiz olanlar ise `invalid_proxies.txt` dosyasına kaydedilir.

3. **Günlük Sayım**:
   - Bugün toplanan toplam proxy sayısını görüntüler.

## Kullanım

1. Depoyu klonlayın:
   ```bash
   git clone https://github.com/Ladorex/proxy-tool.git
   cd proxy-tool
   ```

2. Gerekli bağımlılıkları yükleyin:
   ```bash
   pip install requests
   ```

3. Aracı çalıştırın:
   ```bash
   python proxy_tool.py
   ```

## Menü Seçenekleri

- **1. Proxy Çekici**: Belirlenen API listesinden proxy toplamaya başlar.
- **2. Proxy Doğrulayıcı**: Toplanan proxy'leri doğrular.
- **3. Günlük Proxy Sayısı**: Bugün toplanan proxy sayısını görüntüler.
- **4. Geliştirici Hesapları**: Yaratıcının Instagram ve GitHub hesaplarını görüntüler.
- **5. Çıkış**: Uygulamayı kapatır.

## Örnek Çıktılar

### Proxy Çekici
```
Proxies kaydedildi: 2024-12-14_log.txt
```

### Proxy Doğrulayıcı
```
[92mGeçerli Proxy: 123.456.78.90:8080[0m
[91mGeçersiz Proxy: 98.765.43.21:3128[0m
```

### Günlük Sayım
```
Bugün Toplanan Proxy Sayısı: 150
```

## Geliştirici

- **Instagram**: [@ladorex.1](https://instagram.com/ladorex.1)
- **GitHub**: [@Ladorex](https://github.com/Ladorex)

## Lisans

Bu proje MIT Lisansı altında lisanslanmıştır. Ayrıntılar için `LICENSE` dosyasına bakınız.
