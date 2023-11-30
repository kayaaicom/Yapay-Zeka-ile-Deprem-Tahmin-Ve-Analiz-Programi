<h1>Yapay Zeka İle Deprem Tahmin Ve Analiz Programı</h1>

<h2>Deprem Tahmini Projesi</h2>

Bu proje buraya basit mantığı ile kodlanmış şekilde yüklenip, [Kaya AI](https://kaya-ai.com/) tarafından arkaplanda en uç noktaya kadar geliştirilmektedir. <br><br>Genel olarak Python kullanılarak geliştirilmiş bir Deprem Tahmini sistemidir. Ana amaç, Türkiye'nin son bir aylık deprem verilerini toplayarak, bu verileri işleyip LSTM (Long Short-Term Memory) ağları kullanarak gelecekteki depremlerin büyüklüklerini tahmin etmektir.

<b>Özellikler</b>

AFAD'ın API'sinden gerçek zamanlı deprem verilerini çeker.<br>
Deprem verileri son 30 güne ait verilerdir.(tarafınızca değiştirilebilir.)<br>
Deprem verilerini işler ve LSTM modeli için uygun hale getirir.<br>
LSTM ağı kullanarak deprem büyüklüklerini tahmin eder.<br>
Gelecekteki deprem büyüklüklerini tahmin eder ve görselleştirir.<br>

<h3>Dosyalar</h3>

    deprem.py: API'den veri çekme, veri işleme, model eğitimi ve temel tahminlerin yapıldığı ana betik.
    extra.py: Eğitilmiş modeli yükleyerek gelecekteki deprem büyüklüklerini tahmin eden ve görselleştiren yardımcı betik.

<h3>Kurulum</h3>
Projeyi kullanabilmek için gerekli kütüphaneleri yüklemek gereklidir:

    pip install numpy pandas matplotlib torch requests
    
<h3>Kullanım</h3>

Öncelikle, deprem.py betiğini çalıştırarak veri çekme, işleme ve model eğitimi işlemlerini gerçekleştirin:
    python deprem.py

Model eğitildikten ve kaydedildikten sonra, extra.py betiğini çalıştırarak gelecekteki deprem büyüklüklerinin tahminlerini görüntüleyin (ancak ilk açılan grafiği kapatınca otomatik olarak extra.py çalıştırılmaktadır, manuel çalıştırmanıza gerek kalmamaktadır.):
    python extra.py


Bu projede kullanılan yapay zeka, Long Short-Term Memory (LSTM) ağlarıdır. LSTM'ler, özellikle zaman serisi verileriyle çalışırken etkili olan ve hafıza yeteneklerine sahip olan özel bir tür Yapay Sinir Ağıdır (Artificial Neural Network - ANN). LSTM'ler, geleneksel feedforward sinir ağlarından farklı olarak, bilgiyi uzun süreler boyunca saklayabilme ve geçmiş bilgilere dayanarak kararlar alabilme yeteneğine sahiptirler.

LSTM'in Temel Yapısı ve Matematiksel Formülleri
LSTM hücresinin ana bileşenleri üç kapıdan (gate) oluşur: giriş kapısı, unutma kapısı ve çıkış kapısı. Bu kapılar, hücrenin bilgi akışını düzenler. Her bir kapı, bir aktivasyon fonksiyonu ve bir noktasal çarpım işlemi içerir. Ayrıca, LSTM hücresi bir hücre durumu (C_t) ve bir gizli durum (h_t) içerir.

Detaylı bir şekilde incelemek için LSTM: https://en.wikipedia.org/wiki/Long_short-term_memory
    
<b>Katkıda Bulunma</b><br>
Bu proje, açık kaynaklıdır ve katkılara açıktır. İyileştirmeler, hata düzeltmeleri veya yeni özellikler eklemek için pull request'ler gönderebilirsiniz.
