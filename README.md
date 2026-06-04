# مدبر البيت - تطبيق فواتير ومقاضي ومهام العائلة

## المزايا
- تسجيل دخول وخروج.
- حساب رئيسي وحسابات ثانوية.
- صلاحيات: الميزانية تظهر للحساب الرئيسي فقط.
- فواتير: كهرباء، ماء، إنترنت، غاز، إيجار وغيرها.
- قائمة مقاضي اعتيادية مع صور وأسعار تقريبية من/إلى.
- مقارنة أرخص نوع داخل نفس المجموعة.
- قائمة شراء.
- مهام عائلية مع اختيار أصناف من قائمة المقاضي.
- مصاريف فعلية.
- تقارير شهرية للمصاريف.
- جاهز للاستضافة على Firebase Hosting أو Vercel.

## تشغيل Firebase
1. أنشئ مشروع Firebase.
2. فعّل Authentication > Email/Password.
3. أنشئ Cloud Firestore.
4. انسخ إعدادات تطبيق الويب من Firebase وضعها في `index.html` مكان:
   `firebaseConfig`.
5. انسخ محتوى `firestore.rules` إلى Firestore Rules وانشرها.
6. ارفع الملفات:
   - index.html
   - manifest.json
   - sw.js
   - icon.svg

## تشغيل على Vercel
ارفع الملفات في GitHub ثم اربط المستودع مع Vercel.
لا تحتاج Build Command.
Output Directory اتركه فارغ أو root.

## تشغيل على Firebase Hosting
```bash
npm install -g firebase-tools
firebase login
firebase init hosting
firebase deploy
```

## ملاحظة
الصور حالياً تحفظ كـ Base64 داخل Firestore، وهذا مناسب للصور الصغيرة فقط.
للتطبيق التجاري الأفضل استخدام Firebase Storage للصور.
