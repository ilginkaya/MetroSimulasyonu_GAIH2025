
# 🚇 Metro Simülasyonu - GAIH Mart 2025 Projesi

Bu proje, Python programlama dili kullanılarak Ankara metrosuna benzer bir metro ağında iki istasyon arasında en hızlı rotayı bulmak ve bunu görselleştirmek amacıyla geliştirilmiştir. Kullanıcıdan alınan başlangıç ve hedef istasyonlara göre hem algoritmik çözüm hem de grafiksel harita sunar.

---

## 🔧 Kullanılan Teknolojiler ve Kütüphaneler

| Kütüphane | Açıklama |
|----------|----------|
| `heapq` | Öncelikli kuyruk yapısı (A* algoritması için) |
| `collections` | `deque` ile verimli kuyruk işlemleri (BFS için) |
| `typing` | Tip güvenliği ve anlaşılır fonksiyon imzaları |
| `colorama` | Terminal çıktısına renk katmak için |
| `matplotlib` | Grafiksel metro haritası çizimi |
| `networkx` | Metro ağı graf modellemesi ve görselleştirme |

---

## 🧠 Kullanılan Algoritmalar ve Çalışma Mantığı

### 🔄 BFS (Breadth-First Search)
- Amaç: **En az aktarma ile rotayı bulmak** (Kodda tanımlı ama örnekler A* kullanıyor)
- Genişlik öncelikli arama yaparak önce en kısa geçiş sayısına sahip yolları dener.
- Her istasyon komşularıyla sırayla ziyaret edilir.
- Kuyruk (deque) yapısı kullanılır.

### ⭐ A* (A Star Search)
- Amaç: **En hızlı (en kısa sürede tamamlanan) rotayı bulmak**
- `heapq` ile en düşük maliyetli yol her seferinde öncelikli olarak seçilir.
- Her istasyon için toplam geçen süre hesaplanarak yol bulunur.
- Bu projede heuristic (tahmini mesafe) eklenmediği için Dijkstra eşleniği gibi çalışır.

### ❓ Neden Bu Algoritmalar?
- **BFS**: Aktarma sayısını en aza indirerek karmaşık hatlarda basit yol bulur.
- **A***: Gerçek zamanlı mesafe veya süre ile en kısa yol için idealdir.

---

## ▶️ Örnek Kullanım

```bash
python3 MetroSimulation_Interactive.py

=== Metro Simülasyonu Başladı ===

İstasyon ID'leri: K1, K2, ..., T4
Başlangıç istasyon ID'si: M1
Hedef istasyon ID'si: K4
```

#### ✅ Çıktı:

```bash
En hızlı rota (19 km):
AŞTİ -> Kızılay -> Ulus -> Demetevler -> OSB
```

🔍 Aynı zamanda `matplotlib` ile çizilmiş metro haritası grafik penceresi olarak açılır.

---

## 💡 Geliştirme Fikirleri

- [ ] Terminal üzerinden aktarma sayısını da göster
- [ ] BFS algoritması da aktif test edilsin
- [ ] Daha fazla istasyon ve hat eklensin (dış hatlar, ring hatları)
- [ ] HTML/Flask arayüzü ile web uygulamasına dönüştürülebilir
- [ ] Rota süresine tahmini yolcu yoğunluğu etkisi dahil edilebilir

---

## 👤 Geliştirici

> Bu proje [Global AI Hub](https://globalaihub.com) Python Bootcamp Mart 2025 kapsamında **İlginkaya** tarafından gerçekleştirilmiştir.

---

🧠 Keyifli Kodlamalar!
