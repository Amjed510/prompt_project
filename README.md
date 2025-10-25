# 🌐 مولد البرومبتات الاحترافي | Professional Prompt Generator

> أداة متكاملة لإنشاء برومبتات تعليمية احترافية تغطي جميع لغات البرمجة الحديثة، مع دعم كامل للغتين العربية والإنجليزية.

<div align="center">

![Preview](https://user-images.githubusercontent.com/placeholder/prompt-generator-cover.png)

[🎯 جرب المشروع محليًا](#🚀-تشغيل-سريع) •
[🛠️ التخصيص](#⚙️-خيارات-التخصيص) •
[📄 Read in English](#readme-in-english)

</div>

---

## 📋 نظرة عامة

يهدف مشروع **Prompt Project** إلى تسهيل توليد برومبتات تعليمية متقدمة للمدرسين، والمطورين، وصناع المحتوى التقني. تم بناء الصفحة التفاعلية `lab_prompt_generator_advanced.html` لتوليد تعليمات متكاملة لبناء لابات برمجية في دقائق، مع دعم تخصيص كامل للغة، الإطار، المستوى، نمط المخرجات، وتفاصيل السيناريو التعليمي.

### أبرز القدرات
- 🌓 **وضع ليلي/نهاري تلقائي** مع حفظ التفضيل في المتصفح.
- 🧠 **منطق ذكي للتعبئة السريعة** (مع/بدون API) مبني على اللغة المختارة.
- 🧩 **قوالب جاهزة** لتطبيقات الويب، المحمول، الـ API، الذكاء الاصطناعي، الألعاب، وتحليل البيانات.
- 🌍 **دعم شامل للغات وأطر العمل** (30+ لغة، 40+ إطار).
- 📤 **خيارات تصدير** متعددة (نسخ، تنزيل HTML، تنزيل Markdown).
- 📈 **إحصائيات فورية** لعدد الكلمات، الأحرف، والأسطر.
- 🛡️ **إرشادات جودة مدمجة** تشمل الأداء، الأمن، الاختبار، والتوثيق.

---

## 🗂️ جدول المحتويات
1. [🚀 تشغيل سريع](#🚀-تشغيل-سريع)
2. [🛠️ متطلبات النظام](#🛠️-متطلبات-النظام)
3. [⚙️ خيارات التخصيص](#⚙️-خيارات-التخصيص)
4. [🧪 أمثلة وسيناريوهات](#🧪-أمثلة-وسيناريوهات)
5. [🧠 كيف يعمل؟](#🧠-كيف-يعمل)
6. [📦 هيكل المشروع](#📦-هيكل-المشروع)
7. [🧱 التقنيات المستخدمة](#🧱-التقنيات-المستخدمة)
8. [🛣️ خارطة الطريق](#🛣️-خارطة-الطريق)
9. [🤝 المساهمة](#🤝-المساهمة)
10. [📝 الترخيص](#📝-الترخيص)
11. [📄 README in English](#readme-in-english)

---

## 🚀 تشغيل سريع
1. قم بتنزيل/استنساخ المستودع:
   ```bash
   git clone https://github.com/Amjed510/prompt_project.git
   ```
2. افتح الملف الرئيسي مباشرة في المتصفح:
   ```text
   prompt_project/lab_prompt_generator_advanced.html
   ```
3. لا حاجة لأي بناء أو خادم — كل شيء يعمل محليًا (Client-Side Only).

> 💡 **نصيحة:** احتفظ بالنسخة على GitHub Pages أو أي خدمة استضافة ثابتة للوصول السريع.

---

## 🛠️ متطلبات النظام
| ‎المكون‎         | ‎الحد الأدنى‎ | ‎ملاحظة‎ |
|-----------------|--------------|----------|
| المتصفح         | Chrome 90+, Edge 90+, Firefox 88+, Safari 14+ | مطلوب لدعم ES6 و Clipboard API |
| الاتصال بالإنترنت | اختياري      | ضروري فقط لتحميل ملفات الـ CDN (Bootstrap, Font Awesome, Google Fonts) |
| نظام التشغيل    | Windows / macOS / Linux | يعمل بالكامل محليًا |

---

## ⚙️ خيارات التخصيص
يمكن تعديل مظهر وسلوك المولد بسهولة:

1. **تعديل قائمة اللغات** — من داخل `<select id="programmingLanguage">`.
2. **إضافة قالب جديد** — تحديث دالة `selectTemplate(templateType)` في JavaScript.
3. **تحرير منطق التوليد** — تعديل دالة `generateAdvancedPrompt(data)` لإضافة أقسام جديدة.
4. **إضافة تنبيهات مخصصة** — استخدام الدالة `showAlert(message, type)`.

```javascript
// مثال لإضافة قالب جديد
case 'desktop-app':
    document.getElementById('programmingLanguage').value = 'C#';
    document.getElementById('framework').value = 'WPF';
    // ... باقي الحقول
    break;
```

---

## 🧪 أمثلة وسيناريوهات
| السيناريو | زر التعبئة السريعة | الناتج المتوقع |
|-----------|--------------------|----------------|
| تطبيق ويب بـ React | "بدون API" | نموذج تعليمي مع بيانات Local Storage |
| RESTful API بـ FastAPI | "مع API" | برومبت يغطي PostgreSQL + CRUD + Auth |
| مشروع Flutter للموبايل | قالب "تطبيق موبايل" | يخّصص البيانات للمنصة المحمولة |
| مختبر ذكاء اصطناعي | قالب "ذكاء اصطناعي" | يفعّل مكتبات TensorFlow & Pandas |

---

## 🧠 كيف يعمل
1. **جمع المدخلات**: قراءة القيم من النموذج (لغة، إطار، مستوى، ...).
2. **التحقق**: التأكد من الحقول الضرورية وصحة JSON.
3. **التخصيص**: بناء كائن `data` موحد ثم تمريره إلى `generateAdvancedPrompt`.
4. **التوليد**: دمج القيم ضمن قالب Markdown احترافي كامل.
5. **العرض والتصدير**: إظهار النص داخل واجهة مهيأة مع خيارات النسخ والحفظ.

```mermaid
graph TD;
    A[User Inputs] --> B[Validation];
    B --> C{API or Local?};
    C -->|API| D[prefillWithApi];
    C -->|Local| E[prefillWithoutApi];
    D --> F[generateAdvancedPrompt];
    E --> F;
    F --> G[displayOutput];
    G --> H{Copy \| Download \| Share};
```

---

## 📦 هيكل المشروع
```text
prompt_project/
├── lab_prompt_generator_advanced.html   # الواجهة الرئيسية
├── README.md                            # هذا الملف
├── README_ADVANCED.md                   # توثيق تفصيلي للنسخة السابقة
└── bootstrap-4.0.0-dist/                # أرشيف (غير مستخدم حاليًا)
```

---

## 🧱 التقنيات المستخدمة
- **HTML5 / CSS3 / ES6+** — البنية الأساسية.
- **Bootstrap 5 CDN** — تصميم سريع ومتجاوب.
- **Font Awesome 6 CDN** — مكتبة الأيقونات.
- **Animate.css CDN** — حركات انتقالية سلسة.
- **LocalStorage API** — حفظ تفضيلات الوضع الليلي/النهاري.

---

## 🛣️ خارطة الطريق
- [x] الوضع الليلي/النهاري مع حفظ التفضيل.
- [x] القوالب الجاهزة للمشاريع المتنوعة.
- [ ] نظام حفظ التاريخ واسترجاع البرومبتات.
- [ ] دعم التصدير إلى PDF و Markdown.
- [ ] تحويل التطبيق إلى PWA للعمل بدون اتصال.

> 🗳️ **شارك رأيك:** افتح Issue جديد لاقتراح ميزات أو تحسين تجربة المستخدم.

---

## 🤝 المساهمة
1. قم بعمل Fork للمستودع.
2. أنشئ فرعًا جديدًا:
   ```bash
   git checkout -b feature/awesome-feature
   ```
3. ادفع التغييرات مع رسالة واضحة:
   ```bash
   git commit -m "Add awesome feature"
   git push origin feature/awesome-feature
   ```
4. افتح Pull Request ووضح التغييرات.

> **إرشاد:** التزم بأسلوب الكود الحالي وحافظ على التعليقات العربية التوضيحية.

---

## 📝 الترخيص
هذا المشروع متاح للاستخدام التعليمي والتجاري بلا قيود. يُرجى الإشارة إلى المصدر عند إعادة التوزيع.

---

## README in English

### Overview
The **Professional Prompt Generator** is a standalone HTML tool that helps educators and developers craft rich, structured lab prompts covering modern programming languages and frameworks. It supports smart autofill, ready-made templates, dark/light themes, and export utilities.

### Quick Start
1. Clone the repo: `git clone https://github.com/Amjed510/prompt_project.git`
2. Open `lab_prompt_generator_advanced.html` in any modern browser.
3. Fill in the form, choose a template, and click “Generate Advanced Prompt”.
4. Copy, download, or share the generated prompt straight away.

### Key Features
- Smart presets (with/without API) tailored per language.
- Ready-made project templates (Web, Mobile, API, AI/ML, Games, Data Analysis).
- Real-time stats & quality guidelines embedded in the output.
- Extended language/framework catalog (30+ languages, 40+ frameworks).
- Dark/Light mode with preference persisted in LocalStorage.

### Tech Stack
- HTML5, CSS3, Vanilla JS (ES6+)
- Bootstrap 5, Font Awesome 6, Animate.css (all via CDN)

### Roadmap Highlights
- Prompt history & auto-save
- Export to PDF/Markdown
- Progressive Web App

### Contributing
Feel free to fork, create feature branches, and open pull requests. Contributions in both Arabic and English documentation are welcome.

---

<div align="center">

تم بناء المشروع بحب ❤️ لدعم المحتوى العربي البرمجي.

</div>
