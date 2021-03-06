---
machine_translated: true
machine_translated_rev: 72537a2d527c63c07aa5d2361a8829f3895cf2bd
---

# بند فرمت {#format-clause}

تاتر پشتیبانی از طیف گسترده ای از [فرمت های ترتیب](../../../interfaces/formats.md) که می تواند در نتایج پرس و جو در میان چیزهای دیگر استفاده می شود. راه های متعدد برای انتخاب یک فرمت برای وجود دارد `SELECT` خروجی یکی از این موارد مشخص است `FORMAT format` در پایان پرس و جو برای دریافت و در نتیجه داده ها در هر فرمت خاص.

فرمت خاص ممکن است یا برای راحتی استفاده می شود, ادغام با سیستم های دیگر و یا افزایش عملکرد.

## قالب پیشفرض {#default-format}

اگر `FORMAT` بند حذف شده است, فرمت پیش فرض استفاده شده است, که بستگی به هر دو تنظیمات و رابط مورد استفاده برای دسترسی به سرور کلیک. برای [رابط قام](../../../interfaces/http.md) و [مشتری خط فرمان](../../../interfaces/cli.md) در حالت دسته ای فرمت پیش فرض است `TabSeparated`. برای مشتری خط فرمان در حالت تعاملی فرمت پیش فرض است `PrettyCompact` (این تولید جداول جمع و جور انسان قابل خواندن).

## پیاده سازی اطلاعات {#implementation-details}

هنگام استفاده از سرویس گیرنده خط فرمان داده ها همیشه بر روی شبکه در فرمت موثر داخلی منتقل می شود (`Native`). مشتری به طور مستقل تفسیر می کند `FORMAT` بند از پرس و جو و فرمت های داده های خود را (در نتیجه تسکین شبکه و سرور از بار اضافی).
