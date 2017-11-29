# المشاكل والأخطاء الشائعة

## ما دفع لنا

#### 1.لقد بدأت للتو باستخدام هذا الدفع، ولكن يبدو أني قد علقت.

في المرة الأولى التي تبدأ باستخدامها، فإنه سيتم تحميل سلسلة الكتل. هذا يمكن أن يستغرق فترة تصل إلى ساعة و سيظهر  لك كل شيء تريد القيام به.

#### 2. عبارة المرور الغير صالحة للمفتاح الخاص الرئيسي.

هذا هو مجرد طريقة للقول أنها ، "كلمة مرور غير صحيحة". وأنك أدخلت كلمة مرور خاطئة لمحفظتك.

#### 3. "غير قادر على شراء تذاكر: الأموال المتاحة غير كافية ..." ولكن محفظتك تقول ان لديها ما يكفي.

هناك علة معروفة في طريقة الدفع حيث أن الأموال غير الواردة يتم حسابها على أنها متاحة. وذلك بعد تصويت التذكرة، هناك 256 نافذة كتلة حيث لا تزال الأموال مقفلة. في هذه الحالة، فهي معروفة بأنها غير واردة. عندما تنتهي هذه الفترة فإنها  ستكون قابلة للاستخدام مرة أخرى.

#### 4. طريقة الدفع هي عرض التوازن الخاطئ

> هذه التعليمات صالحة كما لو نها من إصدار 0.8.x وقد لا تعمل مع الإصدارات الأحدث.

إذا أن عرض الدفع و التوازن خاطئ، يمكنك إصلاحه باستخدام الأداة المساعدة لسطر الأوامر والكتابة فوق بعض الملفات. وبعضها يمكن  أن يكون مربكا إذا لم تكن مألوفة مع سطر الأوامر، ولكن فقط اتبع التعليمات الخط من قبل سطرو عليك أن تكون على ما يرام.   حيث ترى الأوامر التي  `look like this`, ومجرد نسخها ولصقها تماما كما هي في سطر الأوامر. لا تنسى أن تقوم بالضغط على <ENTER> بعد كل الأوامر. إذا واجهتك مشكلة، انضم إلى [قناة سلاك] (https://decred.slack.com)  و سوف تحصل على مساعدة شخص ما, ولكن أولاً , قم بفحص الأوامر والتأكد من المتاحة حالياً. و بهذا سوف تحتاج لأصول المحفظة. وهذه العملية يجب أن تستغرق ما يقارب ال 15 دقيقة.

1. سنقوم بفتح ثلاثة نوافذ لطاقة شل. لذلك اضغط على مفتاح النافذة. اكتب 'طاقة شل' (لا تكتب علامات الاقتباس هنا أو في المستقبل واضغط موافق.
2. قم بهذا لمرتين اخريتين
3. تنقل بين النوافذ لتتمكن من رؤية الجميع.
4. نسخ ولصق الأمر التالي: `سد $ إنف: بروغرامفيلز / ديكريد / paymetheus` (ملاحظة، في بويرشيل، اضغط كترل + V أو انقر بزر الماوس الأيمن للصق). اضغط على  موافق.
5. قم بتشغيل نفس الأمر في نافذتين أخريتين
6. افتح مستكشف ويندوز.
7. الصق `٪ لوكالابداتا٪ / ديكريد / paymetheus` في شريط الموقع. اضغط على موافق .
8. حذف المجلد "الشبكة الرئيسية".
9. انتقل إلى أحد نوافذ طاقة شل ولصق `./dcrd -u <username> -P <password>`. اضغط على موافق.
10. اذهب إلى أحد نوافذ طاقة شل الأخرى ولصق `./dcrwallet --appdata = $ إنف: لوكالابداتا / ديكريد / بيميثيوس --create`
11. اتبع المطالبات واستيراد الأصول الخاصة بك. قل لا عند طلب الطبقة الإضافية منها والتشفير عندما سئل عما إذا كان لديك أصلها.
12. في هذا السياق، أدخل الكلمات الأصل الخاصة بك واضغط موافق مرتين.
13. قم بلصق الأمر التالي في نفس النافذة: `./dcrwallet -u <username> -P <password> --appdata = $ إنف: لوكالابداتا / ديكريد / paymetheus`. اضغط على موافق.
14. أدخل عبارة المرور الخاصة التي تستخدمها عند إنشاء محفظتك.
15. انتقل إلى نافذة طاقة شل الثالثة ولصق `./dcrctl -u <username> -P <password> --wallet -c $ إنف: لوكالابداتا / ديكريد / بيميثيوس / rpc.cert getbalance`. اضغط على موافق.
16. اضغط إغلاق + C في أول اثنين من النوافذ لإغلاق البرامج (dcrd و dcrwallet).
17. يمكنك إغلاق جميع نوافذ طاقة شل الثلاثة
18. rpc.cert and rpc.key. إرجع إلى مستكشف الويندوز. واحذف اثنين من الملفات, 
19. بدء تشغيل برنامج decred لبدء استخدام الدفع  مرة أخرى.

-----

## إثبات صحة الحصة

#### 1. بعض من نقص / انتهاء التذاكر ولا تزال مغلقة بعد أكثر من يوم واحد.

1. بدء عملية المحفظة مع `--enablevoting` العلم. فإنه لن يصدر عمليات الإلغاء دون ذلك.
2. فتح المحفظة مع `dcrctl --wallet عبارة مرور المحفظة <yourpassphrase> 0`. يجب أن تكون المحفظة مقفلة حتى تكون قادرة على إنشاء عمليات الإبطال والتوقيع عليها.
3. توجيه dcrd لإعلام المحفظة عن تذاكر غاب مرة أخرى لذلك سوف تصدر عمليات الإلغاء مع `dcrctl rebroadcastmissed`.


في هذه النقطة, يجب أن ترى بعض التفاصيل حول معاملات الإلغاء في سجل المحفظة. وحالما يتم استخلاص معاملات الإبطال في هذه الكتل (الذي ينبغي أن يكون الفدرة التالية) سترى الأموال تتحرك إلى فئة توليد حصة غير المكتملة `dcrctl --wallet`. وأخيراً, بعد 256 كتلة, فإنها ستنتقل إلى الفئة القابلة للإنفاق وبالتالي تكون متاحة للإنفاق.