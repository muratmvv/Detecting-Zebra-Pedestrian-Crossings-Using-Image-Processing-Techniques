# Görüntü İşleme Teknikleri ile Zebra Yaya Geçidi Tespiti
Bu proje, otonom sürüş sistemleri ve akıllı şehir teknolojileri için kritik öneme sahip olan yaya geçidi (zebra çizgileri) tespitini, geleneksel görüntü işleme algoritmaları kullanarak gerçekleştirmeyi amaçlar. Proje kapsamında, ham kamera görüntülerinden yaya geçidi bölgesinin ayrıştırılması ve çizgilerin belirginleştirilmesi hedeflenmiştir.

Kullanılan Teknikler ve Algoritmalar

Proje akışı, verimliliği artırmak ve hesaplama maliyetini düşürmek amacıyla belirli aşamalardan oluşmaktadır:

Region of Interest (ROI) Belirleme: Görüntünün tamamı yerine, yol yüzeyinin bulunduğu spesifik alt bölgeye odaklanılarak işlem yükü azaltılmış ve gökyüzü gibi yanıltıcı alanlar elenmiştir.

Sobel Kenar Algılama: Görüntüdeki yoğunluk değişimlerini (gradyanlarını) hesaplayarak özellikle yatay ve dikey çizgilerin geometrik özelliklerini ortaya çıkarmak için kullanılmıştır.

Canny Kenar Tespiti: Gürültü azaltma (Gaussian Blur), gradyan hesaplama ve eşikleme (thresholding) adımlarıyla yaya geçidi çizgilerinin en net ve ince sınırlarını elde etmek için uygulanmıştır.

Renk Alanı Dönüşümü ve Filtreleme: Zebra çizgilerinin beyaz kontrastını belirginleştirmek için Gray Scale (Gri Seviye) dönüşümü ve morfolojik filtreleme işlemleri yapılmıştır.

Uygulama Akışı

Görüntünün alınması ve gri tonlamaya çevrilmesi.

ROI maskeleme ile analiz edilecek bölgenin sınırlandırılması.

Sobel ve Canny operatörleri ile kenar bilgilerinin çıkarılması.

Hough Transform (opsiyonel ise belirtilebilir) veya benzeri geometrik yöntemlerle çizgilerin gruplandırılması.

Sonucun orijinal görüntü üzerine bindirilerek görselleştirilmesi.

Teknolojiler

Python 3.x

OpenCV: Görüntü işleme kütüphanesi.

NumPy: Matris tabanlı hesaplamalar.

Matplotlib: Sonuçların ve ara aşamaların görselleştirilmesi.
