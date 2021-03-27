# temel-progralama




# JavaScript
JavaScript günümüzde gelişmiş olan tüm web sitelerinin neredeyse tamamında kullanılmaktadır. JavaScript web sitelerinin dinamik olmasını ve işlevselliğinin artmasını sağlar. Kullanıcı taraflı ve sunucu taraflı çalışabilir. Web sitelerinin kullanıcılar ile iletişim kurmasına yardımcı olur.


# Web Sayfasına JavaScript Ekleme
3 farklı yol ile eklenebilir.
-   **_Inline script_**
-   **_Internal script_**
-   **_External script_**
    -   **_Multiple External scripts_**
   
  
 ## Inline Script (Satır içi)
JavaScript kodlarını doğrudan HTML belgesine ekleyerek bir web sayfası tarafından yapılan isteklerin sayısını azaltır.
 ```
<!DOCTYPE html>
<html>
  <head>
    <title>Privia</title>
  </head>
  <body>
    <button onclick="alert('Sunumuma hoş geldiniz')">Click Me</button>
  </body>
</html>
```

## Internal Script 
JavaSript kodlarımızı **< script> </ script>** etiketleri arasında yazılır.
**"head"** veya **"body"** içerisinde yazılabilir.
Kodu, HTML dosyasının neresine eklediğimize bağlı olarak JavaScript’in yüklenme şekli değişecektir. Önerilen uygulama yöntemi <**head**> kısmına eklemektir çünkü böylece HTML dosyasının olağan içeriğinden ayrı kalabilir. 
 ```
<!DOCTYPE html>
<html>
  <head>
    <title>Privia</title>
    <script>
      console.log('Sunumuma hoş geldiniz')
    </script>
  </head>
  <body></body>
</html>
```
<**body**> bölümüne eklememiz, web site içeriğinin daha hızlı yüklenerek yüklenme hızını iyileştirir.
 ```
<!DOCTYPE html>
<html>
  <head>
    <title>Privia</title>
  </head>
  <body>
    <button onclick="alert('Sunumuma hoş geldiniz!');">Click Me</button>
    <script>
      console.log('Sunumuma hoş geldiniz')
    </script>
  </body>
</html>
```

## External Script
js uzantısıyla biten tüm dosyalar JavaScript dosyalarıdır.Dosya bağlantısı
 **"head"**  veya **"body"** içerisinde yazılabilir, ancak  ** "head"** yerleştirilmesi tercih edilir. 
 ```
<!DOCTYPE html>
<html>
  <head>
    <title>Privia</title>
    <script src="main.js"></script>
  </head>
  <body></body>
</html>
 ```
 **"body"** içerisinde
 ```
<!DOCTYPE html>
<html>
  <head>
    <title>Privia</title>
  </head>
  <body>
    <script src="main.js"></script>
  </body>
</html>
 ```
 
## Multiple External Scripts
Birden fazla .js uzantılı dosya kullanabiliriz.
 ```
<!DOCTYPE html>
<html>
  <head>
    <title>Privia</title>
  </head>
  <body>
    <script src="./main.js"></script>
    <script src="./index.js"></script>
  </body>
</html>
 ```


#  1.Variables (Değişkenler)
Programlama dilinde işlediğimiz verileri bilgisayarın hafızasında tutmak için yapmış olduğumuz tanımlamalara değişken denir.
Javascript ES5 ve öncesi sürümleri için bu işlem **var** ifadesi ile yapılıyordu.ES6 ve sonrası sürümler için **let** ve **const** ifadeleri de dile eklendi.Bir değişken bildirmek için var, let veya const kullanırız.

**var** değişken değeri sonradan değiştirilebilir ve tekrar tanımlanabilir. Function scope’tur.Function scope olduğu için if-for tanımlanan değişkenlere dışarıdan erişebilirsiniz.

 ```
for(var i = 0; i < 10; i++){  
console.log(i);  
// 0, 1, 2, 3, 4, 5, 6, 7, 8, 9  
}  
console.log(i);  
// 10
  ```
  **let** değişken değeri sonradan değiştirilebilir ve sadece bir kez tanımlanabilir. block scope’tur.Değişkenin değeri sonradan değiştirilebilir.
   ```
  for(let i = 0; i < 10; i++){  
console.log(i);  
// 0, 1, 2, 3, 4, 5, 6, 7, 8, 9  
}  
console.log(i);  
// i is not defined

let pi = 3;  
console.log(pi);  
// 3  
let pi = 3.1415926535897932384626433;  
console.log(pi);  
//Uncaught SyntaxError: Identifier 'pi' has already been declared
 ```
 **const** değişken değeri sonradan değiştirilemez ve tekrar tanımlanamaz.const block scope’tur. Yani sadece tanımlandığı { } süslü parantez içerisinden erişilebilir.
   ```
const pi = 3;  
console.log(pi);  
// 3  

const pi = 3.141;  
console.log(pi);  
//Uncaught SyntaxError: Identifier 'pi' has already been declared
 ```

# 2.Data Types (Veri Tipleri)
Veri tipi, verilerin özelliklerini gösterir.Derleyiciye veri değerinin ne olduğunu söyler.Bu sayede uygun işlemler gerçekleştirilebilir.
JavaScript'te iki farklı veri türü vardır.
 -  Primitive Data Types (İlkel Veri Tipi)
 - Non-primitive Data Type (İlkel Olmayan(Referans) Veri Tipi)

#### İlkel Veri Tipleri(Primitive Data Types)
Değişmez veri türleridir.
 - String
 -  Number
 -  Boolean
 -  Null
 -  Undefined

#### İlkel Olmayan Veri Türü(Non-primitive Data Type)
Değiştirilebir veri türleridir.
 - Object 
 - Functions
 -  Array
 
 ## İlkel Veri Tipleri(Primitive Data Types)
 ### String
 Bir dize metin içeriğidir.Tek veya çift tırnak içine alınmalıdır.
 
  ```
  var text1="Merhaba";
  var text2='Dünya';
  var sentence= text1 + "" + text2;
   ```
   ### Number
   Ondalık basamaklı veya ondalık olmayan pozitif veya negeatif sayıları göstermemizi sağlayan veri tipidir.
   
     ```
     var a=25; //integer
     var b=80.5; //float
     var c=4.25e+6; //üstel gösterim
    ```
   number veri tipi bazı özel değerlere sahiptir.
   
  ```
 alert(16/0); //Infinity
 alert(-16/0); // -Infinity
   alert("Yazı yazı")/2; //NaN (Not a Number)
   ```
 ### Boolean
  Yalnızca iki değer tutabilir.true(evet) ve false(hayır).
 ```
     var okuyor= true; //evet,okuyor
     var uyuyor= false; //hayır,uyumuyor
     alert(1>2); //false
     alert(5==5); //true
```
   ### Null
  Bir değişken null değerine sahipse o değişkenin değeri yoktur.
   ```
    var x= null; //değeri yok
    var y=" "; //değeri var boşluk
   ```
   ### Undefined
   Bir değişken tanımlanmış ancak bir değer atanmamışsa tanımsız değere sahip olur.
   ```
    var a;
    var b= "Merhaba Dünya";
    alert(a); //undefined
    alert(b); // Merhaba Dünya
  ```
     
   ## İlkel Olmayan Veri Türü(Non-primitive Data Type)
   ### Object (Nesne)
   Birden farklı veri tiplerini depolamamıza izin verir.
   ```
   var school = {}; 
   var student {"name":"ali","class": "9A", "score":90};
    
   var car = { 
     "model": "Fiat-egea", 
     "color": "white", 
      "year" : 2018 }
   ```
   ### Functions
   Her bir fonksiyon, bir JavaScript işlemidir.Bir görevi yerine getiren veya değer hesaplayan kod bloklarıdır.
   ```
   function selamla(name){ return  "Hello, " +name; }
 function selamYap(selamFonksiyon, adı){
     return selamFonksiyon(adı); 
}
var result = selamYap(selamla, "Ahmet"); alert(result);
 // Merhaba, Ahmet
```
   
   ### Array (Dizi)
   Bir değişkenin birden fazla değerini depolamak için kullanılar veri tipidir.Dizideki her bir değer **index** olarak bilinen sayısal bir konuma sahiptir.İlk index değeri 0 dır.
   ```
   var color = ["Mavi", "Sarı", "Yeşil", "Turuncu"]; 
   var city = ["Ankara", "İstanbul", "Malatya"];  
   alert(color[0]); //  Mavi 
   alert(city[1]); //İstanbul
   ```
   
   ## Typeof (Operatör Türü)
   Bir değişkenin hangi veri türünü içerdiğini bulmak için kullanılır.
   ```
     typeof  15; // "number"
     typeof  42.7; //  'number'  
     
   typeof  'merhaba'; // 'string'  
   
   typeof  true; // "boolean"  

typeof {adı: "Hasan", "yas": 22}; // "Object"  

typeof  function(){}; // "Functions"
   ```
   
# 3.Arrays
Birden fazla verinin saklanması için oluşturulan değişkenlere dizi adı verilir. 
Değişkenlerdeki her bir veriye  eleman  denir. Dizi elemanları  indeks değerleri  ile çağrılırlar. İndeksler bir çok programlama dilinde olduğu gibi 0'dan başlar. 0'dan başlamasının sebebi programlama dillerinin tamamen insan mantığı oluşturulmuş olduğunun göstergesidir.

 ##  Dizi Oluşturma 
```
var arr = new Array()
console.log(arr) 
----------------------------
var arr = []
console.log(arr)
```
##  Başlangıç Değerine Sahip Dizi oluşturma  

```
const numbers = [0, 3.14, 9.81, 37, 98.6, 100]
// Numara arrayi
const webTechs = ['HTML', 'CSS', 'JS', 'React', 'Redux', 'Node', 'MongDB'] 
// sitring arrayi

console.log('Numbers:', numbers)
//[0,3.14,9.81,37,98.6,100]

console.log('Web technologies:', webTechs)
//[HTML,CSS,JS,React,Redux,Node,MongDB]

```

 ## Index (Dizin)
Dizideki elemanlara indexlerini kullanarak ulaşırız. Bir dizinin index değeri 0 dan başlar.
```
const numbers = [0, 3.14, 9.81, 37, 98.6, 100] 

console.log(numbers[0]) //   0
console.log(numbers[5]) //   100
```

## Array Öğesini Değiştirme
Dizinin elemanları oluşturulduktan sonra değiştirilebilir.
```
const numbers = [1, 2, 3, 4, 5]
numbers[0] = 10 
numbers[1] = 20 

console.log(numbers) // [10, 20, 3, 4, 5]
```
# Diziyi Değiştirme Yöntemleri

 - Constructor                                
 - fill
 - concat
 - length
 - indexOf
 - lastIndexOf
 - includes
 - Array.isArray
 - toString
 - join
 - slice
 - splice
 - push
 - pop
 - shift
 - unshift
 - reverse
 - sort
 
 ### Constructor
 Dizi oluşturmak için kullanılır.
 ```
 const arr = Array() 
console.log(arr)
 ```
### fill
Diziyi sabit değerler ile doldurmak için kullanılır.
```
const eightXvalues = Array(8).fill('X')
console.log(eightXvalues) // ['X', 'X','X','X','X','X','X','X']

const four4values = Array(4).fill(4) 
console.log(four4values) // [4, 4, 4, 4]
```
### concat
İki farklı diziyi birleştirmek için kullanılır.
```
const firstList = [1, 2, 3]
const secondList = [4, 5, 6]
const thirdList = firstList.concat(secondList)

console.log(thirdList) // [1, 2, 3, 4, 5, 6]
```
### length
Dizinin boyutunu öğrenmek için kullanılır
```
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.length) // 5 
```
### indexOf 
Bir dizide istenen elemanın olup olmadığını kontrol etmek için kullanılır.Eğer var ise elemanın index değerini yok ise -1 döndürür.
```
const numbers = [1, 2, 3, 4, 5]

console.log(numbers.indexOf(5)) //  4
console.log(numbers.indexOf(0)) //  -1
console.log(numbers.indexOf(1)) //  0
console.log(numbers.indexOf(6)) //  -1
```
### lastIndexOf
Eğer dizide aranan eleman birden fazla kez var ise son eşleşmenin index değerini yok ise -1 döndürür.
```
const numbers = [1, 2, 3, 4, 5, 3, 1, 2]

console.log(numbers.lastIndexOf(2)) // 7
console.log(numbers.lastIndexOf(0)) // -1
console.log(numbers.lastIndexOf(1)) //  6
console.log(numbers.lastIndexOf(4)) //  3
console.log(numbers.lastIndexOf(6)) // -1
```
### includes
Aranan elemanın dizide olup olmadığını kontrol etmek için kullanılır.Eğer var ise true yok ise false değer döner.
```
const numbers = [1, 2, 3, 4, 5]

console.log(numbers.includes(5)) // true
console.log(numbers.includes(0)) // false
```
### Array.isArray
Veri tipinin array olup olmadığını kontrol eder.
```
const numbers = [1, 2, 3, 4, 5]
console.log(Array.isArray(numbers)) // true

const number = 100
console.log(Array.isArray(number)) // false
```
### toString
Değişkeni stringe çevirmek için kullanılır.
```
const numbers = [1, 2, 3, 4, 5]
console.log(numbers.toString()) // 1,2,3,4,5
```
###  join
Dizinin elemanlarını birleştirerek string veri tipine dönüştürür.join içinde gönderdiğimiz argüman sayesinde elemanların aralarındaki birleştirme şekillerini değiştirebiliriz.
```
const names = ['Asabeneh', 'Mathias', 'Elias', 'Brook']

console.log(names.join()) // Asabeneh,Mathias,Elias,Brook
console.log(names.join(' # ')) //Asabeneh # Mathias # Elias # Brook
```
###  slice
Başlangıç ve bitiş indexsi olmak üzere iki değişken alabilir.Verilen aralıktaki elemanları kesmek için kullanılır.
```
const numbers = [1, 2, 3, 4, 5]

console.log(numbers.slice(0)) // tüm elemanlar kopyalanır
console.log(numbers.slice(1, 4)) // [2,3,4]  
``` 
### splice
Üç parametre alır: Başlangıç konumu, kaldırılma sayısı ve eklenecek öğe sayısı.
```
const numbers = [1, 2, 3, 4, 5, 6]
console.log(numbers.splice(3, 3, 7, 8, 9)) // [1, 2, 3, 7, 8, 9] 
```
###  push
Dizinin sonuna eleman eklemek için kullanılır.
```
const numbers = [1, 2, 3, 4, 5]
numbers.push(6)

console.log(numbers) //  [1,2,3,4,5,6]
```
###  pop
Dizinin sonundaki elemanı silmek için kullanılır.
```
const numbers = [1, 2, 3, 4, 5]
numbers.pop() 

console.log(numbers) //  [1,2,3,4]
```
### shift
Dizinin başındaki elemanı silmek için kullanılır.
```
const numbers = [1, 2, 3, 4, 5]
numbers.shift() 

console.log(numbers) // [2,3,4,5]
```
###  unshift
Dizinin başına eleman eklemek için kullanılır.
```
const numbers = [1, 2, 3, 4, 5]
numbers.unshift(0) 

console.log(numbers) //  [0,1,2,3,4,5]
```
### reverse
Dizinin elemanları ters çevirmek için kullanılır.
```
const numbers = [1, 2, 3, 4, 5]
numbers.reverse() 

console.log(numbers) // [5, 4, 3, 2, 1]

numbers.reverse()
console.log(numbers) // [1, 2, 3, 4, 5]
```
### sort
Dizi elemanlarını artarak sıralar.
```
const webTechs = [
  'HTML',
  'CSS',
  'JavaScript',
  'React',
  'Redux',
  'Node',
  'MongoDB',
]

webTechs.sort()
console.log(webTechs) // ["CSS", "HTML", "JavaScript", "MongoDB", "Node", "React", "Redux"]
```
## Dizi İçerisinde Dizi 
```
const firstNums = [1, 2, 3]
const secondNums = [1, 4, 9]

const arrayOfArray = [
  [1, 2, 3],
  [1, 2, 3],
]
console.log(arrayOfArray[0]) // [1, 2, 3]

const frontEnd = ['HTML', 'CSS', 'JS', 'React', 'Redux']
const backEnd = ['Node', 'Express', 'MongoDB']
const fullStack = [frontEnd, backEnd]
console.log(fullStack) // [["HTML", "CSS", "JS", "React", "Redux"], ["Node", "Express", "MongoDB"]]

console.log(fullStack.length) // 2
console.log(fullStack[0]) // ["HTML", "CSS", "JS", "React", "Redux"]
console.log(fullStack[1]) // ["Node", "Express", "MongoDB"]
```
# 4.Conditionals(Koşullu İfadeler)
Koşullu ifadeler birer karar yapılarıdır. Şarta bağlı bir komutu yerine getirmek istiyorsak koşul ifadelerini kullanmalıyız ve  boolean tipi sonuçlar döndürürler. 
-   if
-   if else
-   if else if else
-   switch
-   ternary operator

### if
```
let num = 3
if (num > 0) {
  console.log(`${num} pozitiftir`)
}
//  3 pozitiftir
```
```
let isRaining = true
if (isRaining) {
  console.log('koşulum doğru olduğu için beni görüyorsun')
}
```
### if else
```
let num = 3
if (num > 0) {
  console.log(`${num} pozitiftir`)
} else {
  console.log(`${num} negatiftir`)
}
//  3 pozitiftir

num = -3
if (num > 0) {
  console.log(`${num} pozitiftir`)
} else {
  console.log(`${num} negatiftir`)
}
//  -3 negatiftir
```
###  If Else if Else
```
let a = 0
if (a > 0) {
  console.log(`${a} pozitiftir`)
} else if (a < 0) {
  console.log(`${a} negatiftir`)
} else if (a == 0) {
  console.log(`${a} eşittir sıfıra`)
} else {
  console.log(`${a} sayı değildir`)
}
// 0 eşittir sıfıra
```
### Switch
Aldığı parametreye göre doğrudan şartı çalıştırır.Koşul hangi case'in koşuluna uyuyorsa onun kod bloğu çalışır. Her case’den sonra **break;** koymak zorunludur. Eğer yazılmazsa bütün case’leri çalıştırır.
Switch koşulu, else if koşulundan daha hızlı tepki verir. Bunun nedeni switch koşulu içerisine yazılan herhangi bir koşul sağlandığında break deyimi ile çıktı alınırken else if'te tüm koşullar okunmaktadır.
```
switch (caseValue) {
  case 1:
    // code
    break
  case 2:
    // code
    break
  case 3:
  // code
  default:
  // code
}
```
```
let num = prompt('sayı giriniz')
switch (true) {
  case num > 0:
    console.log('sayı pozitif')
    break
  case num == 0:
    console.log('sayı 0')
    break
  case num < 0:
    console.log('sayı negatif')
    break
  default:
    console.log('sayı değil')
}
```
### Ternary Operators (Üçlü Operatör)
if-else operatörünün yerine kullanılır. if-else ile yazılan kod satırımızı kısa bir şekilde ifade etmek için  kullanılır.
koşul ? true ise yapılacak iş : false ise yapılacak iş
```

var kullaniciSayisi = prompt("1'den 100'e kadar bir sayı giriniz.", "");
kullaniciSayisi == (7) ? alert("Doğru") : alert("Yanlış");

```

# 5.Loops (Döngüler)
Kod bloğunu birden çok kez çalıştırmak için kullanılırlar.
-   for
-   while
-   do while
-   for of
-   forEach
-   for in

## for
Döngünün kaç defa devam ettiğini bildiğimiz durumlarda kullanılır.
```
for (koşul başlangıç değeri; koşul; arttırma/azaltma) {  
// Çalışacak komutlar  
}
```
```
const nums = [1, 2, 3, 4, 5]
for (let i = 0; i < 6; i++) {
  console.log(nums[i])
}
```
## while
Döngünün kaç defa devam edeceğini bilmediğimiz durumlarda kullanılır.
```
koşul başlangıç değeri;  
while (koşul) {  
// Çalışacak komutlar  
arttırma/azaltma  
}
```
```
let count = prompt('pozitif sayı giriniz ')
while (count > 0) {
  console.log(count)
  count--
}
```
## do while
while döngüsüne çok benzer ancak koşul doğru olsun veya olmasın döngü içerisindeki kodlar en az bir kez çalışır.
```
koşul başlangıç değeri;  
do {  
// Çalışacak komutlar  
arttırma/azaltma  
} while (koşul)
```
```
let count = 0
do {
  console.log(count)
  count++
} while (count < 11)
```
## for of
bir array’in index’ine ihtiyacımız yoksa doğrudan değerini (value) istiyorsak for of döngüsünü kullanabiliriz.
```
const numbers = [1, 2, 3, 4, 5]
for (const number of numbers) {
  console.log(number)
}
```
## forEach
Foreach listeler ya da diziler üzerinde işlem yapmak için kullanılan döngü yapısıdır. Özellikle eleman sayısının bilinmediği durumlarda kolaylık sağlar..

```
const countries = ['Finland', 'Sweden', 'Norway', 'Denmark', 'Iceland']
countries.forEach((country, i, arr) => {
  console.log(i, country.toUpperCase())
})
```
## for in
Nesnenin özellikleri arasında dolaşabiliriz.
```
const user = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  skills: ['HTML', 'CSS', 'JS', 'React', 'Node', 'Python', 'D3.js'],
}

for (const key in user) {
  console.log(key, user[key])
}
```
## break
Döngüyü sonlandırmak için kullanılır.
```
for (let i = 0; i <= 5; i++) {
  if (i == 3) {
    break
  }
  console.log(i)
}

// 0 1 2
```
## continue
Döngü adımını atlamak için kullanılır.
```
for (let i = 0; i <= 5; i++) {
  if (i == 3) {
    continue
  }
  console.log(i)
}
// 0 1 2 4 5
```

### Özet
for döngüsü -> yineleme sayısı bilindiğinde her yerde kullanılabilir.
while döngüsü -> yineleme sayısı bilinmediğinde 
do while-> yineleme sayısı bilinmediğinde ancak koşul yanlış olsa bile döngü en az bir kez çalışır
for of -> dizi için kullanılır
forEach -> dizi için kullanılır
for in -> nesne için kullanılır

# 6.Scope (Kapsam)
Değişkenlerin, objelerin, fonksiyonların erişilebilirlik kapsamı vardır.2 Temel scope bulunur.
-   Global Scope
-   Local Scope
### Global Scope
Fonksiyonların dışında tanımlanan ve her yerden erişilebilen scope tipidir. Global Scope’da tanımlı bir değişkene dosya içerisinde her yerden erişilebilir.
### Local Scope
Fonksiyonun içinde tanımlanmış değişkenlerdir. Sadece tanımlandıkları kod bloğunun içerisinde kullanılabilirler.
```
let a = 'JavaScript' // global scope 
let b = 10 //  global scope 
function letsLearnScope() {
  console.log(a, b) // JavaScript 10
  if (true) {
    let a = 'Python'
    let b = 100
    console.log(a, b) // Python 100
  }
  console.log(a, b) // JavaScript 10
}
letsLearnScope()
console.log(a, b) // JavaScript 10
```
### ! Hatırlatma 
Değişkenlerimizden olan **var**  function scope'tur.Function scope olduğu için if-for tanımlanan değişkenlere dışarıdan erişebilirsiniz.
```
function letsLearnScope() {
  var gravity = 9.81
  console.log(gravity)
}
console.log(gravity) // Uncaught ReferenceError: gravity is not defined

if (true) {
  var gravity = 9.81
  console.log(gravity) // 9.81
}
console.log(gravity) // 9.81

for (var i = 0; i < 3; i++) {
  console.log(i) // 0,1, 2
}
console.log(i) //3
```
Ancak **let** ve **const** block scoptur.Sadece tanımlandığı { } süslü parantez içerisinden erişilebilir.
```
function letsLearnScope() {
  const gravity = 9.81
  console.log(gravity)
}
console.log(gravity) // Uncaught ReferenceError: gravity is not defined

if (true) {
  const gravity = 9.81
  console.log(gravity) // 9.81
}
console.log(gravity) // Uncaught ReferenceError: gravity is not defined

for (let i = 0; i < 3; i++) {
  console.log(i) // 0,1,2
}
 console.log(i) // Uncaught ReferenceError: gravity is not defined
```

# 7.Object (Nesne)
Nesneler birden fazla değer alabilir. Nesne tanımlamaları **özellik  :  değeri** şeklinde yapılır.

```
const rectangle = {
  length: 20,
  width: 20,
}
console.log(rectangle) // {length: 20, width: 20}

const person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'D3.js',
  ],
  isMarried: true,
}
console.log(person)
```
### Objenin Verilerine Ulaşma
Objenin verilerine 2 farklı yolla erişebiliriz.
```
const person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'D3.js',
  ],

}

// . kullanarak
console.log(person.firstName)
console.log(person.lastName)


// [''] kullanarak
console.log(person['firstName'])
console.log(person['lastName'])

```
     
### Method
Objeye işlem yapabilme yeteneği kazandıran fonksiyonlardır.

```
const person = {
  firstName: 'Asabeneh',
  lastName: 'Yetayeh',
  age: 250,
  country: 'Finland',
  city: 'Helsinki',
  skills: [
    'HTML',
    'CSS',
    'JavaScript',
    'React',
    'Node',
    'MongoDB',
    'Python',
    'D3.js',
  ],
  getFullName: function () {
    return `${this.firstName} ${this.lastName}`
  },
}

console.log(person.getFullName())
// Asabeneh Yetayeh

```
**Objenin sahip olduğu farklı yöntemler bulunmaktadır.**
### Object.assign
Orjinal nesneyi bozmadan kopyalamak için kullanılır.

  ```
  const person = {
  firstName: 'Asabeneh',
  age: 250,
  city: 'Helsinki',
  skills: ['HTML', 'CSS', 'JS'],
  title: 'teacher',
  address: {
    street: 'Heitamienkatu 16',
    pobox: 2002,
    city: 'Helsinki',
  },
  getPersonInfo: function () {
    return `Ben ${this.firstName} ve ${this.city} yaşıyorum. ${this.age} yaşındayım.`
  },
}

const copyPerson = Object.assign({}, person)
console.log(copyPerson)
  ```   
  ### Object.keys
  Objenin özelliklerini veya anahtarlarını dizi olarak almak için kullanılır.
  ```   
  const keys = Object.keys(copyPerson)
console.log(keys) 
//['name', 'age', 'country', 'skills', 'address', 'getPersonInfo']

const address = Object.keys(copyPerson.address)
console.log(address) 
//['street', 'pobox', 'city']
  ```   
  ### Object.values
   Bir nesnenin değerlerini dizi olarak almak için kullanılır.
   
    const values = Object.values(copyPerson)
    console.log(values)
   ###  Object.entries
   Bir dizideki anahtarları ve değerleri almak için kullanılır.
   ```   
   const entries = Object.entries(copyPerson)
console.log(entries)
   ```   
###  hasOwnProperty
Bir nesnede belirli bir anahtarın veya özelliğin mevcut olup olmadığını kontrol etmek için kullanılır.
```   
console.log(copyPerson.hasOwnProperty('name'))
console.log(copyPerson.hasOwnProperty('score'))
```   

# 8.Functions
Belirli bir görevi gerçekleştirmek için kullanılan kod bloğudur.Kodun temiz ve kolay okunmasını ,yeniden kullanılabilmesini ve test etmeyi kolay hale getirir.
```   
function addTwoNumbers() {
  let numOne = 10
  let numTwo = 20
  let sum = numOne + numTwo

  console.log(sum)
}

addTwoNumbers() // çağırma
```   

**return, fonksiyon tarafından döndürülen değeri belirler.**

```  
function addTwoNumbers() {
  let numOne = 2
  let numTwo = 3
  let total = numOne + numTwo
  return total
}

console.log(addTwoNumbers())
```  
**Fonksiyona parametre olarak farklı veri türleri gönderilebilir.**
```   
function areaOfCircle(r) {
  let area = Math.PI * r * r
  return area
}

console.log(areaOfCircle(10)) 
```   

```  
function sumTwoNumbers(numOne, numTwo) {
  let sum = numOne + numTwo
  return sum
}

console.log(sumTwoNumbers(10, 20))
```  

### Anonymous Function
```  
const anonymousFun = function () {
  console.log(
    'Merhaba Dünya'
  )
}
```  
### Expression Function
Anonim fonksiyonun parametreye sahip olup return ile bir değer elde ettiğimiz fonksiyonlardır.
```  
const square = function (n) {
  return n * n
}

console.log(square(2)) // -> 4
```  
###  Self Invoking Functions
Bir değer döndürmeleri için bu fonksiyonu kullanırken değer göndermemize gerek yok.
```  
let squaredNum = (function (n) {
  return n * n
})(10)

console.log(squaredNum)
```  
#### Arrow Function
Arrow fonksiyonlar, normal fonksiyonlara alternatiftir.function anahatar kelimesinin yerine arrow function sembolü geliyor.
```
function square(n) {
  return n * n
}

console.log(square(2)) // 4

const square = (n) => {
  return n * n
}

console.log(square(2)) // 4
```  
Normal fonksiyonlardan farklı olarak arrow fonksiyonlarda return anahtar kelimesi kullanılmadan da geriye değer döndürülebilir.Kodun bir satırdan oluşması ve süslü parantez içinde bulunmaması gerekir.
```  
const printFullName = (firstName, lastName) => `${firstName} ${lastName}`

console.log(printFullName('Asabeneh', 'Yetayeh'))
```  
#### Function with default parameters
fonksiyonu çağırırken değer gönderilmeyen durumlar için varsayılan bir parametre belirlenebilir.
```
function greetings(name = 'Peter') {
  let message = `${name}, hoş geldin`
  return message
}

console.log(greetings())  // Peter,hoş geldin
console.log(greetings('Mark')) // Mark, hoş geldin
```
```
const greetings = (name = 'Peter') => {
  let message = name + ', hoş geldin'
  return message
}

console.log(greetings()) // Peter,hoş geldin
console.log(greetings('Mark')) // Mark, hoş geldin
```

# 9.Higher Order Function
Parametre olarak başka bir fonksiyonu alan veya sonuç olarak başka bir fonksiyonu dönen fonksiyonlardır.
Yüksek Mertebe Fonksiyonlar, soyutlamaların yapılmasına olanak sağlayarak,fonksiyon API’lerin oluşturulmasında yardımcı olur.
### Callback
Fonksiyonun başka bir fonksiyona parametre olarak gönderilmesidir.
```
const callback = (n) => {
  return n ** 2
}
​

function cube(callback, n) {
  return callback(n) * n
}
​
console.log(cube(callback, 3)) //27
```
#### Returning function
Yüksek dereceli fonksiyonlar, fonksiyonu döndürebilir(return).
```
const higherOrder = n => {
  const doSomething = m => {
    const doWhatEver = t => {
      return 2 * n + 3 * m + t
    }
    return doWhatEver
  }
​
  return doSomething
}
console.log(higherOrder(2)(3)(10))
```
## setting time
JavaScript'te, belirli bir zaman aralığında bazı etkinlikler gerçekleştirilebilir veya bir süre için bazı etkinlikler tekrarlı olarak gerçekleştirilebilir.

 - setInterval 
 - setTimeout
 
 #### setInterval
 Fonksiyonun belirli aralıklarla çalışması için kullanılır.
```
function sayHello() {
  console.log('Selam')
}
setInterval(sayHello, 2000) // her 2 saniyede konsolda Selam yazar
```
#### setTimeout
Fonksiyonun belirli bir zamandan sonra çalışması için kullanılır.
```
function sayHello() {
  console.log('Selam')
}
setTimeout(sayHello, 2000) // 2 saniye sonra konsolda Selam yazar
```
# 10.Destructuring and Spreading

Destructuring bir obje veya bir array içinden her bir elemanın alınıp bir degişken içine kaydedilmesi işlemidir.
### 1. Destructuring arrays
```
const numbers = [1, 2, 3]
const [num1, num2, num3] = numbers
console.log(num1, num2, num3) // 1, 2, 3,

const countries = ['Finland', 'Sweden', 'Norway']
const [fin, swe, nor] = countries
console.log(fin, swe, nor) // Finland, Sweden, Norway
```

#### İç içe (Nested) Dizilerde Destructuring
```
const fullStack = [
  ['HTML', 'CSS', 'JS', 'React'],
  ['Node', 'Express', 'MongoDB']
]

const [frontEnd, backEnd] = fullstack
console.log(frontEnd, backEnd)

//["HTML", "CSS", "JS", "React"] , ["Node", "Express", "MongoDB"]
```
### 2. Destructuring objects
```
const props = {
  user:{
    firstName:'Asabeneh',
    lastName:'Yetayeh',
    age:250
  },
  post:{
    title:'Destructuring and Spread',
    subtitle:'ES6',
    year:2020
},
skills:['JS', 'React', 'Redux', 'Node', 'Python']

}
}

const {user, post, skills} = props
const {firstName, lastName, age} = user
const {title, subtitle, year} = post
const [skillOne, skillTwo, skillThree, skillFour, skillFive] = skills
```
## Spread or Rest Operator
Spread  sıfır yada daha fazla parametre alan fonksiyonların kullanımında, string veya array(dizi) gibi ifadelerin fonksiyon parametrelerinde yinelenebilir şekilde kullanılmasına ve genişletilmesine olanak sağlar.
**Dizilerde**
```
const nums = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
let [num1, num2, num3, ...rest] = nums
​
console.log(num1, num2, num3)
console.log(rest)
/* 1 2 3
[4, 5, 6, 7, 8, 9, 10] */ 
```
**Nesnelerde**
```
const user = {
  name: 'Asabeneh',
  title: 'Programmer',
  country: 'Finland',
  city: 'Helsinki',
}

const copiedUser = { ...user }
console.log(copiedUser)
// {name: "Asabeneh", title: "Programmer", country: "Finland", city: "Helsinki"}
```
**Arrow Fonksiyonlarda**
```
const sumAllNums = (...args) => {
  console.log(args)
}

sumAllNums(1, 2, 3, 4, 5)
//[1, 2, 3, 4, 5]
```
# 11.Functional Programming
İşlevsel programlama, daha kısa ve temiz kod yazmamıza ayrıca geleneksel bir şekilde çözülmesi zor olabilecek karmaşık sorunları çözmenize olanak tanır.
-   forEach
-   map
-   filter
-   reduce
-   find
-   findIndex
-   some
-   every
### forEach
ForEach yöntemi yalnızca dizi ile kullanılır .Öğe,indeks veya her ikisiyle ilgileniyorsak forEach kullanırız.
```
const countries = ['Finland', 'Estonia', 'Sweden', 'Norway']
const newCountries = []
countries.forEach((country) => newCountries.push(country))

console.log(newCountries) // ["Finland", "Estonia", "Sweden", "Norway"]
```
### map
Bir diziyi değiştirmek istediğimizde eşleme yöntemini kullanırız.Map metodunu sadece dizilerle kullanıyoruz ve her zaman bir dizi döndürüyor.
```
const countries = ['Finland', 'Estonia', 'Sweden', 'Norway']
const newCountries = countries.map((country) => country.toUpperCase())

console.log(newCountries) // ["FINLAND", "ESTONIA", "SWEDEN", "NORWAY"]
```
```
const countries = ['Finland', 'Estonia', 'Sweden', 'Norway']
const countriesLength = countries.map((country) => country.length)

console.log(countriesLength) // [7, 7, 6, 6]
```
### filter
filtre yöntemi bir dizi ile kullanılır ve filtrelenmiş öğelerden oluşan bir dizi döndürür.
```
const countries = ['Finland', 'Estonia', 'Sweden', 'Norway', 'Iceland']
const countriesWithLand = countries.filter((country) =>
  country.includes('land')
)
console.log(countriesWithLand) // ["Finland", "Iceland"]
```
### reduce
Bir dizideki tüm sayıları bir arada toplamak veya bir dizideki öğeleri çarpmak veya öğeleri birleştirmek için kullanırız.
```
const numbers = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
const sum = numbers.reduce((acc, cur) => acc + cur)
console.log(sum) // 55
```
```
const strs = ['Hello', 'world', '!']
const helloWorld = strs.reduce((acc, cur) => acc + ' ' + cur)
console.log(helloWorld) // "Hello world !"
```
### find 
Dizide gönderilen parametreye uygun olan ilk veriyi bulur.
```
const countries = ['Finland', 'Estonia', 'Sweden', 'Norway', 'Iceland']
const index = countries.find((country) => country.includes('o'))
console.log(index) // Estonia
```
### findIndex
find ile çalışma prensibi aynıdır.Tek farkı eşleşen değerinin index değerini döndürür.
```
const countries = ['Finland', 'Estonia', 'Sweden', 'Norway', 'Iceland']
const index = countries.findIndex((country) => country.includes('o'))
console.log(index) // 1
```
### some
dizi ile kullanılır ve bir mantıksal değer döndürür. Maddelerden biri veya birkaçı kriterleri karşılıyorsa sonuç doğru, aksi takdirde yanlış olacaktır.
```
const evens = [0, 2, 4, 6, 8, 10]
const someAreEvens = evens.some((n) => n % 2 === 0)
const someAreOdds = evens.some((n) => n % 2 !== 0)
console.log(someAreEvens) // true
console.log(someAreOdds) // false
```
### every 
some ile benzerdir ancak every tüm verilerin koşulu sağlayıp sağlamadığını kontrol eder.
```
const evens = [0, 2, 4, 6, 8, 10]
const someAreEvens = evens.some((n) => n % 2 === 0)
const someAreOdds = evens.some((n) => n % 2 !== 0)

console.log(someAreEvens) // true
console.log(someAreOdds)  // false
```
# 12.Classes
Javascript programlama dili, geleneksel programlama dillerindeki gibi gelişmiş özelliklere sahip olmasa da  _nesneye yönelik programlama_  açısından son derece esnek bir yapıya sahiptir.

Javascript dilinde  **class** benzeri tanımlamalar fonksiyonlar yardımıyla yapılmaktadır. Her fonksiyon bir  **class**  olarak değerlendirilebilir ve her fonksiyonun  _**new**_ anahtar sözcüğü ile bir nesnesi oluşturulabilir.

#### Class Tanımlama
```
class Person {
  // code goes here
}
```
Class dan obje oluşturmak:
```
const person = new Person()
```
#### Class Constructor
Object’in (nesnenin) oluşturduğu yapıcı metoda erişmek için kullanılan özelliktir.
```
class Person {
  constructor(firstName, lastName) {
    this.firstName = firstName
    this.lastName = lastName
  }
}

const person1 = new Person('Asabeneh', 'Yetayeh')

console.log(person1)
// Person {firstName: "Asabeneh", lastName: "Yetayeh"}
```
**Default values with constructor**
Varsayılan değerlere sahiptirler.
```
class Person {
  constructor(
    firstName = 'Asabeneh',
    lastName = 'Yetayeh',
    age = 250,
    country = 'Finland',
    city = 'Helsinki'
  ) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
  }
}

const person1 = new Person() 
console.log(person1)
//Person {firstName: "Asabeneh", lastName: "Yetayeh", age: 250, country: "Finland", city: "Helsinki"}

const person2 = new Person('Lidiya', 'Tekle', 28, 'Finland', 'Espoo')
console.log(person2)
//Person {firstName: "Lidiya", lastName: "Tekle", age: 28, country: "Finland", city: "Espoo"}
```
#### Class methods
Yöntemler, classın içindeki JavaScript işlemleridir.
```
class Person {
  constructor(firstName, lastName, age, country, city) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
  }
  getFullName() {
    const fullName = this.firstName + ' ' + this.lastName
    return fullName
  }
}

const person1 = new Person('Asabeneh', 'Yetayeh', 250, 'Finland', 'Helsinki')
const person2 = new Person('Lidiya', 'Tekle', 28, 'Finland', 'Espoo')

console.log(person1.getFullName())
console.log(person2.getFullName())
//Asabeneh Yetayeh
//test.js:19 Lidiya Tekle
```
#### Properties with initial value
Bazı özellikler için bir sınıf oluşturduğumuzda bir başlangıç değerimiz olabilir ancak başlangıçta var olan değerimizi daha sonrasında değiştirebiliriz.
```
class Person {
  constructor(firstName, lastName, age, country, city) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.score = 0
  }
  getFullName() {
    const fullName = this.firstName + ' ' + this.lastName
    return fullName
  }
}

const person1 = new Person('Asabeneh', 'Yetayeh', 250, 'Finland')

console.log(person1.score) //0
```
#### getter
Objeden değere erişmemize izin verir.Özelliklere doğrudan objeden erişmek yerine, değeri elde etmek için  kullanılır.
```
class Person {
  constructor(firstName, lastName, age, country, city) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.score = 0
  }
  get getScore() {
    return this.score
  }
}

const person1 = new Person('Asabeneh', 'Yetayeh', 250, 'Finland')

console.log(person1.getScore) //0
```
#### setter
Özelliklerin değerini değiştirmemize izin verir.
```
class Person {
  constructor(firstName, lastName, age, country, city) {
    this.firstName = firstName
    this.lastName = lastName
    this.age = age
    this.country = country
    this.city = city
    this.score = 0
    this.skills = []
  }
  get getScore() {
    return this.score
  }
  set setScore(score) {
    this.score += score
  }
}

const person1 = new Person('Asabeneh', 'Yetayeh', 250, 'Finland', 'Helsinki')

person1.setScore = 1
console.log(person1.score) //1
```
#### Static method
Statik yöntemler, sınıfla doğrudan ilgili olan ancak sınıfın nesnesi içinde bir işe yaramayan veya kullanılmayacak olan yöntemlerdir. Statik yöntemler kullanılarak sınıfla ilgili bazı genel amaçlı yöntemleri sınıf tanımlaması içinde yapar ve böylece bir bütünlük ve düzen sağlamış oluruz.
```
 class  Nokta  {
   constructor(x, y)  {
    this.x = x;
    this.y = y;
    }

  static ikiNoktaArasindakiUzaklik(nokta1, nokta2)  {
    var xFarki = nokta1.x - nokta2.x;
    var yFarki = nokta1.y - nokta2.y;
    return  Math.sqrt(xFarki * xFarki + yFarki * yFarki);
    }
  }
 var p1 =  new  Nokta(3,  5);
 var p2 =  new  Nokta(30,  40);

 var uzaklik =  Nokta.ikiNoktaArasindakiUzaklik(p1, p2);

 console.log(uzaklik);  // 44.204072210600685 
 console.log(p1.ikiNoktaArasindekiUzaklik);  // undefined  
```
#### Inheritance
Kalıtımı kullanarak, ana sınıfın tüm özelliklerine ve yöntemlerine erişebiliriz. Bu, kodun tekrarlanmasını azaltır.
```
class Student extends Person {
  saySomething() {
    console.log('Ben person classından türedim')
  }
}

const s1 = new Student('Asabeneh', 'Yetayeh', 'Finland', 250, 'Helsinki')
console.log(s1)
console.log(s1.saySomething())
console.log(s1.getFullName())

/* Student {firstName: "Asabeneh", lastName: "Yetayeh", age: "Finland", country: 250, city: "Helsinki", …}
I am a child of the person class
Asabeneh Yetayeh 
*/
```

# 13.Document Object Model(DOM)
DOM, HTML dökümanları içerisinde bulunan nesnelere kolaylıkla erişim sağlamak ve üzerinde işlemler yapabilmek için tasarlanan bir modeldir.HTML, gibi belgelerin diğer programlama dilleri veya script dilleriyle iletişim kurabilmesini sağlamak için geliştirilmiş bir arabirimdir. DOM ile HTML dosyamızda bulunan **her şeye** erişim sağlayabiliriz. DOM, nesneler ve özelliklerden oluşur.

```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="utf-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1" />
    <title>React App</title>
  </head>

  <body>
    <!-- <div class="root"></div> -->
    <div id="root"></div>

    <script>
      // const root = document.querySelector('.root')
      // const root = document.getElementById('root')
      const root = document.querySelector('#root')
      root.innerHTML = <h1>Hoş Geldiniz </h1>
    </script>
  </body>
</html>
```
