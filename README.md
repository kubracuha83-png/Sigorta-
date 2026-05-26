# Sigorta Arama Motoru 🔍

Müşteri kazanımı için gelişmiş arama motoru sistemi.

## 🎯 Özellikler

- ✅ Müşteri veritabanı araması
- ✅ Sigorta ürünlerine göre filtreleme
- ✅ Coğrafi bölge araması
- ✅ Fiyat aralığı filtresi
- ✅ Hızlı ve verimli arama (Elasticsearch)
- ✅ REST API
- ✅ Web arayüzü

## 🛠️ Teknoloji Stack

- **Backend**: Python 3.9+
- **Framework**: Flask
- **Database**: PostgreSQL
- **Search Engine**: Elasticsearch 7.x+
- **Frontend**: HTML5, CSS3, JavaScript

## 📋 Gereksinimler

- Python 3.9+
- PostgreSQL 12+
- Elasticsearch 7.x+
- pip

## 🚀 Kurulum

### 1. Ortam Hazırlığı

```bash
git clone https://github.com/kubracuha83-png/Sigorta-.git
cd Sigorta-

python -m venv venv

# Windows:
venv\Scripts\activate
# Linux/Mac:
source venv/bin/activate
```

### 2. Bağımlılıkları Yükleyin

```bash
pip install -r backend/requirements.txt
```

### 3. Veritabanı Kurulumu

```bash
psql -U postgres -f database/schema.sql
```

### 4. Elasticsearch Kurulumu

```bash
docker run -d -p 9200:9200 -p 9300:9300 -e "discovery.type=single-node" docker.elastic.co/elasticsearch/elasticsearch:7.14.0
```

### 5. Uygulamayı Çalıştırın

```bash
python backend/app.py
```

Arabirimi şu adreste açın: `http://localhost:5000`

## 📁 Proje Yapısı

```
Sigorta-/
├── backend/
│   ├── app.py
│   ├── requirements.txt
│   ├── config.py
│   └── utils/
│       ├── elasticsearch_client.py
│       └── database.py
├── frontend/
│   ├── index.html
│   ├── style.css
│   └── script.js
├── database/
│   ├── schema.sql
│   └── seed_data.sql
├── README.md
├── .env.example
└── .gitignore
```

## 🔧 API Endpoints

```
GET /api/search?q=query&filters=json
GET /api/customers
POST /api/customers
GET /api/customers/<id>
PUT /api/customers/<id>
DELETE /api/customers/<id>
GET /api/insurances
POST /api/insurances
GET /api/insurances/<id>
PUT /api/insurances/<id>
DELETE /api/insurances/<id>
```

## 📧 İletişim

Sorularınız için: kubracuha83-png@github.com
