# Savaşan İHA - Otonom Kilitlenme ve Kamikaze Kontrol Yazılımı

> [!IMPORTANT]
> ## 🔒 Takım Gizliliği ve Kaynak Kod Politikası
>
> Bu proje, takımımıza ve proje ortaklarımıza ait özel bilgi, yöntem ve uygulamaları içermektedir. **Takım gizliliğini, fikrî emeği ve proje güvenliğini korumak amacıyla kaynak kodlar bu depoda paylaşılmamaktadır.**
>
> Bu README; projenin amacı, mimarisi ve kullanılan teknolojiler hakkında genel bir bakış sunar. Kodun tamamı ve ayrıntılı uygulama bileşenleri yalnızca yetkili takım üyelerinin erişimine açıktır.
>
> 📩 Proje hakkında daha fazla bilgi için depo sahibiyle iletişime geçebilirsiniz.

## 📝 Proje Özeti
Rakip İHA'ları havada tespit edip kilitlenme (lock-on) sağlayan ve yer hedeflerine yönelik otonom kamikaze görevlerini yöneten görüntü işleme tabanlı bir sistemdir. TEKNOFEST Savaşan İHA yarışması isterlerine göre optimize edilmiştir.

## ✨ Özellikler
* **Otonom Kilitlenme:** Rakip İHA'ları YOLO tabanlı modellerle tespit edip 4 saniye boyunca kilitli kalma.
* **QR Kod İşleme:** Yer hedeflerindeki QR kodlarını otonom olarak okuma, veriyi işleme ve sunucuya aktarma.
* **HSS Kaçınma:** Hava Savunma Sistemi (HSS) koordinatlarını sunucudan alarak yasaklı bölgelerden otonom kaçınma.
* **Gerçek Zamanlı Veri Aktarımı:** Görüntü ve telemetri verilerinin socket protokolü ile yer istasyonuna iletilmesi.

## 🛠 Kullanılan Teknolojiler
* **Görüntü İşleme:** OpenCV, YOLOv5/v8, KCF Tracker, PyZbar (QR).
* **Yazılım:** Python (Multithreading, Socket, Requests), CUDA (GPU hızlandırma).
* **Donanım:** NVIDIA Jetson Nano/NX, Raspberry Pi 4.

## 🏗 Proje Yapısı ve Mimarisi
* **Algılama Hattı:** Kamera verilerinin HSV maskeleme ve YOLO ile işlenerek nesne merkez koordinatlarının bulunması
