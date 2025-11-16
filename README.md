# SPSS-CDA-Report
# Eğitim Düzeyi, Sosyoekonomik Sınıf ve Yaşam Memnuniyeti Arasındaki İlişkinin Logit Modellerle İncelenmesi

Bu proje, **IST3051 Kategorik Veri Analizi** dersi final ödevi kapsamında, üç kategorik değişken arasındaki ilişkiyi Hiyerarşik Olmayan Test İstatistiği (HOTİ) Logit modelleri kullanarak analiz etmektedir.

Analiz, **SPSS** yazılımı kullanılarak gerçekleştirilmiştir.

---

## 1. Proje Amacı ve Kapsamı

Bu analizin amacı, bireylerin **Eğitim Düzeyi** ve **Sosyoekonomik Sınıfının**, onların **Yaşam Memnuniyeti** üzerindeki etkisini ve bu değişkenler arasındaki karmaşık etkileşimleri istatistiksel modellerle ortaya koymaktır.

## 2. Veri Seti

Analizde kullanılan veri seti (`Veri Seti Final.csv`), 3 kategorik değişkenden ve bu kategorilerin kesişimindeki gözlem sayılarından (Frekans) oluşmaktadır.

### Değişkenler ve Seviyeleri

* **Eğitim Düzeyi (E):**
    * 1: İlkokul
    * 2: Lise
    * 3: Üniversite ve Üzeri
* **Sosyoekonomik Sınıf (S):**
    * 1: Alt Sınıf
    * 2: Orta Sınıf
    * 3: Üst Sınıf
* **Yaşam Memnuniyeti (Y):**
    * Düşük
    * Orta
    * Yüksek
* **Gözlem Sayısı (FREKANS):**
    * Yukarıdaki kategorilerdeki birey sayısı (Ağırlıklandırma için kullanılmıştır).

---

## 3. Metodoloji ve Analiz

Değişkenler arasındaki ilişkileri incelemek için Hiyerarşik Olmayan Test İstatistiği (Logit) modelleri kullanılmıştır. Model uyumunu değerlendirmek için G2 (Likelihood Ratio Chi-Square) ve AIC (Akaike Information Criterion) istatistikleri incelenmiştir.

### Model Sonuçları

Analiz sonucunda, veriye en iyi uyan modelin **tüm ikili etkileşimleri içeren (ES, EY, SY) model** olduğu tespit edilmiştir.

* Bu model, en düşük G2 (0.231) ve en düşük AIC (20.231) değerlerine sahip olarak, veri yapısını en iyi açıklayan ve aynı zamanda en dengeli model olarak seçilmiştir.
* Modelin matematiksel ifadesi: `log(F_ijk) = λ + λ(E)_i + λ(S)_j + λ(Y)_k + λ(ES)_ij + λ(EY)_ik + λ(SY)_jk`

---

## 4. Bulgular ve Yorum: Mozaik Grafik Analizi

Seçilen nihai modelin (ES, EY, SY) mozaik grafiği, değişkenler arasındaki güçlü yapısal ilişkileri net bir şekilde göstermektedir.
<img width="1246" height="736" alt="image" src="https://github.com/user-attachments/assets/72b08104-a43f-42b2-87dd-9e0096cb974b" />



### Grafiğin Yorumlanması

Sadece ana etkileri içeren modellerin (ilk grafik) aksine, ikili etkileşimleri içeren nihai model (ikinci grafik) veriyle çok daha güçlü bir uyum sergilemektedir.

* **Yüksek eğitim** düzeyine sahip bireylerin **üst sınıfta** yer alma ve **yüksek yaşam kalitesine** ulaşma olasılığı belirgin şekilde artmaktadır.
* **İlkokul mezunları** ise **alt sınıf** ve **düşük yaşam kalitesinde** yoğunlaşmaktadır.
* Genel olarak, etkileşimli modeller; eğitim, gelir düzeyi ve yaşam kalitesi arasında kurulan yapısal zinciri net biçimde ortaya koymakta ve modelin açıklayıcılığını ciddi ölçüde artırmaktadır.
