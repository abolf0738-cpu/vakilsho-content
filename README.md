# وکیل شو - محتوای آنلاین

این مخزن فایل `content.json` را نگه می‌دارد که اپ «وکیل شو» (Lafzdar) از آن پرونده‌ها، تبلیغات و اطلاعیه را دریافت می‌کند.

## آدرس فایل برای اپ

```
https://raw.githubusercontent.com/abolf0738-cpu/vakilsho-content/main/content.json
```

## ساختار content.json

```json
{
  "announcement": "متن اطلاعیه (اختیاری)",
  "cases": [ ... پرونده‌ها ... ],
  "ads": [ ... تبلیغات ... ]
}
```

### نمونه پرونده

هر پرونده باید این فیلدها را داشته باشد:
- `id` (رشته یکتا)
- `category` (مثل family, fraud, homicide, ...)
- `title`, `level`, `brief`, `clientRole`, `allegation`, `issue`
- `evidence` (آرایه از مدارک)
- `questions` (آرایه از سوالات با options و correct و explain)
- `explanation`

### نمونه تبلیغ

```json
{
  "title": "عنوان",
  "text": "متن تبلیغ",
  "link": "https://example.com",
  "enabled": true,
  "placements": ["all"]
}
```

placements می‌تواند شامل: `all`, `home`, `categories`, `cases`, `play`, `result`, `info` باشد.

## نحوه به‌روزرسانی

۱. فایل `content.json` را ویرایش کنید.
۲. تغییرات را کامیت و پوش کنید.
۳. در اپ دکمه «به‌روزرسانی پرونده‌ها» را بزنید یا صبر کنید تا اپ خودش همگام شود.
