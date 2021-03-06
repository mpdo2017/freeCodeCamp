---
title: Random Method
localeTitle: طريقة عشوائية
---
## طريقة عشوائية

طريقة JavaScript `Math.random()` هي طريقة مدمجة ممتازة لإنتاج أرقام عشوائية. عند تنفيذ `Math.random()` ، تقوم بإرجاع رقم عشوائي يمكن أن يكون بين 0 و 1. يتم تضمين 0 و 1 مستثنى.

### توليد رقم نقطة عائم عشوائي بين 0 و 1

سيقوم الأسلوب `Math.random()` بإرجاع رقم عشري (عشري) أكبر من أو يساوي 0 وأقل من (ولكن لا يساوي مطلقًا) 1. وبعبارة أخرى `0 <= x < 1` . فمثلا:

```JavaScript
console.log(Math.random());
// 0.7069207248635578

console.log(Math.random());
// 0.765046694794209

console.log(Math.random());
// 0.14069121642698246
``` 

(وبالطبع ، ستكون الأرقام التي يتم إرجاعها مختلفة في كل مرة. سيتم افتراض ذلك لكافة الأمثلة التالية - ستحدث نتائج مختلفة لكل تمريرة.)

للحصول على رقم عشوائي بين مجموعة أكبر `Math.random()` نتيجة `Math.random()` برقم.

### توليد رقم نقطة عائمة عشوائية بين 0 و max محدد

عادة لا تحتاج إلى أرقام عشوائية بين 0 و 1 - تحتاج إلى أعداد أكبر أو حتى أعداد صحيحة.

على سبيل المثال ، إذا كنت تريد رقم نقطة عائم عشوائيًا بين 0 و 10 ، فيمكنك استخدام:

```JavaScript
var x = Math.random()*10;

console.log(x);
// 4.133793901445541
``` 

### توليد رقم نقطة عائمة عشوائية داخل نطاق

إذا كنت تحتاج إلى رقم نقطة عائمة عشوائي يتراوح بين رقمين محددين ، فيمكنك فعل شيء كالتالي:

```JavaScript
var min = 83.1;
var max = 193.36;

var x = Math.random()*(max - min)+min;

console.log(x);
// 126.94014012699063
``` 

### توليد عدد صحيح عشوائي بين 0 و max

غالبا ما تحتاج إلى الأعداد الصحيحة. للقيام بذلك ، سيتعين عليك استخدام بعض الطرق الأخرى من كائن `Math` ، `Math.floor()` (تقريبًا إلى أقرب عدد صحيح) و `Math.ceil()` (تقريبًا إلى أقرب عدد صحيح).

على سبيل المثال ، إذا كنت تريد التحديد عشوائياً من مصفوفة من 10 عناصر ، فستحتاج إلى رقم عشوائي بين 0 و 9 ضمناً (تذكر أن المصفوفات صفر فهرستها).

```JavaScript
var x = Math.floor(Math.random()*10);

console.log(x);
// 7
``` 

(تذكر أن `Math.random()` لن ترجع بالضبط 1 ، لذلك لن يتمكن `Math.random()*10` العودة تمامًا 10. وهذا يعني أنه بعد التقريب إلى الأسفل ، ستكون النتيجة دائمًا 9 أو أقل.)

### توليد عدد صحيح عشوائي بين 1 و max

إذا كنت بحاجة إلى رقم عشوائي مع الحد الأدنى لعدد 1 (على سبيل المثال ، اختيار يوم عشوائي في يناير) ، يمكنك استخدام أسلوب `Math.ceil()` .

```JavaScript
var x = Math.ceil(Math.random()*31);

console.log(x);
// 23
``` 

طريقة أخرى كانت لاستخدام الوظيفة السابقة (باستخدام `Math.floor()` ) وإضافة 1 إليها:

```JavaScript
var x = Math.floor(Math.random()*31)+1;

console.log(x);
// 17
``` 

### توليد عدد صحيح عشوائي داخل نطاق

وأخيرًا ، تحتاج في بعض الأحيان إلى عدد صحيح عشوائي بين رقمين محددين. على سبيل المثال ، إذا كنت تحاول اختيار تذاكر يانصيب وكنت تعرف أرقام أقل وأكبر رقم:

```JavaScript
var min = 1718;
var max = 3429;

var x = Math.floor(Math.random()*(max-min+1)+min);

console.log(x);
//2509
``` 

### ما مدى عشوائية Math.random ()؟

يمكن الإشارة إلى أن الرقم الذي تم إرجاعه بواسطة `Math.random()` هو رقم زائف عشوائي حيث لا يمكن لأي كمبيوتر إنشاء رقم عشوائي حقيقي ، والذي يعرض عشوائيًا على جميع المقاييس وعلى جميع أحجام مجموعات البيانات. ومع ذلك ، فإن الرقم الزائف العشوائي الذي تولده `Math.random()` يكفي عادة لاحتياجات أي برنامج تقريبًا قد تكتبه. لا تظهر العشوائية الحقيقية فقط في مجموعات الأرقام الكبيرة الفلكية أو عندما تكون هناك حاجة إلى الكسور العشرية غير المألوفة.

### معلومات اكثر:

*   الوثائق: [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/random)