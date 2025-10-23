# Smart Money Algo Pro E5 — كيفية التشغيل

## المتطلبات الأساسية
- Python 3.10 أو أحدث.
- تثبيت الحزم الاختيارية:
  - `ccxt` في حال استخدام ماسح Binance USDT-M Futures.
- اتصال إنترنت عند تشغيل الماسح (اختياري).

## تثبيت الاعتمادات
في حال الحاجة إلى `ccxt`:
```bash
python -m pip install --upgrade ccxt
```
لا توجد اعتمادات إلزامية أخرى؛ السكربت يعمل بالمكتبات القياسية.

## تشغيل التحليل على بيانات محلية
1. جهّز ملف JSON يحوي مصفوفة من شموع OHLCV بالحقول `time`, `open`, `high`, `low`, `close`, `volume`.
2. نفّذ:
```bash
python smart_money_algo_pro_e5.py --data path/to/file.json --analysis-timeframe 1h --bars 5000
```
- `--analysis-timeframe` يضبط الإطار الزمني الأساسي المستخدم داخل المحرك.
- `--bars` يحدد عدد الشموع التي سيتم تحليلها (القيمة الافتراضية 5000).
- يكتب التحليل إلى `FINAL_REPORT_SMART_MONEY_ANALYSIS.md` في نفس المجلد.

للتشغيل مع الإعدادات الافتراضية على بيانات مدمجة:
```bash
python smart_money_algo_pro_e5.py --no-scan --analysis-timeframe 1h
```

## تشغيل ماسح Binance USDT-M Futures
يتطلب توفر `ccxt` واتصال إنترنت.
```bash
python smart_money_algo_pro_e5.py --timeframe 1h --lookback 0 --symbols auto
```
- `--timeframe` يحدد الإطار الزمني للماسح (مثل 15m، 1h، 4h، 1d).
- `--lookback` = 0 يجلب التاريخ الكامل، أو عدديًا (مثال 1000) لتحليل آخر عدد محدد من الشموع بعد بناء السجل التاريخي.
- `--symbols auto` يفحص جميع عقود Binance USDT-M. يمكن تمرير قائمة مفصولة بفواصل مثل `BTC/USDT:USDT,ETH/USDT:USDT`.
- استخدم `--min-daily-change X` لتخطي الرموز ذات تغير 24 ساعة أقل من X (القيمة الافتراضية 0 تعني لا فلترة).
- استخدم `--meme-volume-threshold V` لتجاهل عملات الميم ذات سيولة 24 ساعة أقل من القيمة V (بالـUSDT). القيمة الافتراضية 5,000,000 وتعيينها إلى 0 يعطل الفلتر.
- `--zone-alerts on|off` لتفعيل أو تعطيل التنبيهات الفردية لمناطق EXT/IDM/GOLDEN.
- `--zone-alert-max-age N` يحدد أكبر عمر بالشموع للمنطقة قبل تجاهل التنبيه الفردي (الافتراضي 5 شموع).
- `--choch-followups on|off` لتفعيل أو تعطيل مراقبة CHOCH حتى مناطق SMC (الافتراضي on).
- `--choch-followup-max-age N` يحدد أكبر عمر بالشموع لمتابعة CHOCH قبل تجاهل الحدث (الافتراضي 5 شموع).
- `--console-max-age N` يحصر عرض أحدث الإشارات في الملخص النصي على N شموع (الافتراضي 5 شموع، واستخدام 0 يلغي القيد).

يُنشئ السكربت تقريرًا موحدًا ويطبع ملخصًا ملوّنًا لكل رمز قبل الانتقال إلى التالي.

## توليد تقرير مطابقة Pullback (OS-PB/1)
لإنشاء تقرير الجرد والمقارنة الخاصة بمنطق الـPullback:
```bash
python smart_money_algo_pro_e5.py --pullback-report --pine-source "Smart Money Algo Pro E5 - CHADBULL.txt" --outfile PULLBACK_REPORT.md
```
يستخلص هذا الأمر الجداول والقوالب الإلزامية من كل من ملف Pine والنسخة البايثونية.

## خيارات إضافية مفيدة
- `--trace` لتفعيل سجل التنفيذ التفصيلي، مع `--trace-file trace.json` لحفظه.
- يتم إظهار التنبيهات الفردية للمناطق (`IDM OB تمت الملامسه`، `Hist EXT OB انشي حديثا`، إلخ) في الملخص اللحظي عند تفعيل خيار `--zone-alerts`.

## ناتج التشغيل
- التقارير تُكتب في ملفات Markdown (`FINAL_REPORT_SMART_MONEY_ANALYSIS.md`، `PULLBACK_REPORT.md`).
- سجل الملخص اللحظي يظهر في سطر الأوامر مع السعر الحالي، التغير اليومي، وآخر الإشارات الهيكلية/المناطق المكتشفة، إضافة إلى جدول "متابعات CHOCH" الذي يوضح وصول السعر إلى مناطق EXT/IDM/GOLDEN خلال النافذة المحددة.

