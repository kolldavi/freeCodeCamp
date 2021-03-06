---
title: Comparison Operators
localeTitle: عوامل المقارنة
---
تحتوي JavaScript **على** مقارنات **صارمة** **ونوع تحويل** .

*   المقارنة الصارمة (مثل ===) صحيحة فقط إذا كانت المعاملات من نفس النوع.
    
*   المقارنة المجردة الأكثر استخدامًا (على سبيل المثال ==) تقوم بتحويل المعاملات إلى نفس النوع قبل إجراء المقارنة.
    
*   بالنسبة للمقارنات المجردة العلائقية (على سبيل المثال ، <=) ، يتم تحويل المعاملات أولاً إلى الأوليات ، ثم إلى نفس النوع ، قبل المقارنة.
    
*   تتم مقارنة السلاسل استنادًا إلى الترتيب المعجمي القياسي ، باستخدام قيم Unicode.
    

## ميزات المقارنات:

*   تكون السمتان متساويتان تمامًا عندما يكون لهما نفس التسلسل من الأحرف والطول نفسه والحروف نفسها في المواضع المقابلة.
    
*   رقمين متساويان تمامًا عندما تكون متساوية عدديًا (لها نفس قيمة الرقم). NaN لا تساوي أي شيء ، بما في ذلك NaN. الأصفار الإيجابية والسلبية تساوي بعضها البعض.
    
*   اثنين من المعاملات المنطقية متساوية تماما إذا كان كلاهما صحيحا أو كلاهما غير صحيح.
    
*   اثنين من الكائنات المتميزة لا تساوي أبدا للمقارنات الصارمة أو المجردة.
    
*   يكون التعبير الذي يقارن الكائنات صحيحًا فقط إذا كانت المعاملات تشير إلى نفس الكائن.
    
*   تكون كل من Null و Undefined Typs متساوية تمامًا مع نفسها وتساوي نظريًا مع بعضها البعض.
    

## مشغلي المساواة

### المساواة (==)

يقوم مشغل المساواة بتحويل المعاملات إذا **لم تكن من نفس النوع** ، ثم تطبق المقارنة الصارمة. إذا كان **كلا المعاملات عبارة عن كائنات** ، فإن JavaScript يقارن المراجع الداخلية التي تساوي عندما تشير المعاملات إلى نفس الكائن في الذاكرة.

#### بناء الجملة

 ` x == y 
` 

#### أمثلة

 ` 1   ==  1        // true 
 "1"  ==  1        // true 
 1   == '1'       // true 
 0   == false     // true 
 0   == null      // false 
 
   0   == undefined   // false 
 null  == undefined   // true 
` 

### عدم المساواة (! =)

عامل عدم المساواة بإرجاع true إذا كانت المعاملات غير متساوية. إذا **لم يكن** المعاملان **من نفس النوع** ، يحاول JavaScript تحويل المعاملات إلى نوع مناسب للمقارنة. إذا كانت **كل المعاملات هي كائنات** ، فإن JavaScript يقارن المراجع الداخلية التي لا تساوي عندما تشير المعاملات إلى كائنات مختلفة في الذاكرة.

#### بناء الجملة

 `x != y 
` 

#### أمثلة

 `1 !=   2     // true 
 1 !=  "1"    // false 
 1 !=  '1'    // false 
 1 !=  true   // false 
 0 !=  false  // false 
` 

### الهوية / المساواة الصارمة (===)

عامل تشغيل الهوية بإرجاع true إذا كانت المعاملات متساوية بدقة **مع أي نوع التحويل** .

#### بناء الجملة

 `x === y 
` 

#### أمثلة

 `3 === 3   // true 
 3 === '3' // false 
` 

### عدم الهوية / عدم المساواة الصارمة (! ==)

يتم إرجاع عامل التشغيل non-identity إذا كانت المعاملات **غير متساوية و / أو لا من نفس النوع** .

#### بناء الجملة

 `x !== y 
` 

#### أمثلة

 `3 !== '3' // true 
 4 !== 3   // true 
` 

## مشغلي العلائقية

### أكبر من المشغل (>)

أكبر من المشغل يعود صحيح إذا كان المعامل الأيسر أكبر من المعامل الصحيح.

#### بناء الجملة

 `x > y 
` 

#### أمثلة

 `4 > 3 // true 
` 

### عامل أكبر من أو مساوي (> =)

عامل التشغيل أكبر من أو يساوي بإرجاع true إذا كان المعامل الأيسر أكبر من أو يساوي المعامل الأيمن.

#### بناء الجملة

 `x >= y 
` 

#### أمثلة

 `4 >= 3 // true 
 3 >= 3 // true 
` 

### أقل من المشغل (<)

أقل من عامل التشغيل يعود صحيح إذا كان المعامل الأيسر أقل من المعامل الصحيح.

#### بناء الجملة

 `x < y 
` 

#### أمثلة

 `3 < 4 // true 
` 

### أقل من أو يساوي المشغل (<=)

عامل التشغيل أقل من أو يساوي بإرجاع true إذا كان المعامل الأيسر أقل من أو يساوي المعامل الأيمن.

#### بناء الجملة

 `x <= y 
` 

#### أمثلة

 `3 <= 4 // true 
` 

_يمكنك العثور على مزيد من المعلومات في [MDN](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Comparison_Operators) ._

## مقارنة لاغية وغير محددة

عندما نقارن لاغية وغير محددة نرى سلوك مختلف. يتيح التحقق من سيناريو مختلف من خلال الأمثلة

#### مثال - فحص دقيق للمساواة (===)

console.log (خالية === غير محدد)؛ // O / P - false

Otuput غير صحيح وهذا صحيح لأننا نعلم أن "null" و "undefined" هي أنواع مختلفة.

#### مثال - التحقق من المساواة غير الصارمة (==)

console.log (خالية == غير محدد) ؛ // O / P: - صحيح

ماذا؟ هذا لأن هناك قاعدة خاصة لـ "فارغة" و "غير معرفة". نظرا لأنها متساوية في حالة الفحص غير المتشدد (==) ولكنها لا تساوي أي قيمة أخرى.

إذا استخدمنا عوامل المقارنة مثل <،> ، <= ،> = وما إلى ذلك ، يتم تحويل "فارغ" و "غير محدد" إلى رقم وفي مثل هذه الحالات ، تصبح القيمة "فارغة" 0 و "غير محددة" ستكون نانوية. يتيح التحقق من بعض تلك الأمثلة.

#### مثال - قارن الصفر بـ 0 (صفر)

console.log (خالية> 0) ؛ // O / P - false console.log (فارغة) = 0) ؛ // O / P - صحيح console.log (خالية == 0) ؛ // O / P - false

غريب؟ وفقا للبيان الأول ، لا تكون القيمة null أكبر من 0 ومن العبارة الثانية تكون null أكبر من أو تساوي 0. لذا ، إذا فكرنا رياضيا ومقارنة كلتا العبارتين ، فستصل إلى النتيجة أن null تساوي 0. لكن ، حسب البيان الثالث ليس صحيحا. لماذا ا؟

والسبب هو "المقارنة" و "التحقق من المساواة" يعملان بطريقة مختلفة. في المقارنة ، يتم أولاً تحويل "null / undefined" إلى رقم لذلك ، في أول حالتين "null" تصبح 0 و لذلك case1) (فارغة> 0) -> false و case2) (null> = 0) -> true. ولكن ، في التحقق من المساواة (==) ، تعمل "خالية / غير محددة" دون أي تحويل وكما هو موضح أعلاه (قاعدة خاصة) ، في التحقق من المساواة "خالية / غير محددة" تساوي فقط بعضها البعض ولا تساوي أي شيء آخر. وبالتالي (خالية == 0) -> كاذبة.

#### مثال - قارن غير محدد 0 (صفر)

console.log (غير محدد> 0)؛ // O / P - false console.log (غير محدد> = 0)؛ // O / P - false console.log (غير محدد == 0) ؛ // O / P - false

هنا ، نختبر نفس الحالات كما فعلنا للشيء الفارغ لكن النتيجة أخرى مختلفة. لماذا ا؟

الأسباب هي على النحو التالي. في الحالتين الأوليين ، نقوم بمقارنة غير معروف مع 0 وكما ذكرنا أعلاه بالمقارنة يتم تحويل غير معرفة إلى NaN. NaN هي قيمة خاصة تعود دائمًا كاذبة بالمقارنة مع أي رقم وهذا هو السبب في أننا حصلنا على نتائج خاطئة في أول حالتين. بالنسبة للبيان الثالث ، فإن السبب هو نفسه كما هو مذكور في "null". في التحقق من المساواة "لاغية / غير محددة" تساوي فقط بعضها البعض ولا تساوي أي شيء آخر. وبالتالي (undefined == 0) -> false.