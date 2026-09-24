# مدل داده و ساختار محتوایی: صفحه فرود فارسی (Data Model & Content Structure)

**کد فیچر**: `001-persian-landing-page`  
**تاریخ**: ۲۰۲۶-۰۹-۲۴ (2026-09-24)  
**سند مشخصات مبنا**: `specs/001-persian-landing-page/spec.md`  

---

## ۱. نهاد هدر و نوار وضعیت سیستم (Top System Bar Entity)

```yaml
TopBar:
  kernel_title: "کرنل سیستم RASHAI"
  host_badge: "[میزبانی روی RASHAI.DEV]"
  role_badge: "توسعه‌دهنده ابزار و سامانه‌های خودگردان"
  lang_switcher:
    label: "English / EN"
    url: "../"
    tooltip: "مشاهده نسخه اصلی انگلیسی جهت مقایسه"
```

---

## ۲. نهاد معرفی و بخش هیرو (Hero Entity)

```yaml
HeroSection:
  eyebrow: "آزمایشگاه شخصی و زرادخانه ابزارها"
  title_primary: "RashAI"
  title_tld: ".dev"
  description: "طراحی و مهندسی شده توسط رشا (علی رشیدی). ساخت ابزارهای الگوریتمی با اهرم بالا، جریان‌های کاری ایجنتیک و موتورهای تصمیم‌گیری خودکار مبتنی بر هوش مصنوعی مدرن."
  tags:
    - label: "سامانه‌های هوش مصنوعی"
      type: "primary"
    - label: "جریان‌های کاری ایجنتیک"
      type: "teal"
    - label: "ریاضیات تصمیم"
      type: "default"
    - label: "اتوماسیون فرایندها"
      type: "default"
    - label: "متن‌باز"
      type: "default"
```

---

## ۳. ماتریس آجرهای ماژولار باوهاوس (Brick Matrix Entity)

```yaml
BrickMatrix:
  title: "ماتریس موتور ماژولار"
  rows:
    - row_id: 1
      bricks:
        - text: "دستور / استدلال"
          color: "ink"
          width: 140px
        - text: "ارزیابی U"
          color: "coral"
          width: 80px
    - row_id: 2
      bricks:
        - text: "خط‌لوله"
          color: "teal"
          width: 90px
        - text: "استقرار آرتفکت"
          color: "coral-dk"
          width: 130px
    - row_id: 3
      bricks:
        - text: "داده"
          color: "sand"
          width: 70px
        - text: "حلقه بازخورد ■"
          color: "ink"
          width: 150px
```

---

## ۴. نهاد نوار آمار (Metrics Strip Entity)

```yaml
Metrics:
  - id: "arsenal_count"
    label: "زرادخانه ابزارهای فعال"
    value: "+۱۲"
    color: "coral"
  - id: "philosophy"
    label: "فلسفه اصلی مهندسی"
    value: "بدون کدهای اضافه (Zero Bloat)"
    color: "ink"
  - id: "execution_model"
    label: "الگوی اجرا"
    value: "هم‌افزایی انسان و هوش مصنوعی"
    color: "teal"
  - id: "node_domain"
    label: "گره دامنه"
    value: "RashAI.dev"
    color: "ink"
```

---

## ۵. نهاد کارت‌های ابزار زرادخانه (Tool Cards Entities)

```yaml
ToolCards:
  - id: "markov-kaisa"
    name: "Markov Kai'Sa"
    category: "گیمینگ الگوریتمی"
    status_label: "v2.0.0"
    status_type: "oss"
    description: "اسکریپر زنده داده‌های Lolalytics و تولیدکننده زنجیره تصمیم مارکوف برای League of Legends. محاسبه نمره فایده ریاضی (U) به جای نرخ برد خام و تزریق چیدمان بهینه ۷ آیتمی مستقیماً به کلاینت بازی."
    specs: ["Python 3", "Markov Chain", "Lolalytics API", "CLI Picker"]
    action_text: "مشاهده سورس / مخزن"
    action_url: "https://github.com/PersianXM/markov-kaisa"
    badge: "★ برگزیده"

  - id: "antigravity-suite"
    name: "مجموعه ابزارهای Antigravity"
    category: "تجربه توسعه هوش مصنوعی"
    status_label: "لایو"
    status_type: "live"
    description: "مجموعه‌ای جامع از ابزارهای توسعه برای Google Antigravity: اصلاح رندرینگ راست‌به‌چپ (RTL) و فارسی، مسیریابی پروکسی کدهای باز، ابزارهای تزریق مدل و ارکستریتورهای جریان کار خودکار."
    specs: ["Antigravity", "Proxy Router", "RTL Engine", "TypeScript"]
    action_text: "ابزارهای داخلی"
    action_url: null
    badge: "سوئیت توسعه"

  - id: "watermark-cleanser"
    name: "پاک‌کننده واترمارک جمینای"
    category: "هوش مصنوعی بصری و رسانه"
    status_label: "فعال"
    status_type: "live"
    description: "ابزار تخصصی برای شناسایی دقیق و حذف بدون افت کیفیت (Lossless) واترمارک‌های مصنوعی SynthID و آرتیفکت‌های خروجی‌های تصویری مدل‌های هوش مصنوعی Google Gemini."
    specs: ["Python", "OpenCV / PIL", "Gemini Vision"]
    action_text: "برنامه مستقل"
    action_url: null
    badge: "ابزار کاربردی"

  - id: "universal-skill-converter"
    name: "مبدل فراگیر مهارت‌ها (Skill Converter)"
    category: "مهندسی ایجنتیک"
    status_label: "متن‌باز"
    status_type: "oss"
    description: "نمایش میانی مستقل از پلتفرم (USIR) و خط‌لوله کامپایلر مهارت‌های ایجنت‌های هوش مصنوعی. ترنسپایل خودکار تعاریف ابزارها و جریان‌های کاری میان Claude، Cursor و Codex با بهینه‌سازی درخت انتزاعی نحو (AST)."
    specs: ["Python 3.11", "USIR Engine", "AST Optimizer", "FastAPI Web UI"]
    action_text: "مشاهده سورس / مخزن"
    action_url: "https://github.com/PersianXM/universal-skill-converter"
    badge: "★ برگزیده"

  - id: "option-box"
    name: "Option-Box"
    category: "مالی محاسباتی و معاملات الگوریتمی"
    status_label: "v1.4.0"
    status_type: "oss"
    description: "موتور بلادرنگ قیمت‌گذاری کمّی اختیار معامله و آربیتراژ برای بورس اوراق بهادار تهران (TSE). محاسبه پارامترهای یونانی بلک-شولز (دلتا، گاما، تتا، وگا، رو)، حل نوسان‌پذیری ضمنی (IV) و اسکن زنده ماتریس آربیتراژ."
    specs: ["Black-Scholes", "Greeks Engine", "IV Solver", "FastAPI", "TSETMC API"]
    action_text: "مشاهده سورس / مخزن"
    action_url: "https://github.com/PersianXM/Option-Box"
    badge: "★ برگزیده"

  - id: "meowmeow-tv"
    name: "MeowMeow TV"
    category: "استریم رسانه و اندروید"
    status_label: "v2.8.0"
    status_type: "oss"
    description: "کلاینت استریم سینمایی نسل جدید برای تلویزیون و اندروید باکس. توسعه‌یافته با Jetpack Compose for TV، پخش شتاب‌یافته سخت‌افزاری با Media3/ExoPlayer، مسیریابی هوشمند فوکوس کنترل از راه دور (D-pad) و رندرینگ زیرنویس سفارشی."
    specs: ["Kotlin 2.4", "Android SDK 37", "Compose for TV", "Media3 / ExoPlayer"]
    action_text: "مشاهده سورس / مخزن"
    action_url: "https://github.com/PersianXM/MeowMeow"
    badge: "Android TV"
```

---

## ۶. نهاد مانیفست و اصول سازنده (Manifesto Entity)

```yaml
Manifesto:
  title: "مانیفست سازنده ابزار"
  subtitle: "اصول معماری و استانداردهای طراحی سامانه‌ها"
  principles:
    - number: "۰۱"
      title: "اجرای تک‌کلیدی (One-Key Execution)"
      statement: "هر ابزار باید وظیفه مشخص خود را با کمترین اصطکاک و تنها با یک ورودی آغاز کند. ابزاری که نیازمند تنظیمات پیچیده روزمره باشد، ابزار مهندسی نیست؛ بوروکراسی نرم‌افزاری است."
    - number: "۰۲"
      title: "دقت و فایده ریاضیاتی (Math Rigor - Score U)"
      statement: "ما به جای میانگین‌های سطحی، فایده ریاضیاتی واقعی (Utility Score U) را در شرایط نااطمینانی بهینه‌سازی می‌کنیم. تصمیمات سامانه‌ها باید متکی بر زنجیره‌های محاسباتی مستحکم باشند."
    - number: "۰۳"
      title: "هم‌افزایی انسان و هوش مصنوعی (Cognitive Loop)"
      statement: "مدل‌های زبانی بزرگ مغز متفکر و موتور شناختی هستند؛ اما کدهای قطعی و استوار دترمینستیک، ستون فقرات اجرای امن و مطمئن هر سیستم به حساب می‌آیند."
```

---

## ۷. نهاد ارتباط و فوتر (Footer & Contact Entity)

```yaml
Footer:
  copy_toast_text: "آدرس ایمیل با موفقیت کپی شد!"
  email: "rasha@rashai.dev"
  github_url: "https://github.com/PersianXM"
  location_badge: "مهندسی‌شده با هوش مصنوعی · آبادان، ایران"
  copyright: "© ۲۰۲۶ RashAI.dev — تمام حقوق محفوظ است."
```
