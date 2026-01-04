# CIFAR Sınıflandırması
Bu egzersiz, 10 farklı kategoriden görüntüler içeren ***CIFAR-10 veri kümesini*** keşfederek CNN becerilerinizi güçlendirecektir. Ayrıca, bir modelin performansını artırmaya yardımcı olabilecek veri artırma tekniklerini öğreneceksiniz.

## 🚨 Bu notebook'u Google Colab'da açın 🚨
- ❗️ Kullanmak için bir Google hesabına giriş yapmanız gerekecek
- [https://colab.research.google.com/](https://colab.research.google.com/) adresine gidin
- `cifar_classification.ipynb` dosyasını yüklemeyi seçin.
 <img src='' width=300>
- Bu, Google Drive'ınızda `Colab Notebooks` adlı bir klasörde saklanan notebook'unuzun bir kopyasını oluşturacaktır
- Ardından, **çalışma zamanı türünü GPU olarak değiştirin ("Runtime --> Change runtime --> GPU")**


## Neden Colab?
Oldukça küçük görüntüler ve standart mimariler bile çok uzun hesaplama sürelerine yol açar. Bunun nedeni, varsayılan olarak sinir ağlarının CPU'nuzda çalıştırılmasıdır. Ancak GPU'lar büyük işlemleri paralel olarak hesaplayabilir, bu da bizim ilgilendiğimiz konudur çünkü her grup içinde, teorik olarak tüm görüntülerin dönüşümünü paralel olarak hesaplamak mümkündür (aslında, geri yayılım tüm görüntülerde aynı anda yapılmalıdır, bu yüzden burada gerçek bir paralelleştirme yoktur). Google'ın GPU'ları sayesinde CNN modellerinin yakınsamasını hızlandırmak için Google Colab kullanalım.

## Google Colab Nedir?
Google Colab, Google'ın GPU'larını kullanma imkanıyla çevrimiçi notebook'lara sahip olmanın bir yolundan başka bir şey değildir. Buradaki fikir, üretimde kullanmak değil (bazı sınırlamalar olduğu için) ancak yeni algoritmaları test etmek ve prototiplemek için Google Colab'ı kullanmaktır. GPU'lara bu ücretsiz erişim, hesaplama süresini hızlandırmanızı sağlar.

