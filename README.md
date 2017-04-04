# 29.03.2017
### 1. Describe an instance of prototypal inheritance in JavaScript?
 ```javascript
 function object(o) {
        function F() {}
        F.prototype = o;
        return new F();
    };
```
### 2. What are closures and how are they used?
Closure funksiya icinde funksiyadir.
### 3. Can you use x === “object” to test if x is an object?
Beli.
### 4. What happens when you don’t declare a variable in Javascript?
Globalda yazmaq isteyrikse ferqi yoxdur. Amma yalniz funksiya daxilinde run etmek isteyirikse var declare etmeliyik. Deyer menimsetmirikse gloabalda var yazmaq mecburidir.
### 5. What is the difference between == and === ?
Ferq odur ki, === (strict equality comparison) obyektleri tiplerine gore muqayise edir ve neticeni cixardir. == (type-converting equality comparison) ise tipleri muxtelifdirse deyerlerinin eyni olub oolmadigini yoxlayir. Meselen: 
 ```javascript
var a = 42;
var b = "42";
console.log(a == b); // true
console.log(a === b); // false
 ```
### 6. What datatypes are supported in Javascript?
* Boolean:
true ve false.
* Null
Null ozu obyektdir.
 ```javascript
var a = null;
console.log(typeof a); // object
consoel.log(a); // null
 ```
* Undefined:
Eger deyisen teyin edib ona deyer vermirikse bize undefined qaytaracaq. Bu deyisen mueyyen bir yer tutur(JavaScriptde 'sonsuz' deye deye bilerik), yeni ancaq flagler qoyulur. 
* Number:
Musbet, menfi, onluq kesr ve s. butun ededler daxildir. 
* String:
"" ve ya '' yazilir. 
* Symbol:
ECMASCRIPT6da yeni datatypedi. Meselen:
 ```javascript
var name = Symbol("Emrah");
var qrup = { p201: true};
qrup[name] = "Ismayilzade";

for (var a in qrup) {
	if(qrup.hasOwnProperty(a)){
		console.log(a); // p201
	}
}
console.log(qrup[name]); // Ismayilzade
Symbol istdeyimiz obyektin propertisini gizlemeye imkan verir. Yaddasda mueyyen yer tutur amma bunu ekrana cixarmir.
Eger bele yazmis olsaydiq:
var name = "Emrah";
var qrup = { p201: true};
qrup[name] = "Ismayilzade";
 ```
 ```javascript
for (var a in qrup) {
	if(qrup.hasOwnProperty(a)){
		console.log(a); 
	}
}
console.log(qrup[name]); 
// p201
// Emrah
// Ismayilzade
 ```
Burda "Emrah"i da vermis olacaqdi.
* Object:
Hemise deyirsiz muellim: 'Javascriptde her sey obyektdir'. Array, date, function hamisi obyektdir. Obyekt vars demeli propertysi de var.
### 7. What would “1”+2+3 and 1+2+“3” evaluate to, respectively?
 ```javascript
var a = "1";
var b = 2;
var c = 3;

console.log(a+b+c); // 123

var a = 1;
var b = 2;
var c = "3";

console.log(a+b+c); // 33
 ```
Eger ilk deyisen stringdirse, ondan sonra gelenleri de string kimi goturecek. Yoxsa connector kimi davranacaq.
### 8. Explain the concept of unobtrusive Javascript?
3 esas prinsipe boolmek olar: 
* index.html-de js kodu yazma, ancaq js faylinda yaz.
* Her js kodu oz loacl scope-unda run olsun. Belelikle qarisiqliq olmayacaq.
* Browsera uygun kod yazma standart her browserda istifade ede bileceyin kod yaz.
### 9. What is the difference between a null value and an undefined value?
* Null ozu obyektdir.
 ```javascript
var a = null;
console.log(typeof a); // object
consoel.log(a); // null
 ```
* Undefined:
Eger deyisen teyin edib ona deyer vermirikse bize undefined qaytaracaq. Bu deyisen mueyyen bir yer tutur(JavaScriptde 'sonsuz' deye deye bilerik), yeni ancaq flagler qoyulur.
### 10. Which conditional statements will JavaScript support?
if, else, else if, switch.
if: 
 ```javascript
var a = 3;
if(a < 5){
	console.log(a); // 3
} 
 ```
else:
 ```javascript
var a = 7;
if(a < 5){
	console.log('Salam');
}else {
	console.log('Sagol'); // Sagol
}
 ```
esle if:
 ```javascript
var a = 5;
if(a < 5){
	console.log('Salam');
}else if(a > 5){
	console.log('Sagol');
}else{
	console.log('Hewzad'); // Hewzad
}
 ```
### 11. What is NaN? 
NaN - Not a number. Deyerin number olub olmadigi yoxlayir, type string, date ve s. olsada olar. isNaN() funksiyasi ile eynidir.
### 12. Explain the meaning of the keyword ‘this’ in JavaScript functions.
Globalda this keywordu windowu bildirir, global funksiya daxilinde de eynen. Obyektde daxilinde obyekti bildirir. 
### 13. What is the difference between undefined and not defined in JavaScript?
undefined deyisen teyin edib deyer vermediyimiz halda cagirdiqda verir. not defined globalda deyer vermedikde qaytarir ve ya umumiyyetle deyisen teyin etmedikde.
 ```javascript
var x;
console.log(x); // undefined
x; 
console.log(x); // is not defined
 ```
### 14. What is function hoisting in JavaScript?
Basa dusmusem amma yaza bilmeyecem.
### 15. Can you name two programming paradigms important for JavaScript app developers?
JavaScript cox paradigmali dildi . OOP ve functionalla birlikde imperative paradigmani da destekleyir.
### 16. What is functional programming?
Funksional proqramlasdirma hesablamalari riyazi funksiyalarin komeyile eden ve mutable(deyisdirile bilen) datadan uzaq duran bir programming paradigmdir.
### 17. What is the difference between classical inheritance and prototypal inheritance?
--- Oxudum basa dusmedim.
### 18. What are the pros and cons of functional programming vs object-oriented programming?
---
### 19. When is classical inheritance an appropriate choice?
---
### 20. When is prototypal inheritance an appropriate choice?
---
### 21. What does “favor object composition over class inheritance” mean?
---
### 22. What are two-way data binding and one-way data flow, and how are they different?
---
### 23. What are the pros and cons of monolithic vs microservice architectures?
Onu basa dusdum ki, Monolithic tek, bir yerde architecture demekdir, microservice ise funksiyalarina, tipine gore ferqli isler goren hisselerin architecturasi demekdir.
### 24. What is asynchronous programming, and why is it important in JavaScript?
Eyni anda bir nece prosesin getmesi ucun istifade olunur. Kontrol axisini(control flow) nizamlayir.
