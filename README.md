# 🎵 Türkçe Şarkı Sözleri: Metin Madenciliği ve NLP Analizi

Bu proje, Metin Madenciliği ve Doğal Dil İşleme (NLP) süreçlerinin gerçek dünya verileri üzerinde nasıl uygulanacağını göstermek amacıyla geliştirilmiştir. Proje kapsamında popüler Türkçe şarkı sözlerinden oluşan özel bir veri seti oluşturulmuş, dilin istatistiksel yapısı (Zipf Yasası) incelenmiş ve veriler makine öğrenmesi modellerine uygun hale getirilmek üzere kapsamlı bir ön işleme (pre-processing) boru hattından (pipeline) geçirilmiştir.

## 🎯 Projenin Amacı ve Kapsamı
1. **İstatistiksel Dil Analizi:** Ham metin verileri üzerinde frekans analizi yapılarak dildeki kelime dağılımlarının Zipf Yasası'na (Log-Log grafiği) uygunluğunun kanıtlanması.
2. **Kapsamlı Ön İşleme:** Gürültülü metin verisinin NLP standartlarına uygun olarak temizlenmesi ve yapılandırılması.
3. **Model Hazırlığı:** İleriki vektörizasyon ve sınıflandırma modellerinde (örneğin duygu analizi veya şarkı öneri sistemleri) kullanılmak üzere temiz `CSV` çıktılarının üretilmesi.

## 🛠️ Kullanılan Teknolojiler ve Kütüphaneler
* **Python 3.x**
* **Veri Manipülasyonu:** `pandas`, `numpy`
* **Görselleştirme:** `matplotlib`
* **Doğal Dil İşleme (NLP):** `nltk` (Natural Language Toolkit), `TurkishStemmer`, `re` (Regex)

## ⚙️ Uygulanan NLP Ön İşleme Adımları
Veri seti üzerinde hiyerarşik olarak aşağıdaki metin madenciliği adımları uygulanmıştır:
1. **Genel Temizlik:** HTML etiketlerinin, sayıların ve noktalama işaretlerinin (cümle sonları hariç) temizlenmesi.
2. **Lowercasing:** Case-sensitivity sorunlarını çözmek için tüm metnin küçük harfe dönüştürülmesi.
3. **Tokenization (Parçalama):** Metnin cümle ve kelime bazlı anlamlı yapı taşlarına (`token`) ayrılması.
4. **Stop Word Removal (Durak Kelimelerin Silinmesi):** Modelde gürültü yaratabilecek, anlamsal değeri düşük bağlaç ve edatların (*ve, ama, de, da*) temizlenmesi.
5. **Lemmatization & Stemming:**
   * *Lemmatization:* Kelimelerin sözlük köklerine indirgenmesi (`WordNetLemmatizer`).
   * *Stemming:* Kelimelerin formolojik eklerinden arındırılarak yapısal gövdelerine inilmesi (`TurkishStemmer`).

## 📁 Depo (Repository) İçeriği
Bu repo, sürecin tüm kodlarını ve işlem aşamalarında üretilen veri setlerini içermektedir:
* `sarki_sozu_isleme.ipynb`: Veri çekimi, Zipf yasası görselleştirmeleri ve tüm NLP ön işleme adımlarının adım adım ("Önce/Sonra" tablolarıyla) raporlandığı ana Jupyter Notebook dosyası.
* `ham_veri_seti.csv`: 55 popüler şarkıdan oluşan, işlem görmemiş orijinal veri seti.
* `lemmatized_veri_seti.csv`: Tüm temizlik aşamalarından geçtikten sonra Lemmatization uygulanmış modellemeye hazır veri seti.
* `stemmed_veri_seti.csv`: Tüm temizlik aşamalarından geçtikten sonra Stemming uygulanmış modellemeye hazır veri seti.

## 👨‍💻 Geliştirici
**Arda Irmak**  
*Gümüşhane Üniversitesi - Bilgisayar Programcılığı*
