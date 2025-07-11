# Hastane Randevu Sistemi

Bu proje web tabanlı bir hastane randevu sistemidir. 

*Bu program ile;*

- Yaklaşan randevular görünebilir,

- Yeni randevular, hasta ve doktor kaydı oluşturulabilir,

- Tüm randevular incelenebilir.

## Proje Yapısı

```
Lv3 Final Projesi/
├── app.py                 # Ana Flask uygulaması
├── database.py            # Veritabanı işlemleri
├── requirements.txt       # Python bağımlılıkları
├── README.md             # Proje dokümantasyonu
├── appointments.db       # SQLite veritabanı dosyası
├── tests/                # Test dosyaları
│   ├── __init__.py
│   ├── test_app.py       # Flask uygulama testleri
│   └── test_database.py  # Veritabanı testleri
├── config/               # Konfigürasyon dosyaları
│   └── pytest.ini       # Pytest ayarları
├── scripts/              # Yardımcı scriptler
│   └── run_tests.py     # Test çalıştırıcı
├── static/               # Statik dosyalar
│   ├── css/
│   │   └── style.css
│   └── img/
└── templates/            # HTML şablonları
    ├── index.html
    ├── about.html
    ├── contact.html
    ├── appointments.html
    ├── add_appointment.html
    └── add_doctor.html
```

## Test Etme

Bu proje kapsamlı testler içerir. Testleri çalıştırmak için:

### Gereksinimler
```bash
pip install -r requirements.txt
```

### Testleri Çalıştırma

#### Tüm Testleri Çalıştır
```bash
python scripts/run_tests.py
```

#### Belirli Test Dosyasını Çalıştır
```bash
python scripts/run_tests.py tests/test_database.py
python scripts/run_tests.py tests/test_app.py
```

#### Pytest ile Doğrudan Çalıştır
```bash
pytest -v                           # Tüm testler
pytest tests/test_database.py -v    # Sadece veritabanı testleri
pytest tests/test_app.py -v         # Sadece Flask uygulama testleri
```

### Test Kapsamı

#### Veritabanı Testleri (`tests/test_database.py`)
- Veritabanı başlatma ve tablo oluşturma
- Hasta ekleme, listeleme ve arama
- Doktor ekleme, listeleme ve arama
- Randevu ekleme, güncelleme, silme
- İstatistik hesaplama
- Veritabanı kısıtlamaları

#### Flask Uygulama Testleri (`tests/test_app.py`)
- Tüm route'ların çalışması
- Form gönderimi ve veri işleme
- API endpoint'leri
- Hata yönetimi
- Randevu durumu güncelleme

### Test Yapısı

```
tests/
├── __init__.py          # Test paketi başlatıcı
├── test_database.py     # Veritabanı işlemleri testleri
└── test_app.py         # Flask uygulama testleri

config/
└── pytest.ini         # Pytest konfigürasyonu

scripts/
└── run_tests.py       # Test çalıştırıcı script
```
