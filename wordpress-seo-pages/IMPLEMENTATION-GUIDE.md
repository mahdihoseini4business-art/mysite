# راهنمای پیاده‌سازی در وردپرس + Elementor

## اطلاعات سایت
- **دامنه:** mahdihoseiny.ir
- **قالب:** Shokrino
- **صفحه‌ساز:** Elementor
- **رنگ‌ها:** #0f172a | #b91c1c | #14b8a6 | #ffffff

---

## مرحله ۱: رفع مشکل noindex (فوری!)

صفحه اصلی شما الان `noindex` دارد و گوگل آن را ایندکس نمی‌کند.

1. وارد **پنل وردپرس** شوید
2. **Rank Math** (یا Yoast) → Titles & Meta → Homepage
3. Robots Meta → **Index** را انتخاب کنید
4. ذخیره کنید

---

## مرحله ۲: اضافه کردن CSS برند

### روش A: از Customizer
1. Appearance → Customize → Additional CSS
2. محتوای فایل `css/mahdi-brand.css` را کپی و Paste کنید
3. Publish

### روش B: از Elementor
1. Elementor → Site Settings → Custom CSS
2. محتوای فایل را Paste کنید

---

## مرحله ۳: تنظیم رنگ‌های Elementor

1. Elementor → Site Settings → Global Colors
2. این رنگ‌ها را اضافه کنید:

| نام | کد رنگ |
|---|---|
| Dark | #0f172a |
| Red | #b91c1c |
| Teal | #14b8a6 |
| White | #ffffff |

3. Global Fonts → Primary: Vazirmatn (از قبل نصب است)

---

## مرحله ۴: ساخت صفحات جدید

برای هر صفحه در پوشه `pages/`:

1. **Pages → Add New**
2. عنوان صفحه را وارد کنید
3. **Edit with Elementor**
4. محتوای فایل `.md` مربوطه را بخش‌به‌بخش در Elementor بسازید
5. **SEO Meta** را در Rank Math تنظیم کنید (Title و Description از فایل)
6. **Permalink** را طبق URL پیشنهادی تنظیم کنید
7. Publish

### ترتیب ساخت (اولویت):
1. ✅ `/mashvareh-branding` — مشاوره برندینگ
2. ✅ `/mashvareh-bazaryabi` — مشاوره بازاریابی
3. ✅ `/moshaver-kochak` — کسب‌وکارهای کوچک
4. ✅ `/moshavereh-raygan` — مشاوره رایگان
5. ✅ `/ghimat-moshavereh` — قیمت
6. 🔄 صفحه اصلی — بازنویسی (فایل `00-homepage-seo.md`)

### صفحات خدمات فرعی (پوشه `pages/services/`):

| URL | فایل | کلمه کلیدی |
|---|---|---|
| `/services/hoviat-bazari` | `hoviat-bazari.md` | طراحی هویت بصری برند |
| `/services/estrategi-brand` | `estrategi-brand.md` | استراتژی برند |
| `/services/estrategi-bazaryabi` | `estrategi-bazaryabi.md` | استراتژی بازاریابی |
| `/services/digital-marketing` | `digital-marketing.md` | مشاوره بازاریابی دیجیتال |
| `/services/online` | `online.md` | مشاوره بازاریابی آنلاین |
| `/services/manshor-brand` | `manshor-brand.md` | تدوین منشور برند |
| `/services/estrateji-mohtava` | `estrateji-mohtava.md` | استراتژی محتوا |
| `/services/rebranding` | `rebranding.md` | ری‌برندینگ |
| `/services/brand-shakhsi` | `brand-shakhsi.md` | برندینگ شخصی |
| `/services/logo` | `logo.md` | طراحی لوگو حرفه‌ای |
| `/services/social-media` | `social-media.md` | مدیریت شبکه‌های اجتماعی |
| `/services/instagram-ads` | `instagram-ads.md` | تبلیغات اینستاگرام |
| `/services/marketing-campaign` | `marketing-campaign.md` | طراحی کمپین بازاریابی |
| `/services/seo-content` | `seo-content.md` | سئو و بازاریابی محتوا |

---

## مرحله ۵: ساختار Elementor هر صفحه

### الگوی استاندارد:

```
┌─────────────────────────────┐
│  HERO (پس‌زمینه #0f172a)    │
│  H1 + Subtitle + 2 CTA     │
├─────────────────────────────┤
│  محتوای اصلی (سفید)         │
│  H2 + متن + کارت‌ها         │
├─────────────────────────────┤
│  FAQ (پس‌زمینه #f8fafc)    │
│  Accordion Elementor        │
├─────────────────────────────┤
│  CTA Banner (#b91c1c)       │
│  H2 + دکمه رزرو             │
└─────────────────────────────┘
```

### ویجت‌های Elementor پیشنهادی:
- **Hero:** Section با Background Gradient + Heading + Text + Button
- **خدمات:** Icon Box یا Flip Box (از Element Pack)
- **FAQ:** Accordion widget
- **CTA:** Section با Background Color + Heading + Button
- **آمار:** Counter widget

---

## مرحله ۶: بهینه‌سازی صفحات موجود

| صفحه | اقدام |
|---|---|
| `/about-me` | SEO Title: «بهترین مشاور برندینگ» + لینک به صفحات خدمات |
| `/consultant` | SEO Title: «رزرو جلسه مشاوره برندینگ» + Schema |
| `/blog` | دسته‌بندی جدید (برندسازی، بازاریابی، مشکلات) |
| `/contact-us` | نگه‌داری + لینک به consultant |

---

## مرحله ۷: منوی سایت

منوی اصلی را به‌روز کنید:

```
خدمات ▼
  ├── مشاوره برندینگ
  ├── مشاوره بازاریابی
  ├── کسب‌وکارهای کوچک
  └── خدمات فرعی ▼
        ├── هویت بصری برند
        ├── استراتژی برند
        ├── استراتژی بازاریابی
        ├── بازاریابی دیجیتال
        ├── مشاوره آنلاین
        ├── منشور برند
        ├── استراتژی محتوا
        ├── ری‌برندینگ
        ├── برندینگ شخصی
        ├── طراحی لوگو
        ├── شبکه‌های اجتماعی
        ├── تبلیغات اینستاگرام
        ├── کمپین بازاریابی
        └── سئو و محتوا

مقالات
درباره من
مشاوره رایگان  ← (دکمه قرمز در منو)
```

---

## مرحله ۸: لینک‌سازی داخلی

بعد از ساخت هر صفحه:
1. از صفحه اصلی به ۳ صفحه خدمات لینک دهید
2. از هر صفحه خدمت به صفحات مرتبط لینک دهید
3. از مقالات وبلاگ به صفحات خدمات CTA بگذارید
4. همه صفحات به `/consultant` لینک CTA داشته باشند

---

## مرحله ۹: Schema Markup

در Rank Math → Schema:
- صفحات خدمات → **Service** schema
- صفحه اصلی → **Person** + **WebSite**
- `/about-me` → **Person**
- `/consultant` → **Service** با offers

---

## مرحله ۱۰: Sitemap

1. Rank Math → Sitemap Settings → فعال
2. صفحات جدید خودکار اضافه می‌شوند
3. در Google Search Console → Sitemap را Submit کنید

---

## لوگو (فعلاً ندارید)

تا لوگو آماده شود، از متن استفاده کنید:

```html
<span class="mh-logo-text">مهدی <span>حسینی</span></span>
```

یا در Elementor: Heading widget با استایل:
- «مهدی» → رنگ #0f172a
- «حسینی» → رنگ #b91c1c

---

## چک‌لیست نهایی

- [ ] noindex صفحه اصلی رفع شد
- [ ] CSS برند اضافه شد
- [ ] رنگ‌های Global Elementor تنظیم شد
- [ ] ۵ صفحه اولویت بالا ساخته شد
- [ ] ۱۴ صفحه خدمات فرعی ساخته شد
- [ ] صفحه اصلی بازنویسی شد
- [ ] منوی سایت به‌روز شد
- [ ] لینک‌سازی داخلی انجام شد
- [ ] Schema markup تنظیم شد
- [ ] Sitemap در Search Console ثبت شد
- [ ] اولین ۴ مقاله وبلاگ منتشر شد

---

## سوال دارید؟

اگر در هر مرحله گیر کردید، بگویید تا راهنمایی دقیق‌تر بدهم.
