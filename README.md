# مهارة الكتابة العربية الفصيحة ونبذ العَرَنْجِيَّة
### (Anti-Aranjiya Arabic Writing Skill)

**Arabic writing skill for AI agents** — strips English calques and translated phraseology (العَرَنْجِيَّة) from Arabic text: `قام بزيارة` → `زار`, `تم التوقيع بواسطة` → `وقّع`. Works with Claude Code, Codex, Antigravity and VS Code agent harnesses.

🔗 **الموقع المرجعي (المعجم والتراكيب والنماذج): [specailm5.github.io/anti-aranjiya-skill](https://specailm5.github.io/anti-aranjiya-skill/)**

> مهارة برمجية ولغوية احترافية لنماذج الذكاء الاصطناعي والمحررات الذكية (Codex، Claude Code، Antigravity IDE، VS Code Agent Harness) لتدقيق النصوص والترجمات العربية وتخليصها من **«العَرَنْجِيَّة»** (الأساليب والتراكيب الإفرنجية المترجمة حرفياً)، استناداً إلى كتاب **«العَرَنْجِيَّة: بلغات أعجمية وألسن عربية»** للترجمان **أحمد الغامدي**.

---

## 📖 ما هي المهارة؟

**العَرَنْجِيَّة** (نحتٌ من: *عربية + إفرنجية*) هي التعبير عن الأفكار والتراكيب الغربية بألفاظ عربية؛ فتكون الجملة مستقيمة الإعراب ظاهراً، لكنها إفرنجيةٌ في جوهرها وبنائها ورصف ألفاظها (مثل: كثرة الأفعال المساعدة `قام بزيارة` بدلاً من `زار`، والمبني للمجهول المرفوق بالفاعل `تم التوقيع بواسطة فلان` بدلاً من `وقّع فلان`، والتكلف في أدوات الربط مثل `حيث أن`، `من خلال`، `على صعيد`).

هذه المهارة تُمكِّن الوكيل الذكي (AI Agent) من كتابة وتدقيق النصوص العربية على سَنَن كلام العرب الفصحاء، وحفظ لسان الكاتب والمترجم من العجمة الهجينة المعاصرة.

---

## 📂 بنية المهارة ومكوناتها

```
arabic_writing_skill/
│
├── SKILL.md                              # الدليل الأساسي للمهارة (الأصول والأوامر والنواهي)
│
├── references/
│   ├── vocabulary_and_idioms.md          # معجم الألفاظ والتعابير العرنجية وبدائلها الفصيحة
│   └── stylistic_patterns.md             # سجل التحويلات الأسلوبية والنحوية المتقدمة
│
├── examples/
│   └── before_after_texts.md             # نماذج تطبيقية كاملة (سياسية، إدارية، أدبية) قبل وبعد التحوير
│
├── aranjiya.pdf                          # نسخة كتاب «العرنجية» الأصلية (المصدر المرجعي)
└── aranjiya_text.txt                     # النص الكامل المستخرج للبحث والرجوع
```

---

## 🚀 طرق التثبيت والاستخدام (Installation Guide)

يمكن تثبيت المهارة إما **محلياً** على مستوى مشروع معين، أو **عاماً (Global)** لتعمل في كافة المشاريع تلقائياً.

---

### أولاً: التثبيت العام لبيئة Claude Code و Codex و Antigravity (موصى به)

لتفعيل المهارة في كل مشروعاتك دون الحاجة لتكرار تثبيتها في كل مجلد:

#### لنظام Windows (PowerShell):
```powershell
# 1. تثبيت لبيئة Claude Code
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.claude\skills\anti-aranjiya-arabic-writing"
Copy-Item -Recurse -Force "SKILL.md", "references", "examples" "$env:USERPROFILE\.claude\skills\anti-aranjiya-arabic-writing\"

# 2. تثبيت لبيئة Codex و Agent Skills العامة
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.agents\skills\anti-aranjiya-arabic-writing"
Copy-Item -Recurse -Force "SKILL.md", "references", "examples" "$env:USERPROFILE\.agents\skills\anti-aranjiya-arabic-writing\"

# 3. تثبيت لبيئة Google Antigravity / Gemini
New-Item -ItemType Directory -Force -Path "$env:USERPROFILE\.gemini\config\skills\anti-aranjiya-arabic-writing"
Copy-Item -Recurse -Force "SKILL.md", "references", "examples" "$env:USERPROFILE\.gemini\config\skills\anti-aranjiya-arabic-writing\"
```

#### لنظام macOS / Linux (Bash):
```bash
# 1. لبيئة Claude Code
mkdir -p ~/.claude/skills/anti-aranjiya-arabic-writing
cp -r SKILL.md references examples ~/.claude/skills/anti-aranjiya-arabic-writing/

# 2. لبيئة Codex و Agent Harness
mkdir -p ~/.agents/skills/anti-aranjiya-arabic-writing
cp -r SKILL.md references examples ~/.agents/skills/anti-aranjiya-arabic-writing/

# 3. لبيئة Antigravity / Gemini
mkdir -p ~/.gemini/config/skills/anti-aranjiya-arabic-writing
cp -r SKILL.md references examples ~/.gemini/config/skills/anti-aranjiya-arabic-writing/
```

---

### ثانياً: التثبيت المحلي داخل مشروع محدد (VS Code Workspace Harness)

إذا أردت حصر المهارة داخل مستودع أو مجلد عمل واحد في VS Code:

1. انسخ مجلد المهارة داخل مجلد `.agents/skills/` أو `.claude/skills/` في جذر مشروعك:
```powershell
# داخل مجلد مشروعك الحالي:
New-Item -ItemType Directory -Force -Path ".agents\skills\anti-aranjiya-arabic-writing"
Copy-Item -Recurse -Force "path\to\SKILL.md", "path\to\references", "path\to\examples" ".agents\skills\anti-aranjiya-arabic-writing\"
```

2. بمجرد فتح المشروع في **VS Code** أو تشغيل `Claude Code` / `Codex`، سيتم اكتشاف المهارة وقراءتها تلقائياً عند صياغة أي نص أو كود باللغة العربية.

---

### ثالثاً: الاستخدام اليدوي (Direct System Prompt / Custom Instructions)

إذا كنت تستخدم واجهات الويب (مثل ChatGPT أو Claude أو Gemini) مباشرة دون بيئة برمجية:
* افتح ملف [`SKILL.md`](SKILL.md) وانسخ محتواه وضعه في خانة **التعليمات المخصصة (Custom Instructions)** أو **System Prompt**.

---

## ⚡ كيف تعمل المهارة؟ (أوامر ونواهٍ سريعة)

| الأسلوب العرنجي الهجين ❌ | الصواب العربي الفصيح الأصيل ✅ | التوجيه اللغوي |
| :--- | :--- | :--- |
| **قام بزيارة** الطبيب | **زار** الطبيب | الاشتقاق المباشر ونبذ الأفعال المساعدة. |
| كُتِبَ التقرير **من قبل** فلان | **كتب** فلانٌ التقريرَ | امتناع المبني للمجهول إذا عُلِمَ الفاعل. |
| سافر **من أجل** طلب العلم | سافر **طلباً** للعلم | إحياء المفعول لأجله الصريح. |
| اعتذر **حيث أن** سيارته تعطلت | اعتذر **لأنّ** سيارته تعطلت (أو **إذ**) | "حيث" ظرف مكان ولا يليها "أنّ". |
| أريد هذا **فقط** | **ما أريد إلا هذا** / **إنما أريد هذا** | أسلوب الحصر والقصر بدلاً من رمي "فقط" آخراً. |
| كان الموقف **الأكثر صعوبة** | كان الموقف **أصعبَ** المواقف | صيغة أفعل التفضيل المباشرة. |
| **لعب دوراً محورياً** في الحادث | **كان قطب الرحى** / **كان له أثرٌ عظيم** | استعارة مسرحية مستوردة تقابلها أصالة البيان. |
| **تبنّى** الفكرة، و**عكس** واقعه | **استحسن** الفكرة، و**أبان عن** واقعه | التبني للولد، والعكس للقلب والرد. |

---

## 📚 المراجع والاعتماد

* كتاب **«العَرَنْجِيَّة: بلغات أعجمية وألسن عربية»**، للترجمان **أحمد الغامدي** (الطبعة الثانية 1445هـ / 2023م).
* نصوص وشواهد الأوائل (الجاحظ في «البيان والتبيين» و«البخلاء»، القاسم بن سلام في «الأموال»، نهج البلاغة، صحيح البخاري).

---

## 📜 الترخيص (License)
هذه المهارة مفتوحة المصدر ومتاحة للاستخدام الشخصي والتجاري والبحثي لدعم وتعزيز الفصاحة والبيان في الذكاء الاصطناعي.
