## عنوان المشروع 
مشروع تصنيف التشخيص الطبي
الهدف من هذا المشروع هو بناء نماذج تعلم آلي لتصنيف نتيجة تشخيص طبي (مثل وجود مرض معين أو عدمه) بناءً على بيانات تحتوي على معلومات عن المرضى ونتائج طبية أولية.
## وصف البيانات 
البيانات المستخدمة تتضمن أعمدة مثل:

ID, Patient Age, Patient Sex: معلومات تعريفية وأساسية عن المريض.

Left-Fundus, Right-Fundus: روابط أو مسارات لصور الشبكية (لم يتم استخدامها في هذا النموذج).

Left-Diagnostic Keywords, Right-Diagnostic Keywords: كلمات مفتاحية تصف نتائج التشخيص.

أعمدة طبية مثل: N, D, G, C, A, H, M, O: تمثل خصائص أو ملاحظات طبية.

filepath, filename: مسارات الصور (تم تجاهلها في النماذج).

labels, target: المتغير الهدف (المتغير الذي نحاول التنبؤ به).
## معالجة البيانات 
التعامل مع القيم الفارغة (NaNs): تم استخدام SimpleImputer بتقنية المتوسط لملء القيم الناقصة.

تقييس البيانات (Standardization): تم استخدام StandardScaler لجعل القيم ذات توزيعات طبيعية لتناسب النماذج.

اختيار الأعمدة المفيدة: تم استبعاد الأعمدة غير المهمة مثل ID, filepath, filename.
## النماذج المستخدمة 
تم تدريب ثلاثة نماذج ومقارنتها:

1.اSVM (داعم المتجهات)

2.اSGD (الانحدار التدرجي العشوائي)

3.الانحدار اللوجستي (Logistic Regression)
## تقييم الأداء 
![Capture](https://github.com/user-attachments/assets/6c99cbd6-9637-4d33-95d2-51d900e2c5a9)

## الأدواة و المكتبات المستخدمة 

مكتبات:

Pandas, NumPy: لمعالجة البيانات.

Matplotlib, Seaborn: للرسم البياني والتحليل البصري.

Scikit-learn: لبناء النماذج والتقييم.

## الإستنتاج 
جميع النماذج أعطت نتائج متقاربة.

نموذج Logistic Regression أعطى أفضل دقة بشكل بسيط.

المشروع يثبت إمكانية بناء نموذج تصنيفي فعال باستخدام بيانات طبية منظمة.

