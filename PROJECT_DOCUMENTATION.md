# 🏢 نظام Smart Mall CRM - التوثيق الشامل

## 📋 نظرة عامة على المشروع

### 🎯 الوصف
نظام إدارة علاقات العملاء المخصص للمولات والمراكز التجارية، مطور باستخدام Flutter مع دعم كامل للغة العربية ومميزات متقدمة لإدارة المستأجرين والوحدات التجارية وأنظمة الصيانة.

### 🚀 المميزات الرئيسية
- **🔐 نظام مصادقة آمن** مع JWT وتشفير البيانات
- **👥 إدارة المستخدمين** بأدوار وصلاحيات متعددة
- **🏪 إدارة الوحدات التجارية** مع تتبع شامل
- **🔧 نظام طلبات الصيانة** المتقدم
- **📊 تقارير وتحليلات** في الوقت الفعلي
- **📱 واجهة محمولة** متجاوبة وحديثة
- **🌐 دعم اللغة العربية** كامل مع RTL
- **🎨 تصميم Material Design** عصري

## 🛠 التقنيات المستخدمة

### Frontend (Mobile App)
```yaml
Framework: Flutter 3.24.3
Language: Dart 3.5.3
UI Kit: Material Design 3
State Management: Provider
Localization: flutter_localizations
```

### المكتبات الأساسية
```yaml
HTTP Client: dio ^5.9.0
Storage: shared_preferences ^2.5.3
Charts: fl_chart ^0.68.0, syncfusion_flutter_charts ^29.1.38
UI Components: flutter_spinkit, shimmer, lottie
Icons: feather_icons ^1.2.0
Image Handling: cached_network_image, image_picker
PDF Generation: pdf ^3.11.3, printing ^5.14.2
QR Code: qr_flutter, qr_code_scanner
```

## 📁 هيكل المشروع

```
smart_mall_crm_app/
├── lib/
│   ├── main.dart                 # نقطة البداية
│   ├── models/                   # نماذج البيانات
│   │   ├── user_model.dart
│   │   └── user_model.g.dart
│   ├── screens/                  # شاشات التطبيق
│   │   ├── splash_screen.dart
│   │   ├── login_screen.dart
│   │   ├── dashboard_screen.dart
│   │   ├── tenants_screen.dart
│   │   ├── units_screen.dart
│   │   ├── maintenance_screen.dart
│   │   └── reports_screen.dart
│   ├── services/                 # خدمات التطبيق
│   │   └── auth_service.dart
│   ├── widgets/                  # المكونات المعاد استخدامها
│   │   ├── custom_button.dart
│   │   ├── custom_text_field.dart
│   │   └── loading_overlay.dart
│   ├── utils/                    # الأدوات المساعدة
│   │   ├── app_constants.dart
│   │   └── theme.dart
│   └── providers/                # إدارة الحالة
├── assets/                       # الموارد
│   ├── images/
│   ├── icons/
│   ├── animations/
│   └── fonts/
├── android/                      # إعدادات Android
├── ios/                          # إعدادات iOS
└── pubspec.yaml                  # تبعيات المشروع
```

## 🎨 التصميم والمظهر

### الألوان الأساسية
```dart
Primary Color: #2E3B42 (رمادي داكن)
Secondary Color: #3498DB (أزرق)
Accent Color: #E74C3C (أحمر)
Success Color: #27AE60 (أخضر)
Warning Color: #F39C12 (برتقالي)
Error Color: #E74C3C (أحمر)
```

### الخطوط
- **Arabic**: Cairo (Regular, Bold)
- **English**: Roboto (Regular, Bold)

### دعم RTL
- دعم كامل للغة العربية
- تخطيط من اليمين إلى اليسار
- نصوص وتسميات عربية شاملة

## 🔐 نظام المصادقة والأمان

### مميزات الأمان
- **JWT Authentication**: نظام رمز مميز آمن
- **Password Encryption**: تشفير كلمات المرور
- **Session Management**: إدارة جلسات المستخدمين
- **Role-based Access**: التحكم بالوصول حسب الأدوار
- **Data Validation**: التحقق من صحة البيانات

### أدوار المستخدمين
```dart
admin: مدير النظام - صلاحيات كاملة
manager: مدير - صلاحيات إدارية
employee: موظف - صلاحيات محدودة
tenant: مستأجر - عرض البيانات الخاصة
maintenance: فني صيانة - إدارة الصيانة
```

## 📱 الشاشات والوظائف

### 1. شاشة البداية (Splash Screen)
- **الوظيفة**: عرض شعار التطبيق وفحص حالة المصادقة
- **المميزات**: رسوم متحركة، انتقال تلقائي
- **المدة**: 3 ثوانٍ

### 2. شاشة تسجيل الدخول
- **الحقول**: البريد الإلكتروني، كلمة المرور
- **المميزات**: تذكر البيانات، نسيان كلمة المرور
- **التحقق**: validation شامل للبيانات
- **دخول تجريبي**: admin@smartmall.com / admin123

### 3. لوحة المعلومات
- **الإحصائيات**: عرض البيانات الأساسية
- **الرسوم البيانية**: تحليلات بصرية
- **الاشعارات**: تنبيهات مهمة
- **الوصول السريع**: اختصارات للوظائف

### 4. إدارة المستأجرين
- **قائمة المستأجرين**: عرض وبحث
- **إضافة مستأجر**: نموذج شامل
- **تحديث البيانات**: تعديل المعلومات
- **تتبع العقود**: حالة الإيجار

### 5. إدارة الوحدات التجارية
- **خريطة المول**: عرض بصري للوحدات
- **تفاصيل الوحدة**: معلومات شاملة
- **الحالات**: متاح، مؤجر، تحت الصيانة
- **التسعير**: إدارة الأسعار

### 6. نظام الصيانة
- **طلبات الصيانة**: إنشاء وتتبع
- **الأولويات**: عادي، عالي، عاجل
- **تعيين الفنيين**: إدارة المهام
- **التقارير**: إحصائيات الصيانة

### 7. التقارير والتحليلات
- **تقارير مالية**: الإيرادات والمصروفات
- **تقارير الإشغال**: نسب الإشغال
- **تقارير الصيانة**: أداء الصيانة
- **التصدير**: PDF, Excel, CSV

## 🔧 التطوير والبناء

### متطلبات النظام
```bash
Flutter SDK: 3.24.3+
Dart SDK: 3.5.3+
Android Studio: Latest
VS Code: مع امتداد Flutter
```

### خطوات التثبيت
```bash
# 1. استنساخ المشروع
git clone <repository-url>
cd smart_mall_crm_app

# 2. تثبيت التبعيات
flutter pub get

# 3. إنشاء ملفات التسلسل
flutter pub run build_runner build

# 4. تشغيل التطبيق
flutter run
```

### بناء APK للإنتاج
```bash
# Debug APK
flutter build apk --debug

# Release APK
flutter build apk --release

# Bundle للنشر
flutter build appbundle --release
```

### بناء iOS
```bash
# iOS Debug
flutter build ios --debug

# iOS Release
flutter build ios --release
```

## 🌐 API والاتصال

### Base URL
```dart
const String baseUrl = 'https://api.smartmall.com';
const String apiVersion = '/api/v1';
```

### Endpoints الأساسية
```dart
POST /auth/login        # تسجيل الدخول
POST /auth/register     # التسجيل
GET  /auth/profile      # بيانات المستخدم
POST /auth/logout       # تسجيل الخروج

GET  /tenants          # قائمة المستأجرين
POST /tenants          # إضافة مستأجر
PUT  /tenants/:id      # تحديث مستأجر
DELETE /tenants/:id    # حذف مستأجر

GET  /units            # قائمة الوحدات
POST /units            # إضافة وحدة
PUT  /units/:id        # تحديث وحدة

GET  /maintenance      # طلبات الصيانة
POST /maintenance      # إنشاء طلب صيانة
PUT  /maintenance/:id  # تحديث طلب

GET  /reports          # التقارير
GET  /reports/export   # تصدير التقارير
```

### إعدادات HTTP
```dart
Connection Timeout: 30 seconds
Receive Timeout: 30 seconds
Send Timeout: 30 seconds
Retry Policy: 3 attempts
```

## 📊 قاعدة البيانات

### جداول رئيسية
```sql
users: معلومات المستخدمين
tenants: بيانات المستأجرين
units: الوحدات التجارية
leases: عقود الإيجار
maintenance_requests: طلبات الصيانة
payments: المدفوعات
reports: التقارير المحفوظة
```

### العلاقات
- User → Tenant (One to Many)
- Tenant → Unit (One to Many)
- Unit → Maintenance (One to Many)
- Tenant → Payment (One to Many)

## 🚀 النشر والتوزيع

### Android Play Store
1. **التوقيع**: إنشاء keystore
2. **البناء**: flutter build appbundle --release
3. **الاختبار**: اختبار شامل
4. **الرفع**: Google Play Console

### iOS App Store
1. **الشهادات**: iOS Distribution Certificate
2. **البناء**: flutter build ios --release
3. **الأرشفة**: Xcode Archive
4. **الرفع**: App Store Connect

### التحديثات التلقائية
- **OTA Updates**: التحديثات عبر الهواء
- **Hot Reload**: للتطوير السريع
- **Version Control**: إدارة الإصدارات

## 🔍 الاختبار وضمان الجودة

### أنواع الاختبارات
```dart
Unit Tests: اختبار الوحدات
Widget Tests: اختبار المكونات
Integration Tests: اختبار التكامل
Performance Tests: اختبار الأداء
```

### أدوات الاختبار
```yaml
flutter_test: الإطار الأساسي
mockito: محاكاة الخدمات
integration_test: اختبار التكامل
```

### تشغيل الاختبارات
```bash
# اختبار الوحدات
flutter test

# اختبار التكامل
flutter test integration_test/

# تغطية الكود
flutter test --coverage
```

## 📈 الأداء والتحسين

### تحسينات الأداء
- **Lazy Loading**: تحميل البيانات حسب الحاجة
- **Caching**: تخزين مؤقت للبيانات
- **Image Optimization**: ضغط الصور
- **Code Splitting**: تقسيم الكود

### مراقبة الأداء
- **Memory Usage**: استخدام الذاكرة
- **CPU Usage**: استخدام المعالج
- **Network Calls**: مكالمات الشبكة
- **Battery Usage**: استهلاك البطارية

## 🔄 صيانة وتحديث المشروع

### التحديثات الدورية
- **Flutter SDK**: تحديث الإطار
- **Dependencies**: تحديث المكتبات
- **Security Patches**: التحديثات الأمنية
- **Feature Updates**: مميزات جديدة

### النسخ الاحتياطية
- **Code Repository**: Git backup
- **Database Backup**: نسخ قاعدة البيانات
- **Asset Backup**: نسخ الموارد
- **Configuration Backup**: نسخ الإعدادات

## 📞 الدعم والمساعدة

### المطور
- **الاسم**: Smart Mall CRM Team
- **البريد**: support@smartmall.com
- **الموقع**: https://smartmall.com
- **التوثيق**: https://docs.smartmall.com

### المساهمة
- **GitHub**: Repository للمساهمات
- **Issues**: تتبع المشاكل
- **Pull Requests**: طلبات الدمج
- **Code Review**: مراجعة الكود

## 📄 الترخيص والحقوق

```
© 2024 Smart Mall CRM System
جميع الحقوق محفوظة

هذا المشروع مطور لأغراض تعليمية وتجارية
يمكن استخدامه وتعديله حسب الحاجة
```

---

## 🎉 خلاصة المشروع

تم تطوير نظام Smart Mall CRM كحل شامل ومتكامل لإدارة المولات والمراكز التجارية. يوفر النظام:

✅ **واجهة مستخدم حديثة** مع دعم كامل للعربية
✅ **نظام أمان متقدم** مع أدوار متعددة
✅ **إدارة شاملة** للمستأجرين والوحدات
✅ **نظام صيانة متطور** مع تتبع كامل
✅ **تقارير وتحليلات** في الوقت الفعلي
✅ **كود نظيف ومنظم** قابل للتطوير
✅ **توثيق شامل** لجميع المكونات
✅ **جاهز للنشر** على المتاجر الرقمية

النظام جاهز للاستخدام الفوري أو التطوير المستقبلي حسب الاحتياجات المحددة! 🚀