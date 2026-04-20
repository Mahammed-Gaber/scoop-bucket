# Pixify Scoop bucket

**[English](#english) | [العربية](#arabic)**

Official Scoop bucket for [Pixify](https://github.com/Mahammed-Gaber/pixify) — same release URLs and editions as the [Homebrew tap](https://github.com/Mahammed-Gaber/homebrew-pixify) (`pixify-free` / `pixify-pro`).

---

<div id="english" dir="ltr">

## English

### Available manifests

| App | Manifest | CLI after install |
|-----|----------|-------------------|
| Free | `pixify-free.json` | `pixify-free` |
| Pro | `pixify-pro.json` | `pixify-pro` |

Releases (including Windows zips and checksums) are published on **[Mahammed-Gaber/pixify](https://github.com/Mahammed-Gaber/pixify/releases)** — not on the `Pixify-Pro` repo alone.

### Prerequisites

- [Scoop](https://scoop.sh/) installed.
- **64-bit Windows** (manifests match `Pixify-*-Windows-v{version}.zip`).

### Add this bucket (first time)

Replace `OWNER/REPO` with your GitHub path if you fork the bucket:

```powershell
scoop bucket add pixify https://github.com/Mahammed-Gaber/scoop-bucket
```

### Install

**Free:**

```powershell
scoop install pixify/pixify-free
```

**Pro:**

```powershell
scoop install pixify/pixify-pro
```

If the bucket name differs, use `scoop install <bucket-name>/pixify-free` (or `pixify-pro`).

### libvips on Windows

The Homebrew formulas treat **vips** as optional in code; on Windows you usually need **libvips** available (PATH) for non-static builds.

- Guide: [install-libvips.md](https://github.com/Mahammed-Gaber/pixify/blob/main/docs/install-libvips.md)
- Optional: after `scoop bucket add extras`, you can try `scoop install extras/vips` (see `suggest` in each manifest).

### Update

```powershell
scoop update pixify-free
scoop update pixify-pro
```

### Uninstall

```powershell
scoop uninstall pixify-free
scoop uninstall pixify-pro
```

### Maintainer: bump version / hash after a new GitHub release

1. Ensure release assets exist: `Pixify-Free-Windows-vX.Y.Z.zip` and `Pixify-Pro-Windows-vX.Y.Z.zip` on `Mahammed-Gaber/pixify`.
2. Update `version` and `architecture.64bit.url` / `hash` in both JSON files (or run `scoop hash <path-to-json>` / your bucket’s checkver workflow).
3. `checkver` / `autoupdate` track the **pixify** repo tag `v$version`.

### Migration from old `pixify.json`

The previous single manifest pointed at the wrong repo, asset name, and `pixify.exe`. Remove it and install **`pixify-pro`** or **`pixify-free`** explicitly:

```powershell
scoop uninstall pixify
scoop install pixify/pixify-pro
```

### Links

- [Pixify repository](https://github.com/Mahammed-Gaber/pixify)
- [Issues](https://github.com/Mahammed-Gaber/pixify/issues)
- [Homebrew tap](https://github.com/Mahammed-Gaber/homebrew-pixify)

</div>

---

<div id="arabic" dir="rtl">

## العربية

### الملفات المتاحة (manifests)

| التطبيق | الملف | الأمر بعد التثبيت |
|---------|--------|---------------------|
| مجاني | `pixify-free.json` | `pixify-free` |
| Pro | `pixify-pro.json` | `pixify-pro` |

الإصدارات (ومنها أرشيفات Windows والـ SHA256) تُنشر على **[Mahammed-Gaber/pixify](https://github.com/Mahammed-Gaber/pixify/releases)** — نفس مصدر الـ Homebrew، وليس اعتماداً أساسياً على مستودع `Pixify-Pro` فقط.

### المتطلبات

- [Scoop](https://scoop.sh/) مثبت.
- **Windows 64-bit** (يتوافق مع أسماء `Pixify-*-Windows-v{version}.zip`).

### إضافة الـ bucket (أول مرة)

استبدل مسار الريبو إذا كان عندك fork:

```powershell
scoop bucket add pixify https://github.com/Mahammed-Gaber/scoop-bucket
```

### التثبيت

**مجاني:**

```powershell
scoop install pixify/pixify-free
```

**Pro:**

```powershell
scoop install pixify/pixify-pro
```

### libvips على Windows

غالباً تحتاج **libvips** في PATH لبناءات Windows غير الـ static.

- الدليل: [install-libvips.md](https://github.com/Mahammed-Gaber/pixify/blob/main/docs/install-libvips.md)
- اختياري: `scoop bucket add extras` ثم `scoop install extras/vips` (انظر `suggest` في الـ manifest).

### التحديث

```powershell
scoop update pixify-free
scoop update pixify-pro
```

### إلغاء التثبيت

```powershell
scoop uninstall pixify-free
scoop uninstall pixify-pro
```

### للمشرف: بعد إصدار جديد على GitHub

1. تأكد من وجود `Pixify-Free-Windows-vX.Y.Z.zip` و `Pixify-Pro-Windows-vX.Y.Z.zip` على `Mahammed-Gaber/pixify`.
2. حدّث `version` و `url` و `hash` في الملفين (أو استخدم `scoop hash` / سكربت checkver عندك).
3. `checkver` يتبع تاغات مستودع **pixify** (`v$version`).

### الانتقال من `pixify.json` القديم

الملف القديم كان يشير لريبو/أصل خاطئ و`pixify.exe`. احذف التثبيت القديم وثبّت **`pixify-pro`** أو **`pixify-free`**:

```powershell
scoop uninstall pixify
scoop install pixify/pixify-pro
```

### روابط

- [مستودع Pixify](https://github.com/Mahammed-Gaber/pixify)
- [الإبلاغ عن مشكلة](https://github.com/Mahammed-Gaber/pixify/issues)
- [Homebrew tap](https://github.com/Mahammed-Gaber/homebrew-pixify)

</div>
