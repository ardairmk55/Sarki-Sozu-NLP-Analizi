# 🎵 Şarkı Sözü NLP Analizi ve Word2Vec Model Karşılaştırması

## 📖 Proje Hakkında

Bu proje, Türkçe şarkı sözleri üzerinde Doğal Dil İşleme (NLP) teknikleri kullanılarak gerçekleştirilen bir Word2Vec model karşılaştırma çalışmasıdır.

Çalışmada ham şarkı sözü verileri üzerinde ön işleme adımları uygulanmış, farklı Word2Vec modelleri eğitilmiş ve elde edilen sonuçlar Cosine Similarity, Anlamsal Değerlendirme ve Jaccard Benzerlik Analizi yöntemleri ile karşılaştırılmıştır.

---

# 🎯 Ödev Amacı

Bu çalışmanın amacı:

* Türkçe şarkı sözlerinden vektör temsilleri üretmek
* Farklı Word2Vec yapılandırmalarını karşılaştırmak
* Benzer şarkı sözlerini tespit etmek
* Model parametrelerinin başarıya etkisini incelemek
* Cosine Similarity ile nesnel değerlendirme yapmak
* İnsan değerlendirmesi ile anlamsal başarıyı ölçmek
* Modeller arası sıralama tutarlılığını analiz etmektir

---

# 📂 Repository İçeriği

```text
Sarki-Sozu-NLP-Analizi/
│
├── NLP_%25/
│
├── NLP_HAM_VERI.xls
│
├── formatli_lemmatized.xls
│
├── formatli_stemmed.xls
│
├── Manuel_Puanlama_Asistani_TR.xls
│
├── heatmap.png
│
├── sarki_sozu_isleme_arda_irmak_final.ipynb
│
└── README.md
```

---

# 📊 Veri Setleri

## NLP_HAM_VERI.xls

Ön işleme uygulanmamış ham şarkı sözü verilerini içermektedir.

### İçerik

* Şarkı sözleri
* Sanatçı bilgileri
* Metin içerikleri

---

## formatli_stemmed.xls

Stemleme işlemi uygulanmış veri setidir.

Örnek:

```text
seviyorum → sev
gidiyorum → git
```

---

## formatli_lemmatized.xls

Lemmatization işlemi uygulanmış veri setidir.

Örnek:

```text
gidiyorum → gitmek
seviyorum → sevmek
```

---

## Manuel_Puanlama_Asistani_TR.xls

Anlamsal değerlendirme aşamasında kullanılan manuel puanlama tablosudur.

Bu dosya:

* İnsan değerlendirmesi
* Anlamsal benzerlik puanları
* Ortalama skor hesaplamaları

için kullanılmıştır.

---

# 🧠 Kullanılan NLP Teknikleri

## Veri Ön İşleme

* Küçük harfe dönüştürme
* Noktalama temizliği
* Sayı temizliği
* Özel karakter temizliği
* Stopword temizliği

## Metin İşleme

* Tokenization
* Stemming
* Lemmatization

## Word Embedding

* Word2Vec CBOW
* Word2Vec SkipGram

---

# 🎯 Eğitilen Modeller

Bu çalışmada toplam 16 farklı Word2Vec modeli eğitilmiştir.

Kullanılan parametreler:

### Mimari

* CBOW
* SkipGram

### Window Size

* 3
* 5
* 7
* 10

### Vector Size

* 100
* 200
* 300

---

# 📈 Değerlendirme Yöntemleri

## 1️⃣ Cosine Similarity

Her model için giriş metnine en benzer ilk 5 metin bulunmuştur.

### Ölçülenler

* Top-5 sonuçlar
* Benzerlik skorları
* Ortalama cosine değeri

---

## 2️⃣ Anlamsal Değerlendirme

İnsan tarafından gerçekleştirilen değerlendirme.

Puanlama:

| Puan | Açıklama             |
| ---- | -------------------- |
| 1    | Çok alakasız         |
| 2    | Kısmen ilgili        |
| 3    | Orta düzey           |
| 4    | Güçlü benzerlik      |
| 5    | Çok yüksek benzerlik |

---

## 3️⃣ Jaccard Benzerlik Analizi

Modellerin ürettiği ilk 5 sonuç listeleri karşılaştırılmıştır.

Formül:

J(A,B) = |A∩B| / |A∪B|

Bu analiz sayesinde:

* Birbirine en yakın modeller
* En farklı modeller
* En tutarlı sonuç üreten modeller

belirlenmiştir.

---

# 🌡️ Heatmap

Jaccard benzerlik matrisi kullanılarak oluşturulan heatmap aşağıda yer almaktadır.

```text
heatmap.png
```

Bu görsel modeller arasındaki benzerlik ilişkilerini göstermektedir.

---

# 📓 Notebook

Tüm çalışma aşağıdaki notebook içerisinde yer almaktadır:

```text
sarki_sozu_isleme_arda_irmak_final.ipynb
```

Notebook içerisinde:

* Veri temizleme
* Word2Vec eğitimi
* Cosine Similarity hesaplamaları
* Jaccard hesaplamaları
* Heatmap üretimi
* Sonuç analizleri

yer almaktadır.

---

# 🚀 Çalıştırma

Gerekli kütüphaneleri yükleyin:

```bash
pip install pandas numpy gensim scikit-learn matplotlib seaborn nltk
```

Jupyter Notebook'u açın:

```bash
jupyter notebook
```

Notebook'u çalıştırın:

```bash
sarki_sozu_isleme_arda_irmak_final.ipynb
```

---

# 📊 Üretilen Çıktılar

* Cosine Similarity Sonuçları
* Top-5 Benzer Metin Listeleri
* Ortalama Benzerlik Skorları
* Anlamsal Değerlendirme Sonuçları
* Jaccard Matrisi
* Heatmap Görseli

---

# 👨‍💻 Geliştirici

## Arda Irmak

🎓 Gümüşhane Üniversitesi - Bilgisayar Programcılığı

💻 Full Stack Developer

🚀 Founder of CodePort

🌐 NLP • AI • Web Development

GitHub:
https://github.com/ardairmk55

---

# ⭐ Destek

Projeyi faydalı bulduysanız:

⭐ Star vermeyi unutmayın

🍴 Fork oluşturabilirsiniz

📝 Geri bildirim paylaşabilirsiniz

---

## 🎵 Türkçe Şarkı Sözleri Üzerinde NLP ve Word2Vec Analizi

Made with ❤️ by Arda Irmak
