المشروع نظام معلومات لمركز طبي يربط قاعدة بيانات مصممة كويس (ERD، علاقات، وصف جداول) مع واجهات مستخدم مبنية بـ Oracle Forms. الهدف إدارة بيانات المرضى، الأطباء، الأقسام، المواعيد، السجلات الطبية، والفحوصات… مع شاشة دخول وإدارة صلاحيات (ADMIN/HOME/LOG_IN/LOGOUT).

المكوّنات الرئيسية (من الـ ERD والملفات)

استخرجت نصوص المخططين (ERD + Mapping) وطلعت معاي أهم الكيانات والحقول، ومن أبرزها:

patients (المرضى): patient_id, Name, Birth_Date, Address, phone, Email

doctors (الأطباء): Doctor_id, Name, speciality, phone, Email

departments (الأقسام): Dep_ID, Dpe_Name

appointments (المواعيد): Appointment_ID, Date, Time, patient_id, Doctor_id, Dep_ID

medical_record (السجلات الطبية): record_id, record_date, diagnosis, treatment, patient_id

tests / test_result (الفحوصات): test_id, test_type, result

nurse (التمريض): nurse_code, nurse

بالإضافة لعناصر “Belong/Assist/Belong to” اللي توضح العلاقات (مَن يتبع مَن، ومَن يساعد مَن)

تقدر تطّلع على قوائم التسميات اللي استخرجتها:

تحميل معاينة نصوص ERD

تحميل معاينة نصوص Mapping

كيف يشتغل النظام (تدفّق بسيط)

تسجيل الدخول: شاشة LOG_IN → بعدها تنتقل إلى HOME

الإدارة (ADMIN): إضافة/تعديل/حذف كيانات أساسية: مرضى، أطباء، أقسام، ممرضين…

المواعيد: ربط مريض بدكتور في قسم وتاريخ/وقت محدد

السجل الطبي: إدخال/تحديث التشخيصات والعلاجات ونتائج الفحوصات

خروج آمن: شاشة LOGOUT لإغلاق الجلسة

التقنية المستخدمة

Oracle Database + PL/SQL (منطق الإجراءات/الدوال/التريجرز متوقع داخل الداتابيس)

Oracle Forms/Modules لواجهات المستخدم (.fmb المصدر و.fmx تنفيذ)

مستندات توثيق بالعربي لشرح المتطلبات والجداول

ERD/Mapping بصيغة draw.io (موثّق بنية الداتابيس وعلاقاتها)
