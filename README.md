# Etkileşim Sözlüğü · BYK LAB

UI/UX etkileşimlerinin ortak dilini kurmak için yapılmış tek sayfalık referans.
Amaç: "akordeon gibi açılsın" ya da "yeni ekran açılıyormuş gibi kutu çıksın"
dendiğinde herkesin aynı şeyi anlaması.

**Canlı:** https://byk-etkilesim-sozlugu-furkan-geless-projects.vercel.app

## Ne var içinde

Her etkileşim için bir kart:

- Türkçe + İngilizce adı (terim karışıklığını bitirmek için)
- Canlı, dokunulabilir demo
- "Nasıl hissettirir" etiketi
- Kopyalanabilir kod — varsayılan olarak **gizli**, "Kodu göster" ile akordeon gibi açılır

### Kategoriler

| Kategori | Etkileşimler |
|---|---|
| Açılır / Genişleyen | Akordeon |
| Üst Katman (Overlay) | Modal / Diyalog, Alt Sayfa (Bottom Sheet), Yan Panel (Drawer), İpucu Balonu (Tooltip), Açılır Menü (Dropdown) |
| Bildirim & Durum | Toast, Rozet (Badge), İskelet Yükleyici (Skeleton), Dönen Yükleyici (Spinner), İlerleme Çubuğu |
| Gezinme & Seçim | Sekmeler (Tabs), Segment Kontrol, Anahtar (Switch), Adım Göstergesi (Stepper), Yüzen Buton (FAB) |
| İçerik | Kaydırıcı (Carousel), Aşağı Çekip Yenileme, Sonsuz Kaydırma |

Ayrıca **İkonlar** sekmesinde tüm [Lucide](https://lucide.dev/icons) ikon seti
aranabilir halde; bir ikona tıklayınca kullanım kodu kopyalanır.

## Teknik

Tek dosya: `index.html`. Bağımlılık yok, build yok.
Lucide ikonları CDN'den yüklenir. Dark/light tema, mobil öncelikli.

Yeni etkileşim eklemek için `index.html` içindeki `DATA` dizisine bir obje ekle:

```js
{
  cat: "Kategori", tr: "Türkçe ad", en: "English name",
  desc: "Ne yaptığı",
  feel: "Nasıl hissettirdiği",
  demo: `<!-- canlı demo HTML -->`,
  init: (r) => { /* demoyu çalıştıran JS */ },
  code: `<!-- kartta gösterilecek örnek kod -->`
}
```
