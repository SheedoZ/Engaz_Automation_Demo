# دليل Engaz Automation Demo

آخر مراجعة: 2026-08-12

## 1. الهدف

عرض تجريبي Static لمسار استقبال وتصنيف ومتابعة Leads. الأسماء والأرقام والرسائل والمؤشرات كلها صناعية.

## 2. النسخة الرسمية والتشغيل

- المستودع: `SheedoZ/Engaz_Automation_Demo`
- الفرع: `main`
- المسار المحلي: `D:\Projects\Engaz-Automation-Demo`
- الإنتاج: `https://automation.engaz.premiumpower-eg.com/` عبر GitHub Pages.

## 3. تركيب الملفات

- `index.html`: الواجهة والـfixtures والمنطق التجريبي.
- `v2-core.js`: وظائف الواجهة المشتركة.
- `v2-theme.css`: التصميم.
- `CNAME`, `.nojekyll`: إعداد Pages.
- `.github/workflows/validate.yml`: فحص syntax والخصوصية والروابط والملفات.
- `README.md` و`PROJECT_GUIDE.md`: التعليمات.

## 4. طريقة التعديل

أنشئ فرعًا من `main`. حافظ على البيانات الوهمية والتحذير الواضح، ولا تضف اتصالًا خارجيًا أو تخزينًا. اختبر محليًا، ثم افتح Pull Request وانتظر نجاح `Static safety`.

## 5. اختبار صغير

```powershell
node --check v2-core.js
git diff --check
```

افتح `index.html` وجرّب Run وReset والفلاتر ومراجعة lead وإضافة lead وهمي. لا تدخل بيانات عميل حقيقية.

## 6. النشر والرجوع

الدمج في `main` يعيد نشر GitHub Pages تلقائيًا. راجع النطاق بعد نجاح Pages. للرجوع استخدم `git revert` وادمج التراجع.

## 7. حدود الأمان

لا إرسال رسائل حقيقي ولا backend ولا قاعدة بيانات ولا persistence. `noindex,nofollow` مقصود. أي بيانات عميل أو credentials ممنوعة.
