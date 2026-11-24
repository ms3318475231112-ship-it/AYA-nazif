# تسعير الدهان: تحويل لتطبيق أندرويد عن طريق GitHub

## محتوى الحزمة
- www/index.html : البرنامج
- assets/ : صور الأيقونة (اللوجو)
- package.json و capacitor.config.json : إعدادات التطبيق
- build-apk.yml : ملف بناء الـ APK (لازم يتحط في مكان خاص، شوف الخطوة 6)

## الخطوات
1. سجل دخول على github.com.
2. اضغط علامة + فوق على اليمين > New repository.
3. الاسم: paint-pricing. اختار Public. متعلمش على أي خيار تاني. اضغط Create repository.
4. فك ضغط paint-app.zip. ارفع اللي جواه من رابط "uploading an existing file":
   - مجلد www
   - مجلد assets
   - ملف package.json
   - ملف capacitor.config.json
   اضغط Commit changes.
5. اتأكد إن في المستودع: www/index.html و assets (3 صور) و package.json و capacitor.config.json.
6. ملف البناء: اضغط Add file > Create new file. في خانة الاسم اكتب بالظبط:
   .github/workflows/build-apk.yml
   (لما تكتب / هيعمل المجلدات لوحده). افتح build-apk.yml من الحزمة بالنوت باد، انسخ كل محتواه والصقه في المربع الكبير. اضغط Commit changes.
7. افتح تبويب Actions. هتلاقي Build Android APK شغال. لو مبدأش: اختاره من الشمال > Run workflow.
8. استنى 5 لـ 10 دقايق لحد علامة ✓ خضراء.
9. افتح العملية > Artifacts > نزل paint-pricing-apk > فك الضغط > app-debug.apk.
10. ابعته للموبايل وثبته (اسمح بالتثبيت من مصادر غير معروفة).

لو ظهرت علامة ✗ حمراء: افتح العملية، اضغط على الخطوة اللي جنبها ✗ وابعت صورة الخطأ.
