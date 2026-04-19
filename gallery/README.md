# 🖼️ معرض الصور

معرض صور بالحجم الكامل مُحسَّن للهاتف — مستضاف على GitHub Pages.

---

## 🚀 خطوات الإعداد الأول

### 1. فعّل GitHub Pages
في إعدادات المستودع (Settings → Pages) اختر:
- **Source:** `Deploy from a branch`
- **Branch:** `main` → `/` (root)

ثم احفظ — سيظهر رابط موقعك مثل:
```
https://اسمك.github.io/اسم-المستودع/
```

### 2. فعّل صلاحية GitHub Actions للكتابة
في إعدادات المستودع:
`Settings → Actions → General → Workflow permissions`
→ اختر **"Read and write permissions"** ثم احفظ.

---

## 📤 كيفية إضافة الصور (أسهل طريقة)

### الطريقة ١ — رفع مباشر من المتصفح (بدون تقنية) ✅

1. افتح مستودعك على GitHub
2. ادخل مجلد **`photos/`**
3. اضغط **"Add file" → "Upload files"**
4. اسحب صورك أو اختَرها
5. اضغط **"Commit changes"**

✨ **ينتهي العمل هنا!** GitHub Action سيُحدِّث `photos.json` تلقائياً ويُضيف الصور للمعرض.

---

### الطريقة ٢ — عبر سطر الأوامر (للمطورين)

```bash
# انسخ صورك إلى مجلد photos/
cp /path/to/my-photo.jpg photos/

# ارفع التغييرات
git add photos/
git commit -m "إضافة صور جديدة"
git push
```

---

## 🛠️ تخصيص المعرض

في ملف `index.html`، ابحث عن هذا القسم:

```js
// ── Config ──────────────────────────────────────────────
const GALLERY_TITLE = 'معرض الصور';  // ← غيّر العنوان
```

---

## 📁 هيكل الملفات

```
/
├── index.html          ← صفحة المعرض
├── photos.json         ← قائمة الصور (تُحدَّث تلقائياً)
├── photos/             ← ضع صورك هنا
│   ├── photo1.jpg
│   └── ...
└── .github/
    └── workflows/
        └── update-gallery.yml   ← GitHub Action للتحديث التلقائي
```

---

## 📱 المميزات

- ✅ تصميم يُغطي الشاشة بالكامل
- ✅ محسَّن للهاتف أولاً
- ✅ تنقل بالسحب (Swipe)
- ✅ دعم لوحة المفاتيح (← →)
- ✅ تحميل تدريجي للصور
- ✅ تحديث تلقائي عند إضافة صور
- ✅ يعمل بدون خادم (GitHub Pages)
