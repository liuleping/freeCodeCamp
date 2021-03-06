---
title: Packets
localeTitle: الحزم
---
## الحزم

الحزمة هي وحدة أساسية للاتصال عبر شبكة رقمية. وتسمى الحزمة أيضًا **مخطط بيانات أو مقطعًا أو كتلة أو خلية أو إطارًا ،** وفقًا للبروتوكول المستخدم لإرسال البيانات. عندما يتم نقل البيانات ، يتم تقسيمها إلى بنية مشابهة للبيانات قبل الإرسال ، تسمى الحزم ، والتي يتم إعادة تجميعها إلى مقطع البيانات الأصلي بمجرد وصولها إلى وجهتها.

عادة ما تكون شبكات تبديل الرزم أكثر كفاءة مقارنة بالشبكات بتبديل الدارات. تحتاج الشبكة بتبديل الدارة إلى حجز الموارد طوال مدة الاتصال. يمكن لشبكات حزم التبديل إرسال الحزم حسب الطلب.

في نموذج OSI ، تتوافق الحزم مع الطبقة 3 ، طبقة الشبكة.

## هيكل حزمة البيانات

يعتمد هيكل الحزمة على نوع الحزمة الموجودة على البروتوكول. قراءة المزيد أدناه على الحزم والبروتوكولات. عادة ، تحتوي الحزمة على رأس وحمولة.

يحتفظ الرأس بمعلومات عامة حول الحزمة والخدمة وغيرها من البيانات المتعلقة بالإرسال. على سبيل المثال ، يتطلب نقل البيانات عبر الإنترنت تقسيم البيانات إلى رزم IP ، والتي يتم تحديدها في بروتوكول الإنترنت (IP) ، وتتضمن رزمة IP ما يلي:

*   عنوان IP المصدر ، وهو عنوان IP الخاص بالجهاز الذي يرسل البيانات.
*   عنوان IP للوجهة ، وهو الجهاز أو الجهاز الذي يتم إرسال البيانات إليه.
*   رقم التسلسل الخاص بالحزم ، وهو رقم يضع الحزم بالترتيب بحيث يتم إعادة تجميعها بطريقة تجعل البيانات الأصلية موجودة تماماً كما كانت قبل الإرسال.
*   نوع الخدمة.
*   الأعلام.
*   بعض البيانات الفنية الأخرى.
*   الحمولة ، التي تمثل الجزء الأكبر من الرزمة (كل ما سبق يعتبر بمثابة فوق) ، وهي في الواقع البيانات التي يتم نقلها.

## الحزم والبروتوكولات

تختلف الحزم في البنية والوظائف حسب البروتوكولات المطبقة. يستخدم بروتوكول VoIP بروتوكول IP ، ومن ثم حزم IP. على شبكة Ethernet ، على سبيل المثال ، يتم إرسال البيانات في إطارات Ethernet.

في بروتوكول IP ، تنتقل رزم IP عبر الإنترنت عبر العقد ، وهي الأجهزة وأجهزة التوجيه (التي تسمى تقنيًا العقد في هذا السياق) الموجودة على الطريق من المصدر إلى الوجهة.

يتم توجيه كل حزمة نحو الوجهة استنادًا إلى عنوان المصدر والوجهة. في كل عقدة ، يقرر الموجّه ، استنادًا إلى الحسابات التي تنطوي على إحصائيات وتكاليف الشبكة ، والتي تكون العقدة المجاورة أكثر فاعلية لإرسال الحزمة.

هذه العقدة المحددة هي أكثر فعالية لإرسال الحزمة. هذا جزء من تحويل الرزم الذي يقوم بالفعل بتدفق الحزم على الإنترنت ويجد كل منهم طريقه الخاص إلى الوجهة. تستخدم هذه الآلية البنية الأساسية للإنترنت مجاناً ، وهو السبب الرئيسي الذي تجعل مكالمات VoIP والمكالمات عبر الإنترنت مجانية أو رخيصة جدًا.

على عكس الاتصالات الهاتفية التقليدية حيث يجب تخصيص وتخصيص خط أو دائرة بين المصدر والوجهة (يسمى تبديل الدائرة) ، وبالتالي فإن التكلفة الثقيلة ، تبديل الرزم يستغل الشبكات القائمة مجاناً.

مثال آخر هو TCP (بروتوكول التحكم بالإرسال) ، الذي يعمل مع IP في ما نسميه مجموعة TCP / IP. يعد TCP مسؤولاً عن ضمان موثوقية نقل البيانات. ولتحقيق ذلك ، فإنه يتحقق مما إذا كانت الحزم قد وصلت بالترتيب ، سواء كانت هناك أي رزم مفقودة أو تم تكرارها ، وما إذا كان هناك أي تأخير في إرسال الحزم. يتحكم في ذلك عن طريق ضبط المهلة والإشارات التي تسمى الإقرارات.

## استنتاج

تنقل البيانات في الحزم عبر الشبكات الرقمية وجميع البيانات التي نستهلكها ، سواء كانت نصية أو صوتية أو صورية أو فيديو ، تنقسم إلى حزم يتم إعادة تجميعها في أجهزتنا أو أجهزة الكمبيوتر. هذا هو السبب ، على سبيل المثال ، عندما يتم تحميل صورة عبر اتصال بطيء ، فإنك تشاهد قطعًا تظهر واحدة تلو الأخرى.

#### معلومات اكثر:

[جميع مفاهيم الشبكات في تفاصيل موجزة](https://www.lifewire.com/what-is-a-data-packet-3426310 "مقال نجاة حول حزم البيانات")