# Abdüssamet Kebeli - Game Developer Portfolio

Bu proje, oyun geliştirme portfolyosunu sergilemek amacıyla **Astro** ve **Tailwind CSS** kullanılarak geliştirilmiş tamamen statik bir web sitesidir.

## Özellikler
- **Statik Site Üretimi (SSG)**: Sunucu tarafı render işlememesi gerektirmez. Güvenli ve hızlıdır.
- **Premium Karanlık Tema**: Özel renk paleti ve modern tipografi (Inter).
- **Video Entegrasyonu**: Proje detaylarında farklı çözünürlükleri destekleyen (16:9 PC, 9:16 Mobil) performansı artırılmış, otomatik başlamayan `playsinline` özellikli HTML5 video entegrasyonu.
- **Lighthouse Odaklı Performans**: Minimum JS, CSS animasyonları, ve gecikmeli yükleme optimizasyonları sayesinde 90+ performans skoru elde edilecek şekilde kodlanmıştır.

## Gereksinimler
- Node.js (v18 veya üstü önerilir)

## Kurulum ve Çalıştırma (Local)

1. Proje dizinine terminalde gidin.
2. Bağımlılıkları yükleyin:
   ```bash
   npm install
   ```
3. Geliştirme sunucusunu başlatın:
   ```bash
   npm run dev
   ```
4. Tarayıcınızdan `http://localhost:4321` adresine gidin.

## Build Alma (Üretim)

Sitennizi yayına hazırlamak için üretim (production) sürümünü oluşturmanız gerekir.

```bash
npm run build
```

Bu komut projeyi derler ve çıktı dosyalarını **`dist/`** klasörüne yerleştirir. `dist/` klasörü içerisindeki dosyalar, herhangi bir sunucu gereksinimi olmayan, tamamen statik HTML, CSS, JS ve medya dosyalarından oluşur.

Üretim öncesi son hali yerel olarak test etmek isterseniz şu komutu kullanabilirsiniz (Lighthouse testleri için bu komutu kullanın):

```bash
npm run preview
```

## JSON Veri Yapısı (`src/data/projects.json`)
Portfolyoda yer alan projelerinizi düzenlemek veya yenilerini eklemek için `src/data/projects.json` dosyasını kullanabilirsiniz. Özellikle video boyutuna göre (PC için 16:9, Mobil için 9:16) `aspectRatio` ayarını doğru girmeye dikkat edin.

## Deploy (Netlify / Vercel / GitHub Pages)

Proje statik olduğu için herhangi bir statik site barındırma servisine (hosting) dakikalar içinde yüklenebilir.

### Netlify Üzerinden Deploy
1. Netlify'a GitHub veya GitLab hesabınızla giriş yapın.
2. "Add new site" butonundan "Import an existing project" seçeneğini seçin.
3. Proje reponuzu bağlayın.
4. **Build command:** `npm run build`
5. **Publish directory:** `dist/`
6. "Deploy site" butonuna tıklayın.

### Vercel Üzerinden Deploy
1. Vercel paneline giriş yapın ve Git deponuzu bağlayın.
2. Projeyi içeri aktarırken Vercel otomatik olarak `Astro` projesi olduğunu algılayacaktır.
3. Ayarları varsayılan halindeyken onaylayıp "Deploy" butonuna basın.

### GitHub Pages
GitHub Pages ile yayınlarken `astro.config.mjs` içerisinde `site` ayarını deponuzun URL'si olarak tanımlamanız ve ilgili GitHub Actions workflow dosyasını eklemeniz gerekebilir. Astro'nun resmi [GitHub Pages deploy rehberi](https://docs.astro.build/en/guides/deploy/github/) size detayları sağlayacaktır.
