# Kova

Reklamsız, ücretsiz ve tamamen bilgisayarında çalışan bir medya indirici. Bağlantıyı yapıştırırsın, istediğin biçimde indirirsin. macOS ve Windows'ta çalışır.

Kova, açık kaynak [yt-dlp](https://github.com/yt-dlp/yt-dlp) motorunun üzerine kurulmuş bir arayüzdür. İndirmeyi yt-dlp yapar, dönüştürmeyi [FFmpeg](https://ffmpeg.org/) yapar. Kova bunları senin için tek pencerede toplar.

## İndir

En kolay yol: **[unlualp.com/kova](https://unlualp.com/kova/)**. Sayfa bilgisayarına uygun dosyayı öne çıkarır, tek tıkla iner.

Son sürüm her zaman burada da: **[github.com/alpunlu12-commits/kova/releases/latest](https://github.com/alpunlu12-commits/kova/releases/latest)**

| Bilgisayarın | İndireceğin dosya |
|---|---|
| Mac (Apple Silicon ve Intel, macOS 12 ve sonrası) | `Kova_<sürüm>_universal.dmg` |
| Windows 10 / 11 (64 bit) | `Kova_<sürüm>_x64-setup.exe` |

Sayfadaki `.tar.gz`, `.sig` ve `latest.json` dosyaları uygulama içi güncelleme içindir, bunları indirmene gerek yok. Dosyaların SHA-256 özetleri `SHA256SUMS.txt` içinde.

## Kurulum

### macOS

Tek bir sürüm hem Apple Silicon hem Intel Mac'lerde çalışır. macOS 12 (Monterey) ya da sonrası gerekir.

1. DMG'yi aç ve Kova'yı **Uygulamalar** klasörüne sürükle. Kova'yı DMG'nin içinden çalıştırma, yoksa kendini güncelleyemez.
2. Uygulamalar klasöründe Kova'ya çift tıkla. Kova Apple'a notarize ettirilmediği için macOS ilk seferde açmaz, bir uyarı gösterir. **Bitti**'ye (eski macOS'larda **Tamam**'a) bas. Çöp Sepeti'ne taşıma.
3. **Sistem Ayarları › Gizlilik ve Güvenlik**'i aç ve en alta, Güvenlik bölümüne in. Kova'nın engellendiğini yazan satırın yanındaki **Yine de Aç**'a bas. Bu düğme, Kova'yı açmayı denedikten sonra yaklaşık bir saat görünür.
4. Çıkan pencerede yine **Yine de Aç**'ı seç ve Mac'inin şifresini gir (ya da Touch ID kullan).

Bunu yalnızca ilk açılışta yaparsın. macOS 12'de yol biraz farklı: **Sistem Tercihleri › Güvenlik ve Gizlilik › Genel › Yine de Aç**.

Menü çubuğundan tarayıcıdaki videoyu indirmek istediğinde macOS bir kez daha izin sorar (Kova'nın tarayıcıyı okuması için). Bu izni sonradan **Sistem Ayarları › Gizlilik ve Güvenlik › Otomasyon**'dan değiştirebilirsin.

### Windows

Windows 10 ya da 11, 64 bit gerekir.

1. `Kova_<sürüm>_x64-setup.exe` dosyasını çalıştır. Tarayıcın dosyanın sık indirilmediğini söylerse dosyayı sakla.
2. Kurulum dosyası ücretli bir sertifikayla imzalı olmadığı için Windows "Windows bilgisayarınızı korudu" uyarısını gösterebilir. **Ek bilgi**'ye, sonra **Yine de çalıştır**'a bas.
3. Kurulum yalnızca senin kullanıcı hesabına yapılır, yönetici izni istemez.

Kova'yı kaldırmak için **Ayarlar › Uygulamalar** bölümünü kullan.

## Güncellemeler

Kova açıldıktan birkaç saniye sonra ve sonra günde bir, GitHub'da yeni sürüm olup olmadığına bakar. Yeni sürüm varsa pencerede "Kova <sürüm> hazır" yazar. **Güncelle**'ye basman yeter: Kova yeni sürümü indirir, imzasını doğrular, kurar ve yeniden açılır. İmza tutmazsa hiçbir şeyi değiştirmez. Süren indirmeler varsa önce sorar. **Ayarlar**'daki "Güncellemeleri denetle" ile istediğin zaman elle de bakabilirsin.

Kova'nın kullandığı yt-dlp, FFmpeg ve Deno ayrıca, kendi başlarına güncellenir: yt-dlp 6 saatte bir, diğerleri haftada bir. Bu güncellemeler süren indirmeleri durdurmaz.

0.4.0'dan önceki bir sürümü kullanıyorsan yeni sürümü bir kez elle indirip kur. Sonrası kendiliğinden gelir.

## Özellikler

- **Reklam yok, üyelik yok.** Her şey kendi bilgisayarında olur, araya bir sunucu girmez.
- **macOS ve Windows.** İkisinde de aynı arayüz, aynı biçimler.
- **Sekiz biçim.** Ses için MP3, M4A, OPUS, FLAC ve WAV; video için MP4, MKV ve WEBM. Her biçimin ne işe yaradığı uygulamada tek cümleyle yazar.
- **Gerçek kalite.** Sesler kaynağın en iyi kalitesinden çevrilir. OPUS ve M4A, kaynağın kendi sesini çoğu zaman hiç dönüştürmeden verir. MP3 için 320, 256, 192 ve 128 kbps de seçilebilir. Videolar 4K'ya (kaynakta varsa 8K'ya) kadar iner, MKV dönüştürmesiz en yüksek kaliteyi verir.
- **Rahat oynayan dosyalar.** MP4'te 1080p'ye kadar H.264 seçilir. Mac'te 2K ve 4K için, Mac AV1 destekliyorsa (M3 ve sonrası) QuickTime'ın açabildiği AV1 seçilir.
- **Altyazılar.** Videoda Türkçe ya da İngilizce altyazı varsa istersen dosyanın içine eklenir.
- **Müzik için hazır dosyalar.** MP3 ve M4A dosyalarına kapak resmi (istersen kare kırpılmış), başlık ve sanatçı bilgisi gömülür. İstersen sanatçı ve şarkı adı başlıktan ayrılır.
- **Oynatma listeleri.** Listeyi getir, istediğin videoları seç, hepsini sıraya koy. Aynı anda kaç dosyanın ineceğini (1 ile 3 arası) sen seçersin.
- **Menü çubuğu simgesi (Windows'ta saatin yanında).** Pencereyi kapatınca Kova orada çalışmaya devam eder. Mac'te tarayıcıda açık olan videoyu (Safari, Chrome, Arc, Brave, Edge, Vivaldi ve Opera; Firefox'ta olmaz), Windows'ta kopyaladığın bağlantıyı tek tıkla indirir. İndirme ilerlemesi simgede, Dock'ta ya da görev çubuğunda görünür.
- **İndirme geçmişi.** Biten indirmeler Kova'yı kapatıp açtığında da listede durur. Dosyayı tek tıkla klasöründe gösterir.
- **Klasör seçimi.** Dosyalar varsayılan olarak İndirilenler › Kova klasörüne iner. Klasörü Ayarlar'dan değiştirebilir ya da her indirmede sorulmasını seçebilirsin.
- **Lisans rozeti.** Videonun Creative Commons mu yoksa standart lisanslı mı olduğu önizlemede görünür.

## Bileşenler nasıl geliyor

Kova bu programları kendi içinde taşımaz. İlk açılışta, senin onayınla, resmi kaynaklarından indirir ve doğrular.

| Bileşen | Ne işe yarar | macOS kaynağı | Windows kaynağı | Doğrulama |
|---|---|---|---|---|
| yt-dlp | Medyayı bulur ve indirir | GitHub sürümleri, `yt-dlp_macos.zip` | GitHub sürümleri, `yt-dlp_win.zip` | Yayınlanan SHA-256 özeti |
| FFmpeg | Sesi ve görüntüyü dönüştürür, birleştirir | [ffmpeg.martin-riedl.de](https://ffmpeg.martin-riedl.de/) imzalı derlemesi | [gyan.dev](https://www.gyan.dev/ffmpeg/builds/) "release essentials" derlemesi | SHA-256 özeti; macOS'ta ayrıca Apple geliştirici imzası |
| Deno | yt-dlp'nin bazı siteler için ihtiyaç duyduğu JavaScript çalıştırıcı | GitHub sürümleri, `deno-<mimari>-apple-darwin.zip` | GitHub sürümleri, `deno-x86_64-pc-windows-msvc.zip` | SHA-256 özeti; macOS'ta ayrıca Apple geliştirici imzası |

yt-dlp varsayılan olarak gece kanalından gelir, çünkü sitelerdeki değişikliklere en hızlı o uyum sağlar. Ayarlar'dan kararlı kanala geçebilirsin. macOS'ta FFmpeg ve Deno'nun imzası, yalnızca kendi yayıncılarının Apple ekip kimliğini taşıyorsa kabul edilir.

Her sürüm kendi klasörüne iner, bu yüzden güncelleme sırasında süren indirmeler eski sürümle bitmeye devam eder. Eski sürümler bir sonraki açılışta silinir.

## Dosyalar nerede

| | macOS | Windows |
|---|---|---|
| İndirilen dosyalar (varsayılan) | `~/Downloads/Kova` | `%USERPROFILE%\Downloads\Kova` |
| Ayarlar, geçmiş ve bileşenler | `~/Library/Application Support/com.alp.downloader` | `%LOCALAPPDATA%\com.alp.downloader` |
| Geçici dosyalar | `~/Library/Caches/com.alp.downloader` | `%LOCALAPPDATA%\com.alp.downloader` |
| Günlük dosyası | `~/Library/Logs/com.alp.downloader/kova.log` | `%LOCALAPPDATA%\com.alp.downloader\kova.log` |

Kova'yı tamamen silmek istersen uygulamayı kaldırdıktan sonra bu klasörleri de silebilirsin. İndirdiğin dosyalara dokunulmaz.

## Hata bildirmek

Bir sorun görürsen [GitHub Issues](https://github.com/alpunlu12-commits/kova/issues) üzerinden yaz. Şunları eklersen çok işe yarar:

- Kova sürümü (Ayarlar'da yazar) ve işletim sistemin,
- ne yaptığın ve ne olduğu, ekranda çıkan hata yazısı,
- paylaşılabiliyorsa bağlantı,
- `kova.log` dosyası (adres yukarıda; dosya 1 MB'ı geçince baştan başlar).

## Kullanım notu

Kova; kendi videolarını, izin aldığın içerikleri ve Creative Commons gibi serbest lisanslı içerikleri kaydetmen için yapılmış ücretsiz bir araçtır. İndirdiğin içerikleri paylaşma, yeniden yükleme ya da ticari amaçla kullanma. Türkiye'de kişisel kopya yalnızca kazanç amacı olmadan kendi kullanımın içindir. Bazı sitelerin kullanım şartları indirmeyi kısıtlar, bu şartlara ve yasalara uymak senin sorumluluğundadır. Kova DRM korumalı, ücretli ya da üyelere özel içerikleri indirmez.

Kova medyayı kendi koduyla indirmez. İşi her zaman resmi yt-dlp programı yapar, Kova yalnızca ona ayarları iletir.

## Geliştirme

Gerekenler: Node.js 20.19 ya da 22.12 ve sonrası, Rust (rustup ile) ve Xcode komut satırı araçları.

```bash
npm install
```

Uygulamayı geliştirme modunda açmak için:

```bash
npm run app
```

Bu Mac için kurulabilir `.app` ve `.dmg` dosyası üretmek için:

```bash
npm run app:build
```

Çıktılar `src-tauri/target/release/bundle/` altına düşer.

Bu komut da aşağıdaki `app:build:win` de güncelleme paketi üretmez (`scripts/tauri.local.conf.json` kapatır), o yüzden imza anahtarı gerekmez. Güncelleme paketli sürümler yalnızca `npm run release` ile derlenir.

Arayüzü tarayıcıda, sahte bir arka uçla denemek için `npm run dev` çalıştırıp `http://localhost:1420/#ready` adresini aç. Adresin sonundaki `#ready` ilk açılış ekranını atlar, `#windows` Windows görünümünü, `#update` yeni sürüm uyarısını gösterir (birleştirilebilir: `#ready-windows-update`).

### Windows sürümünü Mac'te derlemek

Windows kurulum dosyası bu Mac'te, [cargo-xwin](https://github.com/rust-cross/cargo-xwin) ile çapraz derlenir. Bir kez şunları kur:

```bash
brew install llvm lld nsis
rustup target add x86_64-pc-windows-msvc
cargo install cargo-xwin
```

cargo-xwin ilk çalıştığında Microsoft'un C çalışma zamanı (CRT) ve Windows SDK dosyalarını indirir. Bu dosyalar Microsoft'un kendi lisansıyla gelir, kullanarak o lisansı kabul etmiş olursun. Sonra:

```bash
npm run app:build:win
```

Kurulum dosyası `src-tauri/target/x86_64-pc-windows-msvc/release/bundle/nsis/` altına düşer.

### Testler

```bash
cd src-tauri && cargo test
```

Gerçek internet üzerinden bileşen kurulumu ve indirme testleri için:

```bash
cd src-tauri && cargo test -- --ignored --nocapture
```

Bu testler Blender Vakfı'nın Creative Commons lisanslı "Big Buck Bunny" filmini kullanır.

Sürüm betiğini, uygulamayı derlemeden, sahte dosyalarla denemek için:

```bash
npm run release:test
```

### Sürüm yayınlamak

Gerekenler: yukarıdaki Windows araçları ve giriş yapılmış [GitHub CLI](https://cli.github.com/) (`brew install gh`, `gh auth login`).

1. Sürüm numarasını `src-tauri/tauri.conf.json`, `package.json`, `src-tauri/Cargo.toml` ve `src/mock.ts` içinde artır.
2. Kısa, Türkçe sürüm notunu `release-notes/<sürüm>.md` olarak yaz. Bu not GitHub sürüm sayfasında ve uygulamadaki güncelleme uyarısında görünür.
3. Değişiklikleri commit'le ve GitHub'a gönder.
4. Çalıştır:

   ```bash
   npm run release
   ```

   Betik macOS Universal ve Windows sürümlerini derler, imzaları denetler ve her şeyi `release/v<sürüm>/` içine koyar: DMG, kurulum dosyası, güncelleme paketleri ve imzaları, `latest.json` ve `SHA256SUMS.txt`. En sonda çalıştırman gereken `gh release create` komutunu yazar. Kendisi hiçbir şeyi yayınlamaz ve hiçbir şeyi GitHub'a göndermez.
5. Yazdığı komutu çalıştır ya da `npm run release -- --collect-only --publish` ile betiğe çalıştırt (önce onay ister).

Derlenmiş dosyaları yeniden toplamak için `npm run release -- --collect-only` yeter.

**İmza anahtarını yedekle.** Güncellemeler `~/.tauri/kova.key` dosyasındaki anahtarla imzalanır. Anahtarın şifresi macOS Anahtar Zinciri'nde `kova-updater-key` adıyla durur. Bu ikisini güvenli bir yere (örneğin bir şifre yöneticisine) yedekle ve kimseyle paylaşma. Anahtar kaybolursa kurulu Kova'lar yeni sürümleri artık kabul etmez, herkesin yeni sürümü elle indirmesi gerekir. Anahtar asla bu depoya girmemeli.

## Lisans

Kova'nın kendi kodu MIT lisanslıdır, ayrıntılar [LICENSE](LICENSE) dosyasında. yt-dlp'nin kaynak kodu Unlicense, hazır derlemesi GPLv3+ bileşenler içerir. FFmpeg GPL, Deno MIT lisanslıdır. Bu programlar Kova ile birlikte dağıtılmaz, her bilgisayara kendi resmi kaynaklarından iner.

## In English

Kova is a free, ad-free media downloader for macOS (Universal, macOS 12+) and Windows 10/11 x64. It is a front-end for [yt-dlp](https://github.com/yt-dlp/yt-dlp) and [FFmpeg](https://ffmpeg.org/): Kova has no media download code of its own; it fetches yt-dlp, FFmpeg and Deno from their official sources on first run, checking their SHA-256 sums (and, on macOS, the publishers' Apple signatures). Get it from the [latest release](https://github.com/alpunlu12-commits/kova/releases/latest): the `.dmg` for Mac, the `-setup.exe` for Windows. The Mac app is not notarized and the Windows installer is not code-signed, so macOS asks you to allow the first launch in System Settings › Privacy & Security ("Open Anyway"), and Windows SmartScreen needs "More info" › "Run anyway". Later versions install from inside the app. Kova is meant for your own videos, content you have permission to save and freely licensed media; it does not download DRM-protected, paid or members-only content. The interface is in Turkish. MIT licensed.
