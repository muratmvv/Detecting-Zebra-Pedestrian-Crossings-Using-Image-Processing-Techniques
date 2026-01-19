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


# English Subtitles

This project aims to detect pedestrian crossings (zebra lines), which are critical for autonomous driving systems and smart city technologies, using traditional image processing algorithms. The project focuses on isolating the pedestrian crossing area from raw camera images and highlighting the lines.

Techniques and Algorithms Used

The project flow consists of specific stages to increase efficiency and reduce computational costs:

Region of Interest (ROI) Determination: Instead of focusing on the entire image, the project focuses on a specific sub-region containing the road surface, reducing computational load and eliminating misleading areas such as the sky.

Sobel Edge Detection: This method calculates density variations (gradients) in the image to reveal the geometric features of horizontal and vertical lines in particular.

Canny Edge Detection: This method uses noise reduction (Gaussian Blur), gradient calculation, and thresholding to obtain the clearest and finest boundaries of pedestrian crossing lines.

Color Space Transformation and Filtering: Gray scale transformation and morphological filtering were performed to enhance the white contrast of zebra stripes.

Application Flow

Image acquisition and grayscale conversion.

Delimitation of the area to be analyzed using ROI masking.

Edge information extraction using Sobel and Canny operators.

Grouping of stripes using Hough Transform (optional, can be specified) or similar geometric methods.

Visualization of the result by overlaying it onto the original image.

Technologies

Python 3.x

OpenCV: Image processing library.

NumPy: Matrix-based calculations.

Matplotlib: Visualization of results and intermediate steps.
