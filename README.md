🚦 YOLOv8 ile Trafik İşaretleri Tespiti (Traffic Sign Detection)

Bu proje, YOLOv8 derin öğrenme modeli kullanılarak trafik işaretlerinin gerçek zamanlı olarak tespit edilmesini amaçlamaktadır. Amaç; otonom sürüş, akıllı ulaşım sistemleri ve sürücü destek uygulamaları için güvenilir bir nesne tespit modeli geliştirmektir.

📌 Projenin Amacı

Trafik işaretlerini görsel veriler üzerinden otomatik olarak tespit etmek

Bilgisayarlı görü (Computer Vision) alanında nesne tespiti (Object Detection) pratiği kazanmak

Gerçek dünya senaryolarında kullanılabilecek bir yapay zeka modeli oluşturmak

🧠 Kullanılan Teknolojiler

Python

YOLOv8 (Ultralytics)

PyTorch

OpenCV

Roboflow (Veri seti yönetimi ve etiketleme)

Ubuntu / Windows

Git & GitHub

📂 Veri Seti

Bu projede kullanılan veri seti, farklı trafik işaretlerini içeren etiketli görsellerden oluşmaktadır.

Format: YOLO (txt label formatı)

Bölümler:

train/ → Eğitim verileri

valid/ → Doğrulama verileri

test/ → Test verileri

Etiketler:

Traffic Light

Stop Sign

Speed Limit

Warning Signs vb.

Veri seti Roboflow üzerinden birleştirilmiş ve YOLO formatına dönüştürülmüştür.

⚙️ Kurulum
git clone https://github.com/jacobtsp/yolov8-trafik-isaretleri.git
cd yolov8-trafik-isaretleri
pip install ultralytics opencv-python

🚀 Model Eğitimi
yolo task=detect mode=train model=yolov8n.pt data=data.yaml epochs=50 imgsz=640

🔍 Test & Tahmin
yolo task=detect mode=predict model=best.pt source=test_images/

📊 Sonuçlar

Model, trafik işaretlerini yüksek doğrulukla tespit edebilmektedir.
Örnek çıktılar:

Gerçek zamanlı kamera görüntüsü üzerinde tespit

Görseller üzerinde bounding box çizimi

Farklı ışık koşullarında başarılı sonuçlar

📈 Hedef doğruluk: %80+
Eğitim sırasında veri artırma (augmentation) ve hiperparametre ayarlamaları yapılmıştır.

🎯 Projeden Kazanımlarım

Bu proje sayesinde:

YOLOv8 mimarisi ile nesne tespiti

Veri seti hazırlama & etiketleme süreci

Model eğitimi, değerlendirme ve iyileştirme

GitHub üzerinde proje dokümantasyonu

Gerçek dünya problemlerine yapay zeka uygulama

konularında ciddi tecrübe kazandım.

🧩 Gelecek Geliştirmeler

 Gerçek zamanlı webcam entegrasyonu

 Modelin mobil (Android) uyarlaması

 Daha büyük ve çeşitli veri seti ile yeniden eğitim

 Farklı YOLOv8 varyantları (s, m, l) ile karşılaştırma

 AR tabanlı trafik işareti gösterimi (gelecek hedef)

