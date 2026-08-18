# boldedit.rotamfizik.com — BoldEdit tanıtım + yasal sayfalar

Google OAuth doğrulaması "homepage must be hosted on a **verified domain you own**"
diyor ve github.io'yu kabul etmiyor (alan adı GitHub'ın). rotamfizik.com bizim
kontrolümüzde olduğu için BoldEdit sayfaları onun bir ALT ALANINDA yayınlanıyor.

## ⚠️ AYRI DEPO OLMASININ SEBEBİ — SİLMEYİN

Bu klasör `MirBedirhanKaygusuz.github.io` deposuna KONULMAZ. O bir "user site"tır ve
içine `CNAME` dosyası koymak TÜM siteyi özel alan adına taşır; `mirbedirhankaygusuz.github.io`
adresleri yönlenmeye başlar. TikTok'un ONAYLI redirect adresi
`https://mirbedirhankaygusuz.github.io/boldedit/tiktok-callback/` orada duruyor ve
OAuth redirect'leri BİREBİR eşleşme ister — yönlendirme onu kırar.

Bu yüzden: **ayrı bir depo (ör. `boldedit-site`) → Pages → custom domain.**
github.io olduğu gibi kalır, TikTok akışına dokunulmaz.

## Kurulum

1. Yeni GitHub deposu aç (`boldedit-site`), bu klasörün İÇERİĞİNİ köküne koy.
2. Settings → Pages → Source: main / root.
3. GoDaddy DNS → CNAME kaydı: `boldedit` → `mirbedirhankaygusuz.github.io`
   (apex ve www'e DOKUNMA — babanın sitesi Vercel'de, oradan geliyor.)
4. Pages ayarında custom domain `boldedit.rotamfizik.com` + "Enforce HTTPS".

## Google Cloud Console → OAuth consent screen

- Application home page: `https://boldedit.rotamfizik.com/`
- Privacy policy:        `https://boldedit.rotamfizik.com/boldedit-privacy/`
- Terms of service:      `https://boldedit.rotamfizik.com/terms.html`
- Authorized domain:     `rotamfizik.com`

## Search Console

`rotamfizik.com` için **Domain** property aç ve GoDaddy'ye TXT kaydı ekleyerek doğrula
(alt alanların hepsini kapsar). Doğrulayan hesap, GCP projesinde **owner ya da editor**
olmalı — Google'ın açık şartı.

## github.io tarafı

Silinmez, olduğu gibi kalır: TikTok redirect'i ve mevcut gizlilik sayfası orada yaşamaya
devam eder. İki alan adında aynı gizlilik metninin durması sorun değildir.
