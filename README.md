# Sürücüsüz Metro Simülasyonu (Rota Optimizasyonu)

Bu proje, bir metro ağında iki istasyon arasındaki **en hızlı** ve **en az aktarmalı** rotayı bulan bir simülasyon geliştirmeyi amaçlamaktadır.

## 🎯 Proje Amacı

Bu projede aşağıdaki hedeflere ulaşılması beklenmektedir:

1. Graf veri yapısı kullanarak metro ağını modelleme
2. **BFS (Breadth-First Search)** algoritması ile **en az aktarmalı** rotayı bulma
3. **A* algoritması** ile **en hızlı** rotayı bulma
4. Gerçek dünya problemlerini algoritmik düşünce ile çözme

---

## 💪 Kullanılan Teknolojiler ve Kütüphaneler

Projenin geliştirilmesinde kullanılan temel Python kütüphaneleri:

- **collections**: BFS algoritması için **deque** kullanılarak kuyruk yapısı oluşturuldu.
- **heapq**: A* algoritmasında **öncelik kuyruğu** yapısını sağlamak için kullanıldı.
- **typing**: Kodun okunabilirliğini artırmak için veri tipleri belirtildi.

---

## 🔄 Algoritmaların Çalışma Mantığı

### 1. BFS Algoritması (en az aktarmalı rota)

**BFS (Breadth-First Search)** algoritması, **en kısa yol** ve **en az aktarma** bulmak için kullanılır. Algoritma:
1. **Kuyruk yapısı (deque)** kullanarak başlangıç istasyonundan itibaren genışleyerek ilerler.
2. **Ziyaret edilen istasyonları** takip eder.
3. **Komşu istasyonları** kontrol eder ve kuyrukta ilerletir.
4. Hedef istasyona ulaşıldığında rota döndürülür.

### 2. A* Algoritması (en hızlı rota)

**A* (A-Star)** algoritması, **en hızlı rota** için kullanılır. Algoritma:
1. **Öncelik kuyruğu (heapq)** yapısı kullanarak en kısa süreyi hesaplar.
2. **Her istasyona olan toplam süreyi** hesaba katar.
3. **Ziyaret edilen istasyonları** kayıt altına alarak tekrar ziyaretleri önler.
4. Hedef istasyona en kısa sürede ulaşan yolu döndürür.

---

## 🎨 Örnek Kullanım ve Test Sonuçları

Kod çalıştırıldığında aşağıdaki gibi test senaryoları uygulanabilir:

### Senaryo 1: **AŞTİ → OSB**
```bash
python SultanBulut_MetroSimulation.py
```
**Çıktı:**
```
1. AŞTİ'den OSB'ye:
En az aktarmalı rota: AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
En hızlı rota (25 dakika): AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
```

### Senaryo 2: **Batıkent → Keçiören**
```
2. Batıkent'ten Keçiören'e:
En az aktarmalı rota: Batıkent -> Demetevler -> Gar -> Keçiören
En hızlı rota (21 dakika): Batıkent -> Demetevler -> Gar -> Keçiören
```

---

## 💡 Projeyi Geliştirme Fikirleri

- **Metro hattının görselleştirilmesi** (Matplotlib, NetworkX vb. ile graf görseli eklemek)
- **Dinamik metro hatları ekleyerek** gerçek dünya simülasyonları yapmak
- **Gerçek zamanlı trafik yoğunluğu** ve bekleme sürelerini modele dahil etmek
- **Mobil veya web uygulama entegrasyonu** ile interaktif küllanım sağlamak
