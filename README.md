# 🌸 بوت أمل للحوامل | Aml Pregnancy Bot

بوت تيليجرام ذكي للعناية بالحوامل، يعمل باللغة العربية ومدعوم بالذكاء الاصطناعي.

An AI-powered Arabic Telegram bot for pregnant women, powered by Claude.

---

## ✨ المميزات | Features

| الميزة | الوصف |
|--------|-------|
| 📅 نصائح أسبوعية | معلومات مخصصة لكل أسبوع من الحمل (1–40) |
| 🩺 فحص الأعراض | تحليل الأعراض وتقديم المشورة |
| 🥗 التغذية | دليل شامل للتغذية الصحية للحامل |
| 🚨 علامات الخطر | قائمة بالأعراض التي تستدعي الطبيب فوراً |
| 💬 أسئلة حرة | الإجابة على أي سؤال يخص الحمل |

---

## 🚀 التثبيت | Setup

### الخطوة 1: إنشاء بوت تيليجرام

1. افتح تيليجرام وابحث عن **@BotFather**
2. أرسل `/newbot`
3. اختر اسماً للبوت (مثلاً: `نور للحوامل`)
4. اختر username (مثلاً: `nour_pregnancy_bot`)
5. احتفظ بـ **Token** الذي ستحصل عليه

### الخطوة 2: الحصول على مفتاح Anthropic

1. اذهب إلى [console.anthropic.com](https://console.anthropic.com)
2. أنشئ حساباً أو سجّل الدخول
3. من قسم **API Keys**، أنشئ مفتاحاً جديداً
4. احتفظ بالمفتاح

### الخطوة 3: تثبيت المتطلبات

```bash
pip install -r requirements.txt
```

### الخطوة 4: إعداد المتغيرات البيئية

```bash
# على Linux/Mac
export TELEGRAM_TOKEN="your_telegram_token_here"
export ANTHROPIC_API_KEY="your_anthropic_key_here"

# على Windows (Command Prompt)
set TELEGRAM_TOKEN=your_telegram_token_here
set ANTHROPIC_API_KEY=your_anthropic_key_here
```

أو انسخ `.env.example` إلى `.env` وعدّل القيم، ثم استخدم:
```bash
pip install python-dotenv
```
وأضف في بداية `bot.py`:
```python
from dotenv import load_dotenv
load_dotenv()
```

### الخطوة 5: تشغيل البوت

```bash
python bot.py
```

---

## 📁 هيكل المشروع

```
pregnancy_bot/
├── bot.py              # الكود الرئيسي للبوت
├── requirements.txt    # المكتبات المطلوبة
├── .env.example        # نموذج متغيرات البيئة
└── README.md           # هذا الملف
```

---

## ☁️ النشر على الخادم | Deployment

### على Railway (مجاني):
1. ارفع الكود على GitHub
2. اذهب إلى [railway.app](https://railway.app) وأنشئ مشروعاً جديداً
3. اربطه بـ GitHub repo
4. أضف المتغيرات البيئية في إعدادات Railway
5. سيعمل البوت تلقائياً!

### على VPS/Ubuntu:
```bash
# تثبيت في الخلفية باستخدام screen
screen -S pregnancy_bot
python bot.py
# Ctrl+A ثم D للخروج من screen مع بقاء البوت يعمل
```

---

## ⚠️ ملاحظة مهمة | Disclaimer

هذا البوت للمعلومات العامة فقط وليس بديلاً عن الاستشارة الطبية المتخصصة.
يجب دائماً استشارة طبيب متخصص لأي قرار طبي.

*This bot provides general information only and is not a substitute for professional medical advice.*

---

## 🛠️ التخصيص | Customization

- لتغيير شخصية البوت: عدّل `SYSTEM_PROMPT` في `bot.py`
- لإضافة أوامر جديدة: أضف `CommandHandler` جديداً
- لتغيير اللغة: عدّل النصوص في `SYSTEM_PROMPT` والرسائل

---

صُنع بـ ❤️ لدعم الأمهات في رحلتهن الجميلة 🤰
