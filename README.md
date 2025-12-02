# İnşaat Yönetim Sistemi

Yapı denetim firmaları için geliştirilmiş kapsamlı inşaat yönetim ve takip sistemi.

## 🚀 Özellikler

- **Şantiye Denetimleri**: Saha denetimlerinin detaylı kaydı ve takibi
- **Hakediş Yönetimi**: Hakediş ödemeleri ve evrak takibi
- **Ruhsat ve Proje Yönetimi**: Ruhsat süreçleri ve proje dosyalarının yönetimi
- **Kullanıcı Yönetimi**: Rol tabanlı erişim kontrolü (Super Admin, Admin, User)
- **İş Planlama**: Gelecek denetim ve işlerin planlanması
- **Firma Yönetimi**: Laboratuvar ve beton firmaları yönetimi
- **Aktivite Logları**: Tüm sistem aktivitelerinin detaylı kaydı
- **İnşaat Listesi**: Excel ile toplu inşaat verisi yükleme

## 📋 Teknoloji Stack

### Backend
- **FastAPI** (Python 3.8+)
- **MongoDB** (Motor - Async Driver)
- **JWT** Authentication
- **Bcrypt** (Password Hashing)
- **Pandas** (Excel Processing)

### Frontend
- **React 19**
- **React Router v7**
- **Radix UI** (UI Components)
- **Tailwind CSS**
- **Axios** (HTTP Client)
- **Craco** (Webpack Configuration)

## 🛠️ Kurulum

### Gereksinimler

- Python 3.8 veya üzeri
- Node.js 16 veya üzeri
- MongoDB 4.4 veya üzeri
- Yarn package manager

### Backend Kurulumu

1. Backend dizinine gidin:
```bash
cd backend
```

2. Python sanal ortamı oluşturun (opsiyonel ama önerilir):
```bash
python -m venv venv
source venv/bin/activate  # Linux/Mac
# veya
venv\Scripts\activate  # Windows
```

3. Gerekli paketleri yükleyin:
```bash
pip install -r requirements.txt
```

4. `.env` dosyası oluşturun:
```bash
cp .env.example .env
```

5. `.env` dosyasını düzenleyin ve gerekli ayarları yapın:
```env
MONGO_URL=mongodb://localhost:27017/
DB_NAME=construction_management
JWT_SECRET_KEY=your-very-strong-secret-key-min-32-characters
CORS_ORIGINS=http://localhost:3000
```

6. Backend sunucusunu başlatın:
```bash
uvicorn server:app --host 0.0.0.0 --port 8001 --reload
```

### Frontend Kurulumu

1. Frontend dizinine gidin:
```bash
cd frontend
```

2. `.env` dosyası oluşturun:
```bash
cp .env.example .env
```

3. `.env` dosyasını düzenleyin:
```env
REACT_APP_BACKEND_URL=http://localhost:8001
```

4. Bağımlılıkları yükleyin:
```bash
yarn install
```

5. Frontend sunucusunu başlatın:
```bash
yarn start
```

Uygulama `http://localhost:3000` adresinde çalışacaktır.

## 📝 İlk Kullanıcı Oluşturma

Sistemde ilk kullanıcıyı oluşturmak için:

1. `http://localhost:3000/register` adresine gidin
2. İlk kayıt olan kullanıcı otomatik olarak **Super Admin** rolü alır
3. Giriş yapın ve diğer kullanıcıları "Kullanıcılar" menüsünden ekleyin

## 🔐 Kullanıcı Rolleri

- **Super Admin**: Tüm yetkilere sahip, kullanıcı yönetimi yapabilir
- **Admin**: Kayıtları düzenleyebilir ve silebilir
- **User**: Sadece kayıtları görüntüleyebilir, oluşturabilir

## 📚 API Dokümantasyonu

Backend çalıştıktan sonra API dokümantasyonuna şu adreslerden erişebilirsiniz:

- Swagger UI: `http://localhost:8001/docs`
- ReDoc: `http://localhost:8001/redoc`

## 🔧 Geliştirme

### Backend Linting
```bash
cd backend
flake8 server.py
```

### Frontend Linting
```bash
cd frontend
yarn lint
```

## 🚨 Önemli Güvenlik Notları

1. **JWT_SECRET_KEY**: Mutlaka güçlü, rastgele bir anahtar kullanın (minimum 32 karakter)
2. **CORS_ORIGINS**: Production'da mutlaka sadece güvenilir domainleri ekleyin
3. **MongoDB**: Production'da authentication aktif olmalı
4. **HTTPS**: Production'da mutlaka HTTPS kullanın

## 📄 Lisans

Bu proje özel bir proje olup, ticari kullanım için izin gereklidir.

## 🤝 Destek

Sorularınız için lütfen proje yöneticisi ile iletişime geçin.
