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
    description: "اسکریپر زنده داده‌های Lolalytics و تولیدکننده زنجیره تصمیم مارکوف برای League of Legends. محاسبه نمره فایده ریاضی (U) به جای نرخ برد خام و تزریق چیدمان بهینه ۷ آیتمی مستقیماً به کلاینت."
    specs: ["Python 3", "Markov Chain", "Lolalytics API", "CLI Picker"]
    action_text: "مشاهده مخزن گیت‌هاب"
    action_url: "https://github.com/PersianXM/markov-kaisa"

  - id: "antigravity-suite"
    name: "مجموعه ابزارهای Antigravity"
    category: "اکوسیستم توسعه‌دهنده"
    status_label: "فعال / توسعه"
    status_type: "live"
    description: "افزونه‌ها و ابزارهای پیشرفته برای محیط توسعه Google Antigravity، شامل اصلاح خودکار نمایش راست‌به‌چپ (RTL)، مسیریابی کدهای باز و تزریق مدل‌ها."
    specs: ["PowerShell", "Extension Scripts", "RTL Injection", "AGY Tools"]
    action_text: "مشاهده کد منبع"
    action_url: "https://github.com/PersianXM"

  - id: "watermark-cleanser"
    name: "پاک‌کننده واترمارک Gemini"
    category: "پردازش بصری"
    status_label: "پایدار"
    status_type: "stable"
    description: "ابزار سبک حذف واترمارک‌های مصنوعی از تصاویر تولیدشده توسط مدل‌های تصویری Imagen و Gemini، بازگرداننده خلوص بصری آرتفکت‌ها بدون افت کیفیت."
    specs: ["Python", "OpenCV", "Image Processing", "Batch CLI"]
    action_text: "مشاهده کد منبع"
    action_url: "https://github.com/PersianXM"

  - id: "universal-skill-converter"
    name: "مبدل مهارت‌های فراگیر (Skill Converter)"
    category: "هوش مصنوعی ایجنتیک"
    status_label: "پایدار"
    status_type: "stable"
    description: "ابزار تبدیل ساختار مهارت‌ها بین اکوسیستم‌های مختلف هوش مصنوعی؛ تبدیل خودکار تعاریف ابزار، فایل‌های SKILL.md و پروتکل‌های اجرایی میان پلتفرم‌ها."
    specs: ["Node.js", "AST Parser", "Markdown Specs", "CLI"]
    action_text: "مشاهده کد منبع"
    action_url: "https://github.com/PersianXM"

  - id: "media-pipeline-bots"
    name: "بات‌های پایپ‌لاین رسانه"
    category: "سنتز صوت و رسانه"
    status_label: "سرویس زنده"
    status_type: "live"
    description: "سیستم خودکار تولید پادکست، صداگذاری متون، و استخراج خلاصه‌های تحلیلی برای کانال‌های تلگرامی با معماری صف توزیع‌شده."
    specs: ["Telegram Bot API", "Edge TTS", "Docker", "AsyncIO"]
    action_text: "مشاهده کد منبع"
    action_url: "https://github.com/PersianXM"

  - id: "domain-tabular-ocr"
    name: "استخراج‌گر داده‌های جدولی و مالی"
    category: "سامانه‌های اسنادی"
    status_label: "تخصصی"
    status_type: "stable"
    description: "موتور تخصصی OCR و پردازش جداول پیچیده فیش‌های حقوقی و اسناد مالی صنعت نفت با اصلاح خودکار جریان متون دوزبانه و اعداد فارسی."
    specs: ["PyMuPDF", "RegEx Engines", "OCR Engine", "Excel Exporter"]
    action_text: "مشاهده کد منبع"
    action_url: "https://github.com/PersianXM"
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
