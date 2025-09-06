# Pusula Academy - Data Science Intern Case Study

**Ad Soyad:** Mehmet Ali Aydoğar  
**Email:** mehmetaliaydogar@gmail.com

---

## 1. Proje Özeti
Bu proje, fiziksel tıp ve rehabilitasyon verisi üzerinde **EDA (Exploratory Data Analysis)** ve basit **veri ön işleme** adımlarını içermektedir.  
Veri seti **2235 gözlem ve 13 özellik** içermekte olup, hedef değişkenimiz **TedaviSuresi**’dir.  

Projenin amacı, veriyi **modellemeye hazır hale getirmek** ve veri yapısını anlamaktır. Model inşa edilmesi zorunlu değildir.

---

## 2. Veri Seti

| Değişken | Açıklama |
|-----------|----------|
| HastaNo | Anonimleştirilmiş hasta ID |
| Yas | Yaş |
| Cinsiyet | Cinsiyet |
| KanGrubu | Kan grubu |
| Uyruk | Uyruk |
| KronikHastalik | Kronik hastalıklar (virgülle ayrılmış) |
| Bolum | Bölüm/Klinik |
| Alerji | Alerjiler |
| Tanilar | Tanılar |
| TedaviAdi | Tedavi adı |
| TedaviSuresi | Tedavi süresi (hedef değişken, seans sayısı) |
| UygulamaYerleri | Uygulama yerleri |
| UygulamaSuresi | Uygulama süresi |

---

## 3. EDA (Exploratory Data Analysis)
- Veri boyutu ve tipleri incelendi.
- Eksik veriler tespit edildi ve bazıları dolduruldu (`Cinsiyet`, `Alerji`, `KanGrubu` vb.).
- Sayısal değişkenlerin dağılımları görselleştirildi (histogram, KDE).
- Kategorik değişkenlerin dağılımları görselleştirildi (barplot).
- Korelasyon matrisi oluşturuldu (`Yas`, `TedaviSuresi_Num`, `UygulamaSuresi_Num`).
- Kronik hastalıklar, tanılar, tedavi adları ve bölümlere göre frekans analizi yapıldı.

---

## 4. Basit Veri Ön İşleme
- Aynı hastanın birden fazla kaydı **HastaNo** bazında tekilleştirildi.
- Hedef değişken (`TedaviSuresi_Num`) ve sayısal özellikler için eksik değerler dolduruldu ve scale edildi.
- Kategorik değişkenler için eksik değerler mod ile dolduruldu ve **One-Hot Encoding** uygulandı.
- Eğitim ve test verisi %80-%20 oranında ayrıldı.
- Pipeline ile veri işleme adımları modüler hale getirildi.

---

## 5. Kullanılan Kütüphaneler
- `pandas`, `numpy` → Veri işleme
- `matplotlib`, `seaborn` → Görselleştirme
- `sklearn` → Ön işleme ve pipeline
- `missingno` → Eksik veri görselleştirme
