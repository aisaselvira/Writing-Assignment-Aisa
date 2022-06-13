WRITING ASSIGNMENT - MINGGU 2 
AISA SELVIRA
========================================

## **1. Javascript Dasar - Scope** 
### Scope = Konsep dalam flow data variabel. Variable Scope merupakan wilayah program yang sudah ditentukan
### Blocks = Suatu code yang terdapat didalam curly braces {}
### <br>

### - **Local Scope**
#### => Variabel yang dideklarasikan di dalam fungsi pada JavaScript. Variabel lokal hanya dapat diakses dari dalam fungsi tersebut.

### - **Global Scope**
#### => Variabel yang dapat diakses oleh setiap kode yang ada, baik di luar, maupun di dalam function.
### <br><br>
---------------------------------------------------

### <br><br>

## **2. Javascript Dasar - Function** 

### Function = Sebuah blok kode yang dirancang dalam sebuah grup untuk menyelesaikan 1 task / 1 fitur. 
### <br>

### **Contoh :**
```
function greeting{
    return 'Hello Word';
};
```
### <br>
### - Parameter Function
### Tercantum di dalam tanda kurung () dalam definisi fungsi. Dengan parameter, function dapat menerima sebuah inputan data dan menggunakannya untuk melakukan tugas. 

### <br>
### **Contoh :** 
```
function myFunction(p1, p2) {
    return p1 * p2;   // The function returns the product of p1 and p2
}
```

### <br>
### - Argumen Function
### Nilai yang diterima oleh fungsi saat dipanggil.

### <br>
### **Contoh :** 
```
function myFunction(p1, p2) {
    return p1 * p2;   // The function returns the product of p1 and p2
}
console.log(myFunction(3,2)); // output 6
```

### <br>
### - Default Parameters
### Digunakan untuk memberikan nilai awal / default pada parameter function dan bisa digunakan jika kita ingin menjaga function agar tidak error saat dipanggil tanpa argumen

### <br>
### **Contoh :**
```
function greetOnWebsite(name = 'Stranger')
    return 'Hello' + name;
}
console.log(greetOnWebsite('David'));
console.log(greetOnWebsite());
```

### <br>
### - Function Helper
### Function yang sudah dibuat pada function lain.
```
function multiplyByNineFifths(number) {
    return number * (9/5);
};
function getFahrenheit(celsius) {
    return multiplyByNineFifths(celcius) + 32;
};
getFarenheit(15);
```

### <br>
### - Arrow Function
### Cara lain menuliskan function. Fitur terbaru yang ada pada ES6 (Javascript Version)
```
const greeting = () => {
    return "Hello World!";
};

const penambahan = (a,b) => {
    return a + b;
};
```
### <br><br>
---------------------------------------------------

### <br><br>

## **3. Javascript Dasar - DOM Manipulation** 
### Standar untuk mendapatkan, mengubah, menambah, atau menghapus elemen HTML. DOM bukan bagian dari JavaScript, melainkan browser (Web API)
### <br>
## *Memanipulasi Element HTML*
* Mencari Element HTML
```
<p id="demo"></p>               <--------->   document.getElementById("demo");
<div class="container"></div>   <--------->   document.getElementByClassName("container"); 
<p id="demo"></p>               <--------->   document.querySelector("#demo");
<div class="container"></div>   <--------->   document.querySelector(".container"); 
```
### <br>
* Mengubah Konten Element
```
1. Element.textContent
Untuk mengubah teks di dalam sebuah element

2. Element.innerHTML
Untuk mengubah konten HTML di dalam sebuah element.
```
### <br>
* Membuat Element HTML
#### *createElement -> textContent -> appenChild* ####
```
<div id="header"></div>

const heading = document.createElement("h1")            
heading.textContent = "Ini merupakan heading";          

document.getElementById("header").appenChild(heading)   

// Hasil pada HTML
<div id="header">
    <h1>Ini merupakan heading</h1>
</div>
```
### <br>
## *Interaksi User (Events)* 
### **Menangkap Interaksi User**
#### - Element.addEventListener(“event”)
#### - Element.onevent
### <br>
### **Event Listener**
### *Dengan cara Element.addEventListener(“event”)*
- Bisa dihilangkan
- Bisa ada beberapa event listener yang sama untuk 1 element
- Memiliki argument tambahan { options }

### <br>
### 1. ) EventListener - Click
### 2. ) EventListener - Blur
### 3. ) EventListener - Form Submission

-----------------------------------------------

### EventListener - Click
####  Menampilkan pop up box.
### **Contoh :**
```
const input = document.getElementById(“user-input”)
const button = document.getElementById(“alert-button”)

button.addEventListener(“click”, function() {
	alert(input.value)
})

// atau
button.onclick = function() { alert(input.value) }

```
### <br><br>
---------------------------------------------------

### <br><br>

## **4. JS Intermediate - Array** 
### Tipe data list order yang dapat menyimpan tipe data apapun di dalamnya seperti String, Number, Boolean, dll.
### Array digunakan untuk menyimpan banyak nilai dalam satu variabel.
### **Contoh :**
```
const cars = ["Pajero", "Avanza", "BMW"];
console.log(cars);

let Data = ["Aisa", "18", "true"];
console.log(Data);
```
### <br>
* Membuat Array
```
Didefinisikan menggunakan square brackets []
```

* Mengakses / Memanggil Array
### Array akan menyimpan sekumpulan data dan memberinya nomer indeks agar mudah diakses.
### Indeks array selalu dimulai dari nol 0.
### **Contoh :**
```
const cars = ["Pajero", "Avanza", "BMW"];
console.log(cars[1]); // Avanza

```
* Update Array
### **Contoh :**
```
const cars = ["Pajero", "Avanza", "BMW"];
cars[0] = 'Lamborgini';
console.log(); 

// ['Lamborgini', 'Avanza', 'BMW' ];
```
* Const in Array
### Kita dapat mengubah array dengan array baru & konten nilai yang ada didalam array dengan nilai lain ketika menggunakan let.
### Const tidak bisa melakukan update data. Namun pada Array dapat melakukan update konten nilai didalam array (mutable).

* Array Properties
### Properties : Fitur yang disediakan oleh Javascript untuk memudahkan developer
### 1. Constructor
### 2. Length
### 3. Index
### 4. Input
### 5. Prototype
--------------------------------------------------
### *.length*
### Length akan mengembalikan nilai dari jumlah panjang data suatu array.

* Array Method
### Javascript menyediakan function / method umum untuk memudahkan kita dalam menggunakannya. Tidak perlu membuat function lagi jika method yang kita butuhkan sudah tersedia.
### **Contoh :**
```
.push()
Method untuk menambahkan item  array pada urutan yang paling akhir.


```
```
.pop()
Method yang menghapus item array index terakhir.

```
```
.shift()
Method untuk menghapus item Array pada index pertama.

```
```
.unshift()
Method untuk menambahkan item Array pada index pertama.

```
```
.sort()
Method untuk mengurutkan secara Ascending atau Descending Alphanumeric.

```
* Looping pada Array
### forEach() dan .map() melakukan looping dan mengembalikan nilai baru dari operasi yang dilakukan
### <br>
### *1.) .forEach() adalah method untuk melakukan looping pada setiap elemen array.*
```
let arr = [1, 2, 3, 4, 5];
arr.forEach ((num, index) => {
    return arr[index] = num * 2;
});
console.log(arr);
// [2, 4, 6, 8, 10]
}
```
### *2.) .map() melakukan perulangan/looping dengan membuat array baru.*
```
let arr = [1, 2, 3, 4, 5];

let doubled = arr.map(num => {
    return num * 2;
});
console.log(doubled);
// '2','4','6','8','10'
```
### **Perbedaan :**
### - **.forEach** tidak dapat membuat Array baru dari hasil operasi yang ada dalam looping & dari segi performance sangat jauh. .forEach() digunakan jika hanya memerlukan looping untuk menampilkan saja atau menyimpan ke database.
### - **.map()** digunakan jika akan melakukan operasi pada array seperti yang dapat mengubah nilai array sebelumnya.

### <br><br>
---------------------------------------------------

### <br><br>

## **5. JS Intermediate - Object** 
### Object : Sebuah tipe data pada variabel yang menyimpan properti dan fungsi (method)
### Properti adalah data lengkap dari sebuah object.
### Method adalah action dari sebuah object. 

* Membuat sebuah object
### Object dapat diassign kedalam sebuah variabel
### Didalam object kita dapat menyimpan properti dengan tipe data apapun.
### **Contoh :**
```
let person = {
    name: 'Aisa',
    age: 18,
    isVerified: true,
};
```
* Mengakses Object dan Property Object
```
- Mengakses Object

let person = {
    name: 'Aisa',
    age: 18,
    isVerified: true,
};
console.log(person); // call variable name to access object

let person = {
    name: 'Aisa',
    age: 18,
    'current address': 'Solo, Jateng', // menggunakan single quote pada key
};


- Mengakses Properti

1. Dot Notation

let person = {
    name: 'Aisa',
    age: 18,
    isVerified: true,
};
console.log(person.name); 

2. Bracket Notation

let person = {
    name: 'Aisa',
    age: 18,
    isVerified: true,
};
console.log(person['name']);
```

* Update Object
### 1. Dot 
### **Contoh :**
```
let student = {
    name: 'Melvin',
    age: 20
}
student.hobby = 'writing'
console.log(student);
```
### 2. Bracket
### **Contoh :**
```
let student = {
    name: 'Melvin',
    age: 20
}
student['address'] = 'Bandung'
console.log(student);

```
* Delete Object Property
### Delete operator
### **Contoh :**
```
let person = {
    name: 'Aisa',
    age: 18,
    isVerified: true,
};
delete person.age;
console.log(person);
```

* Nested Object
### Object yang berasal dari turunan object lainnya.
### **Contoh :**
```
const bookInfo = {
    title: 'Laskar pelangi',
    year: 2005,
    author: {
        name: 'Andrea Hinata',
        age: 55,
        address: 'Solo'
    }
}
console.log(bookInfo);
``` 

* Looping Object
### Menampilkan seluruh object properti menggunakan looping, tidak perlu mengakses secara manual memanggil setiap propertinya.
### **Contoh :**
```
const bookInfo = {
    title: 'Laskar pelangi',
    year: 2005,
    author: {
        name: 'Andrea Hinata',
        age: 55,
        address: 'Solo'
    }
}

for (let key bookfInfo){
    console.log(bookfInfo[key]);
}
```

* Array of Object
### Sama seperti Array yang bisa menyimpan banyak data. Array of object dapat digunakan untuk data yang lebih dari satu.
### **Contoh :**
```
let dataAge = [20, 17, 18]
let dataStudent = [
    {
        name: 'jessica',
        isVerivied: true,
    },
    {
        name: 'william',
        isVerivied: true,
    },
    {
        name: 'chika',
        isVerivied: false,
    }
];

dataStudent.forEach((listStudent) => {
    console.log(listStudent);
})
```
























