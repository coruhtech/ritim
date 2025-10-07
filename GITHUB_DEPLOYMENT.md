# 🚀 GitHub Pages'e Yayınlama Rehberi

Bu rehber, MUDEK Değerlendirme Sistemini GitHub Pages'de yayınlamak için gerekli adımları içerir.

## 📋 Ön Hazırlık

✅ **Tamamlanan İşlemler:**
- README.md dosyası temizlendi (gizli bilgiler kaldırıldı)
- _config.yml dosyası oluşturuldu (Jekyll yapılandırması)
- .github/workflows/deploy.yml dosyası oluşturuldu (otomatik deployment)
- .gitignore dosyası güncellendi
- Tüm dosyalar git'e eklendi ve commit edildi

## 🔧 GitHub'da Repository Oluşturma

### Adım 1: GitHub'da Yeni Repository Oluşturun

1. [GitHub.com](https://github.com) adresine gidin
2. Sağ üst köşede **"+"** butonuna tıklayın ve **"New repository"** seçin
3. Repository bilgilerini girin:
   - **Repository name:** `mudek-degerlendirme` (veya istediğiniz bir isim)
   - **Description:** `MUDEK Ders Değerlendirme ve Analiz Sistemi`
   - **Public** seçeneğini işaretleyin (GitHub Pages için gerekli)
   - **"Create repository"** butonuna tıklayın

### Adım 2: Local Repository'yi GitHub'a Bağlayın

Terminal/PowerShell'de aşağıdaki komutları çalıştırın:

```bash
# GitHub repository'nizi ekleyin (YOUR_USERNAME'i kendi GitHub kullanıcı adınızla değiştirin)
git remote add origin https://github.com/YOUR_USERNAME/mudek-degerlendirme.git

# Branch'i main olarak ayarlayın
git branch -M main

# Kodları GitHub'a gönderin
git push -u origin main
```

## 🌐 GitHub Pages'i Etkinleştirme

### Otomatik Yöntem (Önerilen)

1. GitHub repository sayfanıza gidin
2. **Settings** sekmesine tıklayın
3. Sol menüden **Pages** bölümünü bulun
4. **Source** kısmında:
   - **GitHub Actions** seçeneğini seçin
5. Değişiklikler otomatik olarak kaydedilecektir

### Manuel Yöntem (Alternatif)

Eğer GitHub Actions kullanmak istemezseniz:

1. **Settings** → **Pages** sayfasına gidin
2. **Source** kısmında:
   - **Deploy from a branch** seçeneğini seçin
   - **Branch:** `main` seçin
   - **Folder:** `/ (root)` seçin
3. **Save** butonuna tıklayın

## ✅ Deployment Kontrolü

### GitHub Actions ile Deployment (Önerilen)

1. Repository'nizde **Actions** sekmesine gidin
2. **"Deploy to GitHub Pages"** workflow'unun çalıştığını görmelisiniz
3. Yeşil tik ✅ görünce deployment tamamlanmıştır

### Site Erişimi

Deployment tamamlandıktan sonra sitenize şu adresten erişebilirsiniz:

```
https://YOUR_USERNAME.github.io/mudek-degerlendirme/
```

(YOUR_USERNAME'i kendi GitHub kullanıcı adınızla değiştirin)

## 🔄 Güncellemeler

Kodda değişiklik yaptığınızda:

```bash
# Değişiklikleri ekleyin
git add .

# Commit yapın
git commit -m "Açıklama mesajı"

# GitHub'a gönderin
git push
```

GitHub Actions otomatik olarak sitenizi güncelleyecektir.

## 🛠️ Sorun Giderme

### "404 Page not found" Hatası

- Settings → Pages sayfasını kontrol edin
- GitHub Actions'ın başarıyla çalıştığından emin olun
- 5-10 dakika bekleyin (ilk deployment zaman alabilir)

### Build Hataları

- Actions sekmesindeki hata loglarını kontrol edin
- _config.yml dosyasının doğru formatta olduğundan emin olun

### Değişiklikler Görünmüyor

- Tarayıcı önbelleğini temizleyin (Ctrl+F5)
- GitHub Actions'ın tamamlandığından emin olun
- Repository'nin Public olduğundan emin olun

## 📝 Notlar

- İlk deployment 10 dakikaya kadar sürebilir
- Sonraki güncellemeler genelde 2-3 dakika içinde yayınlanır
- GitHub Pages ücretsiz kullanım için aylık 100GB bant genişliği limiti vardır
- Repository Public olmalıdır (ücretsiz hesaplar için)

## 🔗 Faydalı Linkler

- [GitHub Pages Dokümantasyonu](https://docs.github.com/en/pages)
- [Jekyll Dokümantasyonu](https://jekyllrb.com/docs/)
- [GitHub Actions Dokümantasyonu](https://docs.github.com/en/actions)

---

**Başarılar! 🎉**

Herhangi bir sorun yaşarsanız, GitHub Issues bölümünden destek alabilirsiniz.
